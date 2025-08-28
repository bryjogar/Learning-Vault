# Enrolled Courses
```dataview
table title
from #course-proposal 
where status="enrolled"
```

# Course Catalog
```dataview
table title
from #course-proposal
where !contains(file.name, "Course Proposal")
sort file.name
```


---
