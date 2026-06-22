---
tags:
  - type/structure
  - structure/view
  - type/dataview
  - target/starterkit
aliases:
created: 2026-06-22, 17:30
modified: 2026-06-22, 17:30
template_type: Structure
view_count: 1
---

# Tasks - Zettelkasten
<!-- Open tasks from notes themed Zettelkasten. -->

```dataview
TASK
FROM #theme/zettelkasten
WHERE !completed
GROUP BY file.link
```
