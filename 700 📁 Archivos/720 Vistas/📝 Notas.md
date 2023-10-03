---
banner_icon: 📝
banner: "![[banner01.png]]"
banner_y: 0.73695
banner_lock: true
---
# Notas

```button
name Nueva Nota
type command
action QuickAdd: 100 Nueva Nota
color blue
```
^button-new-note
---
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Estado"],
		dv.pages("#📝")
		.sort(p => p.file.ctime, "desc")
		.filter(p => !p.file.path.includes("Plantillas"))
		.limit(20)
		.map(p => [
		p.file.link,
		f(dv, p, "Estado")
		])
	)
```