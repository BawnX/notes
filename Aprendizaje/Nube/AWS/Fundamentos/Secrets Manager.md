#Cloud #AWS #Fundamentos

[[Daily/2024-04-15.md|2024-04-15]]
**Secrets Manager** es un servicio de AWS que nos ayuda a proteger los datos secretos (contraseñas, claves y tokens) necesarios para acceder a nuestras aplicaciones, servicios y recursos.

También nos permite compartir automáticamente esta información cuando queramos. Además, este servicio evita que tengamos que copiar y pegar los secretos directamente en nuestro código.
Cabe mencionar que el precio por “secreto almacenado” es de 0,40 dolares al mes (Al menos a la fecha de hoy). Ademas de cobrar por cada 10 mil llamadas al API para obtener esos secretos.

Citando textualmente los precios en su sitio web:

> Por dato confidencial al mes
> 0,40 USD por dato confidencial al mes. Una réplica de un dato confidencial se considera un dato confidencial distinto y también se facturará a 0,40 USD por réplica al mes. El precio se prorratea en el caso de los datos confidenciales que se almacenen durante menos de un mes (en función del número de horas).
> Cada 10 000 llamadas a la API
> 0,05 USD cada 10 000 llamadas a la API.