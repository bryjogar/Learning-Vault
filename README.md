# Obsidian Vault: Digital Garden, Course Builder, and Research Hub

Welcome to my Learning Vault! This workspace is designed for capturing fleeting thoughts, developing publishable articles, organizing research, and building entire courses with a repeatable workflow. It leverages powerful community plugins and custom templates to streamline my learning and writing process.

---

## 🚀 Quick Start

1. **Install Required Plugins:**
   - [Dataview](https://github.com/blacksmithgu/obsidian-dataview)
   - [Templater](https://github.com/SilentVoid13/Templater)
   - [Copilot](https://github.com/edward-borland/obsidian-copilot) (requires your own API key)

2. **Configure Plugins:**
   - **Templater:** Set templates folder to `90 System/Templates`. Assign hotkeys as desired (see below).
   - **Copilot:** Enter your API key, select your preferred AI backend, set default mode to "Vault QA", and set the default conversation folder to `00 Inbox`. Commands folder: `90 System/Prompts`.
   - **Dataview:** No special configuration needed for basic functionality.

3. **Personalize Your Vault:**
   - Update `20 Courses/Learning Preferences` with your learning style, background, and preferences. This helps tailor course and assignment generation.

---

## 🗂️ Vault Structure

- **00 Inbox/**: Capture all new notes, ideas, fleeting thoughts, and web clippings here. This is your "pre-processed" data.
- **10 Seeds/**: Processed but not yet integrated notes. Use the Seed template (`ALT+0`) to move items here.
- **20 Courses/**: Each course gets its own folder, created via the Course Scaffold template. Contains subfolders for Seeds, Assignments, and Notes.
- **90 System/**: Configuration, templates, and prompts.

---

## 🔄 Workflow Overview

1. **Capture:**  
   - Add new ideas to `00 Inbox/`.

2. **Seed Processing:**  
   - When ready, use `ALT+0` to insert the Seed template. This moves the note to `10 Seeds/` and adds relevant tags.

3. **Course Creation:**  
   - Use Copilot’s `/Course Proposal` command in QA Mode to generate a course outline from your seeds.
   - If you accept the proposal, right-click `20 Courses/` and create a new note from the `Course Scaffold` template. Enter the course code when prompted.
   - Copy relevant seeds into the course folder, updating their tag to `#CourseCode` (e.g., `#CS4227`).

4. **Syllabus Generation:**  
   - Use Copilot’s `/Syllabus Generation` command, referencing the course folder at the bottom of the prompt.
   - Paste the generated syllabus into the `Syllabus.md` file in the course folder.

5. **Assignments:**  
   - Use the assignment template to create new assignments in the course’s Assignments folder. Fill out the required fields.
   - Write your submission under the "Student Submission" heading.
   - When finished, use `ALT+9` to have Copilot grade your writing.

---

## 🛠️ Hotkey Reference

| Hotkey   | Action                                  |
|----------|-----------------------------------------|
| ALT+0    | Insert Seed Template                    |
| ALT+9    | Copilot: Grade My Writing               |

---

## 🧩 Templates & Automation

- **Seed Template:** Standardizes new ideas for course integration.
- **Course Scaffold:** Automates course folder and file creation.
- **Assignment Template:** Ensures consistent assignment structure.
- **Syllabus Generation:** Guided by strict requirements for coherence and academic rigor (see [[Syllabus Generation]]).

---

## 📚 Additional Notes

- **Learning Preferences:** Update `20 Courses/Learning Preferences` to help the AI tailor content to your needs.
- **Course Catalog & Grades:** Dataview is used to display course catalogs and grades (future feature).
- **Customization:** Feel free to adapt folder names, templates, and workflows to fit your needs.

---

## 📖 License

This vault is a personal learning and research tool. Please respect the privacy of unpublished notes and personal information.

---

Happy learning and creating!
