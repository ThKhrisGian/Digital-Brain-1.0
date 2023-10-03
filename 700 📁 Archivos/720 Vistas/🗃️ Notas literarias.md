---
banner_icon: 🗃️
banner: "![[banner01.png]]"
banner_y: 0.73695
banner_lock: true
---
# Notas literarias

```button
name Nueva Nota Literaria
type command
action QuickAdd: 300 Nueva Nota Literaria
color blue
```
^button-new-literature-note
---
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Tipo"],
		dv.pages("#🗃️")
		.sort(p => p.file.ctime, "desc")
		.filter(p => !p.file.path.includes("Plantillas"))
		.map(p => [
		p.file.link,
		f(dv, p, "Tipo")
		])
		)
```