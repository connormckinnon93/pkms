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

# Project Notes - Days viewed
<!-- Most-viewed project notes (View Count plugin). -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	view_count AS "Views"
FROM "4_Project"
WHERE view_count
SORT view_count DESC
```
