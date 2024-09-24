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

AWS describe su capacidad de cómputo como **“cómputo para cualquier carga de trabajo”. Cómputo se refiere a usar una computadora para procesamiento,** ya sea sumar dos números o alojar un sitio web. Entre los servicios de cómputo se encuentran:

# Instancias o máquinas virtuales

Una **máquina virtual** es un _software_ que simula un sistema operativo, y que puede ejecutar programas dentro de dicho sistema como si fuera una computadora real. Los servicios de máquinas virtuales (o instancias) en AWS son:

- **Amazon EC2**: máquinas virtuales seguras y redimensionables.
- **Amazon EC2 Spot**: cargas de trabajo tolerante a fallas, por hasta el 90% del precio normal (nota: Amazon puede reclamar estas instancias en cualquier momento con solo dos minutos de anticipación).
- **Amazon EC2 AutoScaling**: agrega o elimina automáticamente la capacidad informática para satisfacer tus necesidades bajo demanda.
- **Amazon EC2 LightSail**: plataforma en la nube fácil de usar para crear una aplicación o un sitio web.

# Contenedores
Un **contenedor** es una unidad de software que empaca un _software_ en específico junto con sus dependencias. Se diferencian de las máquinas virtuales en que estas virtualizan el _hardware,_ mientras que los contenedores [virtualizan el sistema operativo](https://cloud.google.com/learn/what-are-containers). Los servicios de contenedores de AWS son:

- **Amazon Elastic Container Services (ECS)**: servicio para correr contenedores confiables y escalables.
- **Amazon Elastic Container Registry (ECR)**: servicio para almacenar, administrar e implementar [imágenes de contenedores](https://platzi.com/clases/2066-docker/32856-conceptos-fundamentales-de-docker-imagenes/).
- **Amazon Elastic Kubernetes Service (EKS)**: servicio de [Kubernetes](https://platzi.com/cursos/k8s/) administrado por AWS.

# _Serverless_

La computación **_serverless_** se refiere a que **la responsabilidad de administrar servidores o máquinas virtuales se le delega al proveedor de nube,** por lo que sólo debemos precuparnos por el código de nuestras aplicaciones. **Amazon Lambda** nos permite ejecutar piezas de código sin servidores.

# Servicios de borde (_Edge_)

El [_Edge Computing_](https://www.xataka.com/internet-of-things/edge-computing-que-es-y-por-que-hay-gente-que-piensa-que-es-el-futuro) se refiere al **cómputo y procesamiento de datos en una ubicación cercana a la necesaria para el negocio.** Los servicios de borde o _edge_ computing de AWS son:

- **Amazon Outposts**: permite ejecutar los servicios de AWS en nuestros propios servidores en lugar de Amazon.
- **Amazon Snow Family**: es una familia de dispositivos desde un disco duro portátil hasta un semi-remolque completo lleno de discos de almacenamiento. Estos dispositivos te permiten cargar archivos en ellos, para luego ser enviados a Amazon y cargados en sus servidores.
- **AWS Wavelength**: permite acceder a los servicios AWS desde dispositivos 5G sin pasar por Internet.
- **VMWare AWS**: permite migrar cargas de trabajo de VMWare a AWS.
- **AWS Local Zones**: permite ejecutar las aplicaciones más cerca de los usuarios finales, a una menor latencia.
- 