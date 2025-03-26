# General
- Considerar utilizar Scream Architecture:
	- https://medium.com/@coffeeandcloud/angular-clean-architecture-approach-fcfe32e983a5
	- https://the-amazing-gentleman-programming-book.vercel.app/es/book/Chapter07_Clean_Architecture
- mover variables a de string a variables de constantes
- Utilizar object con identificadores en vez de switch
- Quitar console logs
- Considerar utilizar formato ErrorOr:
	- https://github.com/amantinband/error-or

# Web App
- Utiliza polifills
- Mandarina(librería interna creo)
## Estilos
- Mover las medidas y colores variables pueden ser globales o por módulos
- Utilizar BEM
- Agrupar por Media Queries (Mixins)
- Utilizar CSS Grid
- Cambiar los tamaños de px por rem y em según corresponda
- Añadir transiciones para los hover y el active
- Reestructurar SCSS
- Considerar realizarlo con CSS
## Estructura
- Agrupar Componentes en una sola carpeta componentes
- Separar por tipo de Contenido si es compartida o es especifica
## Código
- mover todo los string estáticos a una carpeta de constantes
- llevar código  de generación como por ejemplo la fecha a una función genérica
- la carpeta utils tiene mucha replica de el export-pdf recibir parámetros para generar según corresponda y eliminar incensarios
- sacar la lógica de las funciones en los componentes y llevarlo a una carpeta de modelos ya sea como clase o como funciones
- Crear las pruebas unitarias en base a la carpeta de modelos
# Backend
- Reestructurar el proyecto separando controladores de lógica de negocio (idealmente tener algun tipo de handler)
- Separar lógicas por patrón por ejemplo repositories
- Pasar por lo menos a TS
- Quitar loggers y agregarlos por middleware
- Hay funciones de conexión que no están haciendo nada