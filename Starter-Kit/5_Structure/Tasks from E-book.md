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

# Tasks from E-book
<!-- Open tasks from e-book project notes. -->

```dataview
TASK
FROM #type/ebook OR #theme/ebook
WHERE !completed
GROUP BY file.link
```
