#Cloud #AWS #Fundamentos
[[Daily/2024-04-16.md|2024-04-16]]
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
AWS Lambda es un servicio serverless que nos permite ejecutar código en respuesta a eventos, sin preocuparnos por servidores o infraestructura. Estos eventos pueden ser temporizadores, visitas a alguna sección de nuestra aplicación, solicitudes HTTP, entre otros.

Entre sus casos de uso encontramos el (pre)procesamiento de datos a escala, y la ejecución de backends web, móviles y de IoT interactivos. Lambda se puede combinar con otros servicios de AWS para crear experiencias en línea seguras, estables y escalables.
# ¿Cómo se factura Lambda?
Lambda se factura por milisegundos, y el precio depende del uso de RAM. Por ejemplo, 128MB RAM x 30 millones de eventos por mes resultan en un costo de $11.63 al mes.