Se levanto problemas de ciberseguridad y como era una tecnología deprecada se decidió realizar una aplicación web de el formulario de centro de ayuda.
1. Tipo de solicitud:
- Tiene que estar seleccionado por que es obligatorio
- Opciones que tiene consultas, felicitaciones, sugerencias y reclamos
- Reclamos despliega una Card con información adicional para este caso
1. Nombre completo:
- Se valida el largo mínimo y el máximo
- Se valida Inyección de SQL y de scripts
2. RUT:
- Valida formato RUT (XX.XXX.XXX-X)
- Elimina caracteres no numéricos excepto 'k'/'K'
- Formato automático con puntos y guion
3. Teléfono:
- Valida el largo de numero
- Elimina caracteres excepto números
- Aunque no es requerido
4. Correo electrónico:
- Valida Caracteres no permitidos
- Valida Inyección de SQL y de scripts
- Valida el correcto formato de Correo
5. Descripción:
- Valida el largo máximo
- Valida Inyección de SQL y de scripts
6. El botón de envió:
- Cuando los campos requeridos estén completos se activa
- Envía a la pagina de completado