# Requirements
Community Plugins:
`Dataview`
`Copilot`
`Templater`

## Special Note for the Agent
`90 System/Config/Learning Preferences`

## Dataview
No settings changes required for functionality at this time. I'm using dataview just to display a course catalog and eventually to show grades per course.

## Templater
- Update the templates folder to be `90 System/Templates`
- Setup hotkeys as you choose 
	- Insert Seed = `ALT+0` in the below instructions

## Copilot
You must have your own API Key
Update your key, select your preferred AI backend for Chat
Update your Default Mode (Vault QA)
Update your Default Conversation Folder (00 Inbox)
Configure your commands folder to be `90 System/Prompts`

## Config Note
Update the `90 System/Config/Learning Preferences` note with any information about your learning style and preferences. Mine includes information about my work history so if I do a programming or networking class it designs it as one who already knows the basics.

## Hotkey Definitions
`ALT+0` = Insert Templater Template: Seed
`ALT+9` = Copilot: Grade My Writing
# Workflow
All new notes, ideas, fleeting thoughts, web clippings, etc. go into `00 Inbox/`. This folder is your 'pre-processed' data. You see an article or hear someone say something, just throw the note there. You'll come back to it later after you've had a moment to dwell on the idea. 

When you're ready to process simply insert the seed template with the hotkey `Alt+0`. This template will move the file to the `10 Seeds` folder and contains the seed and status tags as well as some brief headings for you to add information for the agent to process. This is the processed, but not yet integrated, folder.

After you feel like you have enough seeds to develop a course (can be as few as 1 seed) use the Copilot chat window (in QA Mode) and use the / command for `Course Proposal`. This will return a proposed course with all of the necessary components in the chat. If you like the course, right click on `20 Courses` and *add a new note from template*. Select the `Course Scaffold` template and apply the course code provided in the course template. This will create the necessary folders and information you need to finish putting your course together. 

Copy the relevant seeds (Anchor seed + any optional seeds you choose). Update their tag from `#seed` to `#$courseCode` (use the actual course code eg. `#CS4227`). Once the course file that matches the course code and seeds are in place, use the Copilot chat again with the / command for Syllabus Generation. At the very end of the prompt is `{20 Course/$CourseCode}` update with the correct course code so the agent can view all related materials. 

When the syllabus is created, copy and paste it to the `Syllabus` file in the course. You now have a fully ready course! Follow the syllabus and complete the readings and assignments as defined. 

Use the assignment template (right click on your assignments directory) to create new files and fill out the requested information: CourseTag (`#REL4300`), Focus Question, Week Number. The first heading should be "Student Submission" from there produce your assignment. When completed use the hotkey `ALT+9` to get the assignment graded. Insert this at the end of your document.