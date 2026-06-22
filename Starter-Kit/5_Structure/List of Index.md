---
tags:
  - type/structure
  - structure/list
  - structure/index
  - type/dataview
  - target/starterkit
aliases:
  - Index
created: 2026-06-22, 17:15
modified: 2026-06-22, 17:15
template_type: Structure
view_count: 1
---

# List of Index
<!-- All index / MOC notes across the vault. -->

```dataview
TABLE WITHOUT ID
	file.link AS Index,
	length(file.inlinks) AS "Inlinks"
FROM #structure/index OR #structure/moc
SORT length(file.inlinks) DESC
```
