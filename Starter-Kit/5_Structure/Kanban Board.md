---
tags:
  - type/structure
  - structure/view
  - type/dataview
  - target/starterkit
aliases:
lead: Dataview kanban board — notes grouped by their kanban:: status (backlog / todo / doing / done).
created: 2026-06-22, 17:50
modified: 2026-06-22, 17:50
template_type: Structure
view_count: 1
---

# Kanban Board
[Home](Home.md) | [ARCO](ARCO%20View.md) | [Inspect](Inspect%20View.md)

> [!Note]
> `= this.lead`
> Set a `kanban` property on any note (`backlog`, `todo`, `doing`, `done`) to place it on this board.

> [!backlog]- Backlog
>```dataview
>TABLE WITHOUT ID
>	file.link as note,
>	file.cday AS "created",
>	file.folder AS "folder"
>FROM ""
>WHERE kanban = "backlog"
>SORT file.folder ASC
>```

> [!todo]- ToDo
>```dataview
>TABLE WITHOUT ID
>	file.link as note,
>	file.cday AS "created",
>	file.folder AS "folder"
>FROM ""
>WHERE kanban = "todo"
>SORT file.folder ASC
>```

> [!doing]+ Doing - _WIP Limit 3_
>```dataview
>TABLE WITHOUT ID
>	file.link as note,
>	file.cday AS "created",
>	file.folder AS "folder"
>FROM ""
>WHERE kanban = "doing"
>SORT file.folder ASC
>```

> [!done]- Done
>```dataview
>TABLE WITHOUT ID
>	file.link as note,
>	file.mday AS "modified",
>	file.folder AS "folder"
>FROM ""
>WHERE kanban = "done"
>SORT file.mday DESC
>```
