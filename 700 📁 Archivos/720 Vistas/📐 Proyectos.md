---
banner_icon: 📐
banner: "![[banner01.png]]"
banner_y: 0.73695
banner_lock: true
cssclass: max, table-max
---
# Proyectos
```button
name Nuevo Proyecto
type command
action QuickAdd: 400 Nuevo Proyecto
color blue
```
^button-new-project
---
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado"],
		 dv.pages("#📐")
		 .filter(p => !p.file.path.includes("Plantillas"))
		 .map(p => [
		 p.file.link,
		 f(dv, p, "F-inicio"),
		 f(dv, p, "F-limite"),
		 f(dv, p, "Estado")]))
```