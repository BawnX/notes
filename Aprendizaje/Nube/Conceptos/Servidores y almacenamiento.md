#Aprendizaje #Nube
[[2024-04-09]]
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
# ¿Cómo se componen los servidores?
PC que forma parte de una red y provee servicios a los
1. Sistema Operativo: Windows, Linux, MacOS
2. Aplicaciones: Apache, Nginx, IIS, PlatziWallet
3. Ubicación: Puede estar onpremises (Instalaciones de la empresa dueña) o nube (Espacio provisto por un proveedor puede ser AWS, Google, etc)
4. Servicio: Provee servicios a cantidad grande de usuarios
# ¿Qué compone el Almacenamiento? 
Repositorio de almacenamiento de información para que este disponible cada que sea necesario:
1. Almacenamiento por objetos: Divide los datos en partes distribuidas en el hardware. Cada unidad se llama objeto. (archivos, imágenes, archivos estáticos. No es para instalación de aplicaciones)
2. Almacenamiento por Archivos: Los datos son guardados como una pieza de información dentro de una carpeta. (Almacenamiento que debe ser compartido por múltiples servidores)
3. Almacenamiento por Bloque: Divide la información en bloques. Tiene un identificador único. Permite que se coloquen los datos más pequeños donde sea más conveniente. (Disco duro del servidor virtual en la nube)