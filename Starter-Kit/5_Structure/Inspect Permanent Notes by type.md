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

# Inspect Permanent Notes by type
<!-- Permanent notes grouped by template_type. -->

```dataview
TABLE WITHOUT ID
	key AS Type,
	length(rows) AS Count,
	rows.file.link AS Notes
FROM "3_Permanent"
GROUP BY template_type
SORT length(rows) DESC
```
