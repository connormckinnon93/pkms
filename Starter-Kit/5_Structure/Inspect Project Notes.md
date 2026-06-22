---
tags:
  - type/structure
  - structure/view
  - type/dataview
  - target/starterkit
aliases:
created: 2026-06-22, 17:15
modified: 2026-06-22, 17:15
template_type: Structure
view_count: 1
---

# Inspect Project Notes
<!-- Project notes with status, sorted by last modified. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	status AS Status,
	file.mday AS Modified
FROM "4_Project"
SORT file.mday DESC
```
