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

# Inspect Folder Usage
<!-- Note counts per folder. -->

```dataview
TABLE WITHOUT ID
	folder AS Folder,
	length(rows) AS Notes
FROM ""
GROUP BY file.folder AS folder
SORT length(rows) DESC
```
