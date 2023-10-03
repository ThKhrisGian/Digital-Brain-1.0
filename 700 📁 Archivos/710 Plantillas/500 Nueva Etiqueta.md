# <%tp.file.title%>
#🏷️
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;
let paginas = dv.pages(dv.current().file.link + "")

if (paginas.length > 0){
	dv.table(["Nombre", "Tipo"], paginas
		.sort(b => b.file.name)
		.map(b => [b.file.link, f(dv, b, "Tipo")]))
}
```