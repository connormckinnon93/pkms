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

# 7 Days - Summary

| [7 Days - Created](7%20Days%20Created%20Chart.md) | [7 Days - Summary](7%20Days%20Created%20List.md) | [7 Days - Modified](7%20Days%20Modified%20Chart.md) | [7 Days - Table](7%20Days%20Table.md) |

<!-- Notes created in the last 7 days. -->

```dataview
LIST
lead + " (" + file.cday + ")"
FROM ""
WHERE file.cday >= date(today) - dur(7 days)
SORT file.cday DESC
```
