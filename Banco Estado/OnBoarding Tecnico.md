[[Daily/2024-09-23.md|2024-09-23]]
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
# Flujo de requerimiento
![[Pasted image 20240923112444.png]]\
# Stack tecnológico
Tener en cuenta que para el backend se utiliza Logger-bech el cual mediante un xtrackid y
código sesión permite pintar el log y darle un tipo, para la obtención de trazas. Estos logs, se pueden obtener desde Kubernetes pero tienen un tiempo máximo de duración de 7 días. En caso que ya no exista el log en kubernetes, existe la herramienta llamada “Elastic Search”. Esta herramienta almacena toda la información histórica. También se utiliza CloudWatch
- APP: Angular - Node, Nestjs.
- NWM: Angular - Node, Nesjts.
- Autoservicios: Angular - Node.
- NWE: Angular - Node, Nesjts
![[Pasted image 20240923113241.png]]
# Pruebas unitarias.
Se crean pruebas unitarias en Jest y Jasmine con un coverage de 85% además de utilizar SonarQuebe para verificar vulnerabilidad y código duplicado.
En algunos casos es necesario revisar el código con el arquitecto aplicativo cuando se tengan vulnerabilidad por si son falsos positivos
# Pruebas de rendimientos.
Para estas pruebas se utiliza JMeter para ver si es capaz de rendir lo requerido
# KUBERNETES
- Cluster: Conjunto de maquinas llamados nodos, kubernetes distribuye las aplicaciones en estos nodos. Estos nodos pueden ser maquinas virtuales y/o servidores. 
- Deployment: Un Deployment en Kubernetes es un objeto que administra y actualiza automáticamente los Pods 
- Ingress: Gestiona el acceso externo a los servicios del cluster, permite la configuración del balanceo de carga las url del servidor o nombres del host. 
- Egress: Permite la comunicación entre un POD interno de un cluster a otro externo (se utiliza para comunicar las aplicaciones Onpremise hacia AWS. 
- Configmap: Permite configurar las variables de entorno de las aplicaciones backend, (las aplicaciones frontend no utilizan variables de entorno en BECH)
# Tipos de infraestructura
En Banco Estado, existen 3 tipos de infraestructura, AWS, Onpremise, IBM. Cada una se utiliza para distintos canales y recursos, los cuales permiten dar servicio a los clientes.
- On-premises: Se refiere a la infraestructura en Servidores locales, los canales APP, Autoservicio, lo utilizan. Todos los artefactos OnPremises viven en gitlab onpremise, el cual tiene la siguiente url gitlab.banco.bestado.cl 
- AWS: Se refiere a la infraestructura en Servidores de la NUBE, estos servicios se cobran por uso, el canal NWM lo utiliza y dispone de distintos servicios, como lo son el de EC2, S3, cloud functions, etc. Todos los artefactos NUBE viven en gitlab Cloud, tiene como url, gitlabcloud.banco.bestado.cl
- IBM: Se utiliza para todo lo que tiene que ver con el BUS y Mainframe.