Tipo:: 🎥
Estado:: 
Autor:: 
URL:: 
Etiquetas:: 
***
# Nuevo de recurso #📌


```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Tipo"],
		dv.pages()
		.where(p => p["De"] == "" + dv.current().file.link)
		.sort(p => p["Tipo"])
		.filter(p => !p.file.path.includes("Plantillas"))
		.map(p => [
		p.file.link,
		f(dv, p, "Tipo")
		])
		)
```