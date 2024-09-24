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
**[EC2](https://platzi.com/clases/1323-aws-cloud-practico/12577-que-es-ec2/) permite alquilar máquinas virtuales, llamadas _instancias EC2_.** Puedes elegir diferentes tipos de **EC2** con diferente CPU, RAM y almacenamiento. Hay instancias optimizadas para cómputo, memoria y almacenamiento, [entre otras](https://docs.aws.amazon.com/es_es/AWSEC2/latest/UserGuide/instance-types.html).

En **EC2**, el sistema de pago más común es por hora o por segundo, dependiendo el tipo de instancia. Por ejemplo, para una instancia que cueste $0.1 la hora, puedes pagar, ya sea una instancia por 24 horas o 24 instancias por una hora. En ambos casos pagas lo mismo (24 * 0.10 = $2.4).

# Opciones y precios bajo demanda

Las instancias pueden redimiensionarse. Puedes empezar por una instancia de bajo costo, y si necesitas aumenta su capacidad, apagas la instancia y seleccionas un nuevo tipo de instancia. Cuando enciendas de nuevo la instancia, verás su capacidad aumentada. La siguiente tabla muestra **algunos tipos de instancias.**

| Nombre      | Especificaciones                         | Precio       |
| ----------- | ---------------------------------------- | ------------ |
| t3.nano     | 2 vCPU’s, 0.5 GiB RAM                    | $0,0052/hora |
| t3.xlarge   | 4 vCPU’s, 16 GiB RAM                     | $0,1664/hora |
| c6g.8xlarge | 32 vCPU’s, 64 GiB RAM                    | $1,088/hora  |
| X1e.xlarge  | 128 vCPU’s, 3904 GiB RAM, 2x 1920 GB SSD | $26,688/hora |

# Hosts dedicados

Los hosts dedicados en Amazon Web Services (AWS) son infraestructuras de servidores físicos que ofrecen un nivel exclusivo de recursos computacionales para las cargas de trabajo de los clientes. En lugar de compartir estos servidores con otros usuarios, los hosts dedicados permiten a los clientes tener un control más granular sobre la ubicación y asignación de sus instancias de Amazon EC2. Esto puede ser beneficioso para aplicaciones que requieren una mayor seguridad, cumplimiento normativo o rendimiento constante.

Los hosts dedicados también brindan la flexibilidad de llevar licencias de software existentes a la nube sin incurrir en costos adicionales. Al utilizar hosts dedicados, los principiantes en AWS pueden garantizar una mayor aislación de recursos y una mayor predictibilidad en el rendimiento de sus aplicaciones, al tiempo que aprovechan la escala y la elasticidad de la nube de AWS.