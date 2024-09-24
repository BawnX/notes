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
El almacenamiento de datos en la nube consiste en **subir tus datos a dicha red de servidores, donde se te proporcionan herramientas para que puedas acceder a ellos de diferentes maneras.**
# Tipos de almacenamiento y sus servicios

Podemos utilizar distintos tipos almacenamiento datos, y para estos hay servicios de AWS. Los tipos de almacenamiento son:

- **Basado en archivos**: el más conocido por todos. Archivos organizados por carpetas y subcarpetas (sistema de ficheros). En esta categoría encontramos a [Amazon Elastic File System (EFS)](https://aws.amazon.com/es/efs/) y [Amazon FSx for Windows File Server](https://aws.amazon.com/es/fsx/windows/).
- **Bloque**: los archivos se almacenan en volúmenes por fragmentos de datos de igual tamaño, sin procesar. Este tipo de almacenamiento es utilizado como disco duro de nuestros servidores o máquinas virtuales. En esta categoría está [Amazon Elastic Block Store (EBS)](https://aws.amazon.com/es/ebs/).
- **Objetos**: la información almacenada se almacena como objetos, de manera que cada objeto recibe un identificador único y se almacena en un modelo de memoria plana. Un ejemplo de esto es [Amazon Simple Storage Service (S3)](https://aws.amazon.com/es/s3/).
# Respaldo de datos
**Amazon Backup administra y automatiza de forma centralizada** las copias de seguridad en los servicios de AWS.
# Servicios de transferencia de datos
¿Qué pasa si necesitamos transferir datos de nuestros servidores hacia AWS (o viceversa)? AWS ofrece distintos servicios para la transferencia de datos.
- **AWS Storage Gateway**: un conjunto de servicios de almacenamiento en la [nube híbrida](https://platzi.com/clases/2200-introduccion-azure/38231-tipos-de-nube-publica-privada-e-hibrida/) que brinda acceso en las instalaciones al almacenamiento en la nube.
- **AWS DataSync**: acelera el traslado de datos desde y hacia AWS hasta diez veces más rápido de lo normal.
- **AWS Transfer Family**: escala de forma segura tus transferencias recurrentes de archivos de **Amazon S3** y **Amazon EFS** con los protocolos [FTP](https://www.arsys.es/soporte/hosting-web/ftp/que-es-ftp#:~:text=FTP%20es%20un%20protocolo%20que,directorios%2C%20borrar%20ficheros%2C%20etc.), [SFTP](https://es.wikipedia.org/wiki/SSH_File_Transfer_Protocol) y [FTPS](https://es.wikipedia.org/wiki/FTPS).