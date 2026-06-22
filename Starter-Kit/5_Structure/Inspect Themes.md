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

# Inspect Themes
<!-- Note counts per #theme/ tag. -->

```dataview
TABLE WITHOUT ID
	theme AS Theme,
	length(rows) AS Count
FROM ""
FLATTEN file.etags AS theme
WHERE startswith(theme, "#theme/")
GROUP BY theme
SORT length(rows) DESC
```
