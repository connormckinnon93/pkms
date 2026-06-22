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

# Notes with SEE references
<!-- Notes that carry a see:: cross-reference. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	see AS "See"
FROM ""
WHERE see
SORT file.name ASC
```
