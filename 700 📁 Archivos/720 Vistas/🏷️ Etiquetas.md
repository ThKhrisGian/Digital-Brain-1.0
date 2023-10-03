---
banner_icon: 🏷️
banner: "![[banner01.png]]"
banner_y: 0.73695
banner_lock: true
---
# Etiquetas

```button
name Nueva Etiqueta
type command
action QuickAdd: 500 Nueva Etiqueta
color blue
```
^button-new-tag
---
```dataview
list
from #🏷️ and -"700 📁 Archivos"
sort file.name
```