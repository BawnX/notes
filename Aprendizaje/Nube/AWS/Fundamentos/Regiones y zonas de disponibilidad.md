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
La infraestructura de AWS está compuesta por **regiones**, **zonas de disponibilidad**, **data centers** y puntos de presencia. Además, se distribuye en diferentes regiones alrededor del mundo. Algunas de ellas son Ohio, Oregon, Norte de California, e incluso lugares exclusivos del gobierno de EE. UU. como GovCloud Este.

Si quieres conocer una lista completa con más sitios, puedes visitar esta [página de AWS](https://aws.amazon.com/es/about-aws/global-infrastructure/?p=ngi&loc=0).

## Cómo escoger una región de AWS

Podemos escoger la región de nuestra aplicación basada en distintos aspectos que mencionaremos a continuación.

**Por ejemplo:**

- El cumplimiento de los requisitos legales y de gobernanza de datos, pues los datos nunca abandonan una región sin su permiso explícito
    
- La proximidad con los clientes porque lanzan en una región cercana en donde estén para reducir latencia. Puedes revisar esta característica desde tu ubicación a cada región en [cloudping.info](https://www.cloudping.info/).
    
- Los servicios disponibles dentro de una región debido a que muchos no funcionan en todas partes. Algunos servicios globales o regionales son…
    
    - **Globales**
        - IAM
        - Route 53
        - Cloudfront
        - WAF
    - **Regionales**
        - EC2
        - Beanstalk
        - Lambda
        - Rekognition

Los precios varían de región a región y son transparentes en la página de precios del servicio

## Zonas de disponibilidad

Una zona de disponibilidad es un grupo de _data centers_ donde cada uno está lleno de servidores. Estos _data centers_ poseen energía, redes y conectividad redundante, están separados entre sí, conectados con un gran ancho de banda y redes de latencia ultra baja.

## Modelo de responsabilidad compartida

Ahora es crucial determinar las responsabilidades de AWS y del cliente dentro del servicio tecnológico que ofrece la compañía.

**AWS se hace responsable de:**

- Hardware y la infraestructura global
- Regiones
- Zonas de disponibilidad
- Ubicaciones de AWS Edge / puntos de presencia
- Software
- Cómputo
- Almacenamiento
- Bases de datos
- Redes

**El cliente se responsabiliza de:**

- Actualizaciones de S.O.
- Protección de los datos que se almacenan
- Manejo de aplicaciones
- Accesos
- Administración de usuarios y grupos

![[Pasted image 20240415144943.png]]
