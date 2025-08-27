<%* 
week = await tp.system.prompt("Week number") 
courseCode = await tp.system.prompt("Course code (e.g. REL4322)")
focus = await tp.system.prompt("Focus question / instructions")
await tp.file.rename(`Week-${week}`)
%>
---
type: assignment
course: <% `#${courseCode}` %>
week: <% week %>
focus: <% focus %>
---

# Student Submission
