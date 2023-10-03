---
banner_icon: 📌
banner: "![[banner01.png]]"
banner_y: 0.73695
banner_lock: true
---
# Recursos

```button
name Nuevo Recurso
type command
action QuickAdd: 200 Nuevo Recurso
color blue
```
^button-new-resource
---
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Tipo", "Estado"],
		dv.pages('#📌')
		.filter(p => !p.file.path.includes("Plantillas"))
		.filter(p => !p.file.path.includes("fileClass"))
		.sort(p => p.file.ctime, "desc")
		.map( p => [
		p.file.link,
		f(dv, p, "Tipo"),
		f(dv, p, "Estado")]
		)
		)
```