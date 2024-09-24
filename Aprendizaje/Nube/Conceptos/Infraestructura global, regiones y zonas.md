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
# INFRAESTRUCTURA GLOBAL
todos los elementos que puede ofrecer el proveedor de servicios de nube distribuido a nivel mundial de Regiones y Zonas.  
Servidores conectados a nivel global para desplegar aplicaciones (internet, última tecnología, hardware, etc). Infraestructura distribuida por todo el planeta tierra (AWS, AZURE, GCP google cloud platform).
# REGIÓN 
Ubicación física donde se agrupan centros de datos. Están distribuidas en todo el mundo para prestar una cobertura Global del proveedor de servicios de nube.  
Criterios para seleccionar una región: LATENCIA (buscar mayor velocidad de respuesta), PRECIO (varía entre países), CATÁLOGO DE SERVICIOS (para el mismo CLOUD PROVIDER puede variar entre regiones).
# ZONA de DISPONIBILIDAD (AZ) 
Es uno o más centros de datos. Con su propia energía, redes y conectividad redundante dentro de una región. Están interconectadas entre ellas con redes de alto ancho de banda y baja latencia. Una REGIÓN puede tener varias ZONAS de DISPONIBILIDAD (AZ). Las AZ están completamente independientes y aisladas entre ellas. Si se cae una zona no tiene que incidir en las otras.  
Balanceador de cargas: distribuye el tráfico de requests entre AZ dentro de una misma región. El diseño de la APP tiene que ser tal que pueda correr en múltiples zonas. Multizona. Por el balanceador de cargas. De esta manera si se cae una AZ no se va a caer la APP. Con esta característica la APP tiene ALTA DISPONIBILIDAD.