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
**Amazon Elastic File System (EFS)** brinda un sistema de archivos elástico, sencillo, sin servidor y práctico basado en **NFS** para las máquinas virtuales de EC2.
[**NFS**](https://www.computerweekly.com/es/definicion/Sistema-de-archivos-de-red-NFS) es un **protocolo de archivos en red que permite acceder a archivos y directorios que no están en tu sistema.** Esto permite que miles de máquinas puedan conectarse a [EFS](https://aws.amazon.com/es/efs/) y procesar los datos que allí se encuentran.
# Características de EFS
EFS es altamente disponible y duradero. **Provee protección contra una interrupción de la zona de disponibilidad,** replicando los archivos en múltiples zonas dentro de una región.
Adicionalmente:
- EFS brinda dos clases de almacenamiento: Standar y Standar IA (para acceso poco frecuente). Puedes implementar políticas para que tus archivos se muevan de Standar a Standar IA después de cierto tiempo.
- Los datos están **encriptados de manera automática.**