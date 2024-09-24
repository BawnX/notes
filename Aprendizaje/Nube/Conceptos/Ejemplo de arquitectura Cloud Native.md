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
Características Arquitectura: Altamente disponible (AZ): 2 zonas de disponibilidad.

# CAPA DE CONECTIVIDAD
Para el on-premises, las instalaciones de la empresa o una capa de networking. A través de un VPN o una conexión dedicada que nos ofrece Cloud P.
# ZONA PRIVADA 
Donde corre el backend de nuestra aplicación. No va a estar expuesta a internet. Nosotros exponemos nuestros servicios, pero nuestra aplicación, los contenedores, las funciones quedan en esta zona privada.
# ZONA PÚBLICA 
servicios que deben estar expuestos hacia internet. Reciben los requests directamente de los usuarios y se comunican con la capa privada donde está el backend. 
## DNS
nombre de dominio (platziwallet com). Le agregamos las reglas de enrutamiento. Se pueden crear a nivel de los DNS opciones de redireccionamiento (basados en el nombre de dominio).  
## CDN (content delivery network ) 
expone el servicio de forma global a través del uso de ubicaciones de borde. Ubicaciones de borde son datacenter pequeños distribuidos por el mundo sobre los cuales puedo poner el contenido estático o dinámico de la aplicación. Esto ayuda a que la experiencia de usuario sea mucho mejor. WAT + CERTIFICADO ( seguridad). Va a ver usuarios que van a estudiar cómo toman ventaja para hacer fraude. Web Application Firework + Certificado de seguridad para agregarle reglas de seguridad a nuestra aplicación. De esta manera protegemos nuestra aplicación de ataques de denegación de servicios, sql injections, ataques de script 
## API GATEWAY 
recibe toda la información se la manda al BALANCEADOR de aplicaciones. Detrás del balanceador podemos tener nuestro backend corriendo en Kubernetes. Este clúster de Kubernetes donde está corriendo PlatziWallet y donde están los microservicios de pagos, cobro, recarga, login, biometría, etc. Estos tienen una capa de almacenamiento (objetos, bloques y archivos).  
## DESPLIEGUE 
para desplegar nuestro backend tenemos: Kubernetes, argo y helm

![[Pasted image 20240410132817.png]]