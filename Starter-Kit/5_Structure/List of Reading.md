---
tags:
  - type/structure
  - structure/list
  - type/dataview
  - target/starterkit
aliases:
created: 2026-06-22, 17:15
modified: 2026-06-22, 17:15
template_type: Structure
view_count: 1
---

# List of Reading
<!-- Notes with a reading status or year read. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	status AS Status,
	read AS "Read"
FROM ""
WHERE read OR status = "reading"
SORT read DESC
```
