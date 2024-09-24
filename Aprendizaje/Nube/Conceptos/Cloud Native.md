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
# **CLOUD NATIVE** 
Construir y ejecutar una aplicación tomando todas las ventajas de Cloud Computing. La aplicación está diseñada para utilizar la escalabilidad, elasticidad, seguridad y flexibilidad del proveedor de servicios Cloud. **CLOUD NATIVE vs. APP TRADICIONALES**
## 1. SISTEMA OPERATIVO
En CLOUD NATIVE el sistema operativo pasa a un segundo plano. Ej: desplegamos la APP en SERVERLESS (la responsabilidad pasa a el Cloud Provider). En ON-PREMISES tenemos dependencia del sistema operativo (Windows Server, Linux, Redhat, etc).
## 2. DESARROLLO
ON-PREMISES (Waterfall development). CLOUD NATIVE (Continuous delivery) pensamos la aplicación para que sea automatizada: su despliegue, su servicios, sus nuevas features, etc. Esto nos da mucha AGILIDAD.
## 3. ESCALABILIDAD
ON-PREMISES (manual) ampliamos los recursos en el datacenter. CLOUD NATIVE (automática) utilizando serverless, contenedores, etc.
## 4. CAPACIDAD
ON-PREMISES (limitada), sobre aprovisionada(compre 10 servidores y estoy usando 2). CLOUD NATIVE (muy grande) el consumo y el costo es sobre lo utilizando.
## 5. INMUTABILIDAD y PREDECIBLE
CLOUD NATIVE es inmutable porque es elástica ante picos de demanda y si tengo un error fácilmente puedo desplegar el servicio por completo. El ON-PREMISES no tiene esa ventaja.

# **CLOUD NATIVE COMPUTING FOUNDATION (CNCF)**
Es una fundación de software open-source que promueve la adopción de Cloud Native Computing. Algunos proyectos (que podemos usar en CLOUD NATIVE): ARGO: se utiliza para hacer despliegue de imágenes en Cluster de Kubernetes  
ETCD y KUBERNETES son vitales para desplegar cualquier aplicación cotenedrizada y orquestarla.  
FLUENTD y PROMETHEUS para toda la parte de observabilidad, monitoreo, trazas. PROMETHEUS se utiliza para las DB de series de tiempo. HELM: nos ayuda a desplegar y automatizar despliegues de aplicaciones dentro de KUBERNETES  
## **BENEFICIOS de una APLICACIÓN CLOUD NATIVE**
1. INDEPENDENCIA: cada aplicación es totalmente independiente de las otras.
2. RESILIENCIA: Puede soportar una caída de infraestructura.
3. ESTANDARIZACIÓN: Para interoperabilidad (con otros proveedores o con un on-premises, por ejemplo) y portabilidad (que se pueda mudar a otro cloud provider) de nuestra aplicación, están basadas en OPEN-SOURCE.
4. AGILIDAD: Flexibilidad en sus despliegues y usualmente más pequeñas (de forma RÁPIDA).
5. AUTOMATIZACIÓN: utilización de prácticas DevOps para despliegues. 1) automatizar el despliegue de la infraestructura (TerraForm) pipelines. 2) Pipelines para automatizar el despliegue de la APP en la APPSTORE y PLAY STORE. 3) Automatizar el despliegue de imágenes en las funciones y los contenedores. Pipelines para el backend de nuestra aplicación.
6. 0 Downtime: utilizando las ventajas de la nube la hago siempre operativa a pesar de los despliegues que haga, de las nuevas features y servicios, o de los cambios que haga sobre la misma. Esto marca ventajas en el mercado.