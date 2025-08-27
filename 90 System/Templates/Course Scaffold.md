<%*
/* Course scaffold (creates folders, placeholder files, moves current note)
   - Prompts for Course Code (folder name)
   - Creates subfolders under 20 Courses/<COURSECODE>
   - Creates 00 Syllabus.md in course root and .keep placeholders in subfolders
   - Moves current active note into the new course folder
*/

const courseCode = await tp.system.prompt("Enter Course Code (e.g., REL4322):");
if (!courseCode) {
  tR += "⛔ Aborted: no course code provided.";
  return;
}

const basePath = `20 Courses/${courseCode}`;

// Subfolders you wanted — edit names/order as needed
const subfolders = [
  "Seeds",
  "Assignments",
  "Notes"
];

// helper: check existence
const exists = p => app.vault.getAbstractFileByPath(p) !== null;

// helper: create folder if missing
async function ensureFolder(p){
  if (!exists(p)) {
    await app.vault.createFolder(p);
  }
}

// helper: create empty file if missing
async function ensureFile(p){
  if (!exists(p)) {
    await app.vault.create(p, "");
  }
}

// ensure base courses folder and this course folder
await ensureFolder("20 Courses");
await ensureFolder(basePath);

// create subfolders
for (const f of subfolders) {
  await ensureFolder(`${basePath}/${f}`);
}

// create a syllabus placeholder at root of course
await ensureFile(`${basePath}/Syllabus.md`);

// create small .keep placeholders inside each subfolder so empty folders persist in sync/git
for (const f of subfolders) {
  await ensureFile(`${basePath}/${f}/.keep`);
}

// move the current active note into the course folder root
// new filename = original title + .md (avoid overwriting existing file)
const origTitle = `${courseCode}`;
let destPath = `${basePath}/${origTitle}`;

if (exists(destPath)) {
  // if file exists, append timestamp to avoid collision
  const stamp = tp.date.now("YYYYMMDD-HHmmss");
  destPath = `${basePath}/${origTitle}-${stamp}.md`;
}

// tp.file.move(destPath) moves the current file to destPath
await tp.file.move(destPath);

tR += `<!-- Copy the course proposal here, and add the courseTag -->`;
%>
