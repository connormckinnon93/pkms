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

# Permanent Notes - Days Viewed
<!-- Most-viewed permanent notes (View Count plugin). -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	view_count AS "Views"
FROM "3_Permanent"
WHERE view_count
SORT view_count DESC
```
