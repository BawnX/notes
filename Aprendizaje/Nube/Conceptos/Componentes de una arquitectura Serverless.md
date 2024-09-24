#Cloud #AWS #Fundamentos

[[Daily/2024-04-15.md|2024-04-15]]

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
# **STREAMS**
es una secuencia de eventos, mensajes o datos que pueden ser procesados una vez ocurren, los cuales pueden ser distribuidos a múltiples consumidores. Abundan en los proyectos donde la palabra clave es “data” o “real-time”. Real-time: es cuando se puede utilizar un evento o una acción que se acabó de generar hace poco. Es streams tiene la capacidad de recibir muchísimos eventos en paralelo (millones) y se los puede enviar a un dashboard para que los grafique y lo pueda ver un equipo de marketing, por ejemplo. De esta manera estoy utilizando un streams para aprovechar al máximo el poder del real time. En los cloud provider estos streams son servicios completamente serverless. El streams tiene que tener la capacidad de recibir esos millones de eventos y enviarselo a un consumidor en tiempo real. 
# **COLAS** 
método para retrasar el trabajo, utilizadas para desacoplar componentes de un sistema. Ejemplo: cola para el cajero del banco. Entonces las COLAS se ubican para no saturar a un componente de la arquitectura. Ejemplo: miles de usuarios piden un certificado a la APP, la COLA en cola estas solicitudes y la aplicación lo va procesando a medida que pueda. De esta manera la APP nunca se cae. 
# **BUCKET** 
estructura donde se puede almacenar una colección de OBJETOS. Estos objetos se pueden consultar. Su costo se basa en la cantidad de solicitudes y espacio utilizado. Almacenamiento por objetos. Un objeto puede ser la foto de cada usuario de la APP. 
# **API** 
es una abreviatura de APPLICATION PROGRAMMING INTERFACES, son mecanismos que permiten a dos componentes de software comunicarse entre sí, mediante un conjunto de definiciones y protocolos. API REST, API HTTPS, API WebSocket, API GraphQL y todos son servicios serveless. La API es la puerta de entrada a nuestra aplicación. 
# **DATASTORE** 
es una base NoSQL creada para proporcionar autoescalamiento, alto rendimiento y facilidad para el desarrollo de aplicaciones. No SQL: llave valor, de memoria, por grafos y documentales.  
# **IDENTITY SERVICES**
servicios en la nube que ayudan a implementar la administración de acceso e identidad de los usuarios a nuestras aplicaciones web o móviles. Servicios para hacer autenticación y autorización. Ejemplo para PlatziWallet: yo puedo registrarme como usuario (autenticación) pero hasta que no registre una tarjeta de crédito no voy a poder realizar un pago (autenticación). 
# **MOTOR DE CONSULTAS** 
motor de consulta SQL que pueden consultar data estructurada, semiestructurada y no estructurada de diferentes fuentes de datos. Ej: PRESTO (Open Source). Query a múltiples fuentes, centralizadas y el costo es por la cantidad de data escaneada. A datos que tengamos en almacenamiento por objetos, a DB no relacionales y relacionales. 
# **BALANCEADORES DE CARGA** (de aplicaciones y de red) 
componente que distribuye el tráfico entre varios destinos, puede ser a nivel de aplicación, red o transporte. Recibe los requests y los distribuye entre las zonas de disponibilidad. El balanceador de aplicaciones es el que va ser nuestro foco, porque va a trabajar en capa 7 del modelo OCI, es decir, va a balancear a nivel de HTTP y HTTPS. El balanceador de red se enfoca en las capas 3 y 4 del modelo OCI, es decir, en balancear tráfico IP, tráfico UDP y tráfico TCP.