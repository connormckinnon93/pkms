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

# Permanent Notes - Created
<!-- Permanent notes by creation date. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	created AS Created
FROM "3_Permanent"
SORT created DESC
```
