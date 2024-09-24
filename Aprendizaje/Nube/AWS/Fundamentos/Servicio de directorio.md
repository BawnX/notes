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

Un **directorio** es una base de datos que contiene información de inicio de sesión de todos los usuarios de una red y puede implementar políticas de seguridad.

Dado que Windows es el sistema operativo más usado a nivel mundial, Microsoft lanzó **Active Directory**. Este servicio permite que las empresas gestionen los inicios de sesión de sus empleados.

# **AWS Directory Service**

Es una oferta de servicio administrado de AWS que posibilita que sus recursos utilicen **Active Directory** y ofrecen:

- Un directorio activo administrado sin tener que ejecutar servidores manualmente
- La opción de directorio activo simple
- El conector AD que brinda a usuarios inicio de sesión en aplicaciones de AWS con sus credenciales
- Un Servicio distribuido con error automático que funciona si hay fallas en los servidores
- El AWS Directory Service es compatible con otros servicios de AWS
# Precios de AWS Directory Service

En este caso AWS menciona que

> Con AWS Directory Service, solo pagará por el tipo y el tamaño de directorio administrado que use. No existe ningún compromiso inicial ni tarifa mínima. Puede eliminar el directorio administrado en cualquier momento.

En caso de querer compartir el directorio con otros servicios como **Microsoft Active Directory** la cosa cambia porque se cobra por cada hora que usemos el servicio:

> Cargo de AWS Directory Service para Microsoft Active Directory 0 USD
> 24 horas x 30 días = 720 horas por controlador de dominio 2 controladores de dominio por directorio administrado (el mínimo) 720 horas x 2 controladores de dominio en total = 1440 horas de controlador de dominio en total 1440 horas en total – 1500 horas de la prueba gratuita limitada = 0 horas de controlador de dominio facturables Al cabo de 30 días o 1500 horas de prueba gratuita (lo que suceda primero), AWS le facturará por directorio administrado de acuerdo con la tarifa por hora.
> Resumen de los cargos tras los primeros 30 días
> Su factura por los primeros 30 días de uso después de que se acabe la prueba gratuita es de 288,00 USD.
> Cargo de AWS Directory Service para Microsoft Active Directory 288,00 USD
> 24 horas x 30 días = 720 horas por controlador de dominio 2 controladores de dominio por directorio administrado (el mínimo) 720 horas x 2 controladores de dominio en total = 1440 horas de controlador de dominio en total 1440 horas en total x 0,20 USD por hora de controlador de dominio = 288,00 USD