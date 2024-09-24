#Aprendizaje #Nube
[[2024-04-10]]
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
# **DEFINICIÓN DE SERVERLESS** 
es la idea de que se puede ejecutar una aplicación basada en servidor sin la necesidad de administrar un servidor. Los CLOUD PROVIDER tienen servicios SERVERLESS. El cloud provider administra el sistema operativo (parcheo, administración, escalabilidad del SO) y el usuario se enfoca en su aplicación. El cloud provider le da al usuario una FUNCIÓN y un CONTENEDOR SERVERLESS. El usuario pone la aplicación en el CONTENEDOR en esa FUNCIÓN.  
# **RETOS de SERVERLESS**
1. ESCALABILIDAD: es muy grande pero está limitada por las cuotas y los límites que pone el cloud provider. Por ejemplo la FUNCIÓN puede tener un límite de concurrencia (ej: 1000 ejecuciones concurrentes por segundo). Estos límites se pueden ampliar a través de una solicitud al cloud provider por medio de un ticket de ampliación de límites. El costo tiene que ver con estos límites.
2. SEGURIDAD: el usuario se enfoca en proteger el código que publica en la función (comunicación de cifrado en tránsito). El usuario no se preocupa de la seguridad del servidor.
3. FIABILIDAD: El cloud provider se compromete con una niveles de disponibilidad por arriba del 99 % (los servicios que tienen que ver con la fiabilidad y alta disponibilidad tienen un SLA muy alto).
4. PAGO POR USO: por el tiempo de ejecución y la cantidad de memoria que uso para una ejecución. Ej: una FUNCIÓN se demora 200 milisegundos en tomar una imagen y convertirla en miniatura. El precio se calcula por ejecución, por consumo, cantidad de peticiones, tiempo de ejecución y cantidad de tráfico.
5. AHORRO de TIEMPO y DINERO: ej: on-premises a serverless. No hay ocupación en administrar o instalar servidores. MEJORA la PRODUCTIVIDAD del DESARROLLADOR: porque los entornos actualmente en nube, los servicios, la forma de testearlos localmente, la forma de automatizar su despliegue y de probarlos es muy fácil. La agilidad para desplegar un servicio por medio de una función, teniendo el código, va a ser muy rápida (10 o 15 minutos).
6. COLD START (tiempo de inicio frío): tiempo para que una FUNCIÓN se “despierte”. Hay que esperar unos 2 o 3 segundos en su primera ejecución. Esto puede afectar a algunas arquitecturas cuando no se tolera ese tiempo de latencia.
7. TIEMPO de CÓMPUTO: Ejemplo. Hay FUNCIONES que su tiempo máximo de vida es 15 minutos y necesitamos un tiempo de ejecución de 30 minutos. FUNCIÓN limitada por un timeout.
8. CONECTIVIDAD: Ejemplo. Consumo de direcciones IP que hace una función dentro de una capa de red. Si es alto hay que evaluar la utilidad que tiene esa función dentro de la capa. Pues es aconsejable que esa función no se ubique dentro de una VPC o una Virtual Private Cloud dentro de la red. Sino que se ejecute fuera de ella para tener más flexibilidad.
9. VENDOR LOCK-IN: si queremos migrar una aplicación de AZURE a AWS lo más probable es que la tengamos que hacer de nuevo.