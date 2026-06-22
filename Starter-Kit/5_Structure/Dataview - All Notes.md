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

# Dataview - All Notes
<!-- Every note in the vault, by last modified. -->

```dataview
TABLE WITHOUT ID
	file.link AS Note,
	file.folder AS Folder,
	file.mday AS Modified
FROM ""
SORT file.mday DESC
```
