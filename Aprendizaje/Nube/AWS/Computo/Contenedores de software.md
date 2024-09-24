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
El propósito de un contenedor es **crear un paquete de tu programa y todas sus librerías y dependencias con las versiones específicas con las que has trabajado,** para producir una imagen que pueda ser **ejecutada en cualquier máquina.**

Un problema común del desarrollo de _software_ es utilizar distintas versiones de diferentes librerías/lenguajes de programación/programas. **Docker nos permite crear contenedores** para resolver este problema.
# Amazon ECS
[**Amazon ECS**](https://aws.amazon.com/es/ecs/) es un servicio de **contenedores**, donde puedes implementar tus imágenes en contenedores en AWS. Cuando corras tus contenedores en AWS, **no notarás diferencia entre tu máquina local y el entorno de AWS.**