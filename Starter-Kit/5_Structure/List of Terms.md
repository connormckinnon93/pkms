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

# List of Terms
<!-- All term/definition notes across the vault. -->

```dataview
TABLE WITHOUT ID
	file.link AS Term,
	lead AS Definition
FROM #type/term
SORT file.name ASC
```
