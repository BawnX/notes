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
**AWS Storage Gateway nos brinda acceso a almacenamiento en la nube prácticamente ilimitado desde nuestra propia infraestructura**.
Storage Gateway se compone de tres puertas de acceso diferentes:
# File Gateway
**File Gateway** provee interfaces [SMB](https://es.wikipedia.org/wiki/Server_Message_Block) y NFS para amazon S3, tanto en Windows como en Linux. Gracias a [File Gateway](https://aws.amazon.com/es/storagegateway/file/), en ambos sistemas operativos veremos un sistema de archivos tal cual como si fuera un disco montado en nuestros computadores, los cuales escriben archivos al sistema, y **File Gateway se encarga de guardarlos en S3**.
Gracias a esto **podemos guardar archivos a S3 como si se tratara de guardar archivos locales.** Los archivos S3 luego pueden ser usados por cualquier servicio de AWS.
# Tape Gateway
Supón que tienes copias de seguridad en cintas físicas. **Tape Gateway te permite migrar copias de seguridad a una bibliteca de cintas virtuales en AWS.** Tape Gateway es compatible con los principales _software_ de respaldo.
Los contenidos de tus cintas se guardan en S3, lo que te permite implementar **S3 Glacier** y **S3 Glacier Deep Archive** para guardar tus copias de seguridad a largo plazo. Una vez que implementas [Tape Gateway](https://aws.amazon.com/es/storagegateway/vtl/), puedes olvidarte de los costos relacionados a mantener las cintas físicas.
# Volume Gateway
[**Volume Gateway**](https://aws.amazon.com/es/storagegateway/volume/#:~:text=Volume%20Gateway%20brinda%20vol%C3%BAmenes%20de,cach%C3%A9%20como%20en%20modo%20almacenado.) otorga **almacenamiento en bloque** con protocolo [iSCSI](https://community.fs.com/es/blog/iscsi-storage-basics-plan-iscsi-san.html#:~:text=el%20almacenamiento%20iSCSI%3F-,iSCSI%20es%20un%20protocolo%20de%20red%20de%20%C3%A1rea%20de%20almacenamiento,trav%C3%A9s%20de%20redes%20TCP%2FIP.), respaldado en la nube. Almacena datos en S3 de acuerdo a dos modos:
- **Modo caché**: almacena los datos principales en S3, mientras que los datos de acceso frecuente se guardan localmente y en caché.
- **Modo almacenado**: todos los datos se guardan localmente, mientras que se hace una copia de seguridad de manera asíncrona en S3.
![[Pasted image 20240416124201.png]]