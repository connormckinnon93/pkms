---
tags:
  - type/structure
  - structure/list
  - type/dataview
  - target/starterkit
aliases:
created: 2026-06-23, 09:00
modified: 2026-06-23, 09:00
template_type: Structure
view_count: 1
---

# Ideas List
<!-- An inbox of raw ideas — fleeting notes awaiting processing. -->

```dataview
TABLE WITHOUT ID
	file.link AS Idea,
	file.cday AS "captured"
FROM "1_Fleeting"
SORT file.cday DESC
```
