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

# Project Notes without source links
<!-- Project notes missing a based_on:: source. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note
FROM "4_Project"
WHERE !based_on
SORT file.name ASC
```
