---
limit: 100
mapWithTag: true
icon: clipboard-list
tagNames: [🗃️]
excludes: 
extends: 
version: 2
---

Tipo:: {"type":"Select","options":{"valuesList":{"1":"✍️","2":"📁","3":"🖼️","4":"🔗","5":"📃","6":"📋","7":"💬"},"sourceType":"ValuesList","valuesListNotePath":"","valuesFromDVQuery":""}}
De:: {"type":"File","options":{"dvQueryString":"dv.pages(\"#📌\").filter(p => !p.file.path.includes(\"710 Plantillas\"))\n.filter(p => !p.file.path.includes(\"fileClass\")).map(p => p.file.link)"}}
Etiquetas:: {"type":"MultiFile","options":{"dvQueryString":"dv.pages(\"#🏷️\")\n.filter(p => !p.file.path.includes(\"710 Plantillas\"))\n.filter(p => !p.file.path.includes(\"fileClass\"))\n.sort(b => b.file.link)"}}