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
Las bases de datos son **colecciones estructuradas de datos.** Almacenan datos electrónicamente, y se acceden a ellos desde un sistema informático. **AWS cuenta con más de quince motores de bases de datos** diferentes, seguros y altamente disponibles.

# Bases de datos relacionales

Los servicios de [bases de datos relacionales](https://ayudaleyprotecciondatos.es/bases-de-datos/relacional/) en AWS son:
- **Amazon Aurora**: base de datos relacional compatible con [MySQL](https://platzi.com/cursos/sql-mysql/) y [PostgreSQL](https://platzi.com/cursos/postgresql/) creada para la nube.
- **Amazon Relational Database Service (Amazon RDS)**: servicio de bases de datos relacionales administrado para MySQL, PostgreSQL, MariaDB, Oracle BYOL o SQL Server. Facilita la configuración, el uso y el escalado de varios motores de bases de datos.
- **Amazon Redshift**: ideal para analítica. Usa SQL para analizar datos estructurados y semiestructurados en almacenamientos de datos, bases de datos operativas y lagos de datos, con _hardware_ y _machine learning_ diseñados por AWS para ofrecer rendimiento al mejor precio a cualquier escala. A propósito, Platzi tiene un curso de [Redshift](https://platzi.com/cursos/redshift-big-data/)
# Bases de datos clave-valor
**Amazon DynamoDB** es una base de datos de documentos y valores clave que ofrece un rendimiento de milisegundos de un solo dígito a cualquier escala. **Está dirigida a aplicaciones de web de alto tráfico, sistemas de comercio electrónico y aplicaciones de juego.**
# Bases de datos en memoria
**Amazon ElastiCache** es un servicio de [almacenamiento de caché en memoria](https://aws.amazon.com/es/caching/?nc1=h_ls) completamente administrado que admite casos de uso flexibles y en tiempo real. Se usa para almacenar en caché administración de sesiones, tablas de clasificación de juegos y aplicaciones Geo-Espaciales. En ElastiCache encontramos **ElastiCache para Memcached** y **ElastiCache para Redis**.
# Bases de datos basadas en documentos
**Amazon DocumentDB** es un servicio de base de datos de larga duración, de alta disponibilidad, rápida, escalable y completamente administrado para operar cargas de trabajo de [MongoDB](https://platzi.com/cursos/mongodb/) esenciales. Entre sus casos de uso se encuentra la gestión de contenidos, catálogos y perfiles de usuario.