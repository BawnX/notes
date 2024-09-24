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
**Amazon ElastiCache** es un servicio de almacenamiento en memoria 100% administrado que admite casos de uso flexibles y en tiempo real.
Es una **base de datos en memoria que almacena datos a los que se ha accedido previamente en [memoria caché](https://aws.amazon.com/es/caching/?nc1=h_ls),** para mejorar la rapidez de acceso a estos datos. Consultar datos en _caché_ siempre es más rápido que consultar directamente la base de datos.
Un ejemplo de uso es el de un sitio de noticias, al cual se accede miles de veces al día. Si los artículos se mantienen en una base de datos en memoria, se podrá acceder a estos mucho más rápido.
ElastiCache posee dos motores, [**Redis**](https://redis.io/) y [**Memcached**](https://memcached.org/). Ambos se monitorean a sí mismos continuamente, y pueden ser escalados hacia arriba o abajo en función de la demanda de la aplicación.
# **Casos de uso:**
1. Sitio de noticias: Acelera la velocidad con la que se encuentran los artículos en la base de datos, en lugar de acceder a la base de datos cada vez que un visitante llegue a la pagina, los artículos ya están listos para ser enviados por la memoria cache.
# **Motores:**
1. ElastiCache para Redis.
2. ElastiCache para Memcached.
Ambos proporcionan un rendimiento extremo, están completamente administrados, no se requiere aprovisionamiento de hardware, ni parcheo de software. ElastiCache se monitorea a si mismo constantemente para garantizar que todo este siempre en linea, y que sea escalable. Se puede escalar hacia arriba o hacia abajo, según sea necesario para satisfacer las necesidades fluctuantes de la aplicación.
Permiten mantener sitios web de alto trafico que requieran baja latencia con procesamiento a tiempo real.
Algunas de las empresas mas conocidas que usan ElastiCache de AWS son:

1. Peloton
2. AirBNB
3. Duolingo