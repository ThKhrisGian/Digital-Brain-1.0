---
mapWithTag: true
tagNames: [📝]
limit: 100
excludes: 
extends: 
---
Estado:: {"type":"Select","options":{"valuesList":{"1":"🌱","2":"🌿","3":"🌲"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
Etiquetas:: {"type":"MultiFile","options":{"dvQueryString":"dv.pages(\"#🏷️\")\n.filter(p => !p.file.path.includes(\"710 Plantillas\"))\n.filter(p => !p.file.path.includes(\"fileClass\"))\n.sort(b => b.file.link)"}}