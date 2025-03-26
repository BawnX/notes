
# Terminos 
- Freezing: Cuando se paran los despliegues a fin de mes por recursos
# Consideración Commit
1. A partir de la última rama en producción los desarrolladores deben crear una rama con el siguiente formato: **CODIGO-HU_responsable_Descripción-HU**  
  Ejemplo: CELTP-8095_rschneid_Mejorar-Mensaje-Comprobante-web  
2. **Se debe registrar en la HU la rama que se creó**. Esto por si alguno no está, poder sacar el nombre de la rama desde ahí.
3. La rama que contiene el nuevo desarrollo debe quedar operativa en cuanto a ejecución, pruebas unitarias y generación de binarios.  
4. Como célula nos reuniremos para determinar que desarrollos se pasarán a QA.  
5. **Se debe realizar el merge de cada rama con la rama principal**. Para esto se reunirá desarrollador y LT con el objetivo de resolver conflictos.  
6. Una vez que todos los desarrollos se encuentren en la rama principal, **se debe ejecutar pruebas unitarias (npm run test), generar los binarios (npm run build)** y corregir lo necesario.  
7. **Desplegar la nueva versión en ambiente QA**.  
8. Se debe certificar las HU por parte de QA.  
9. Si la mejora se aprueba por parte de QA **se debe eliminar, por parte del desarrollador, la rama creada**.  
10. Una vez cerrado el PaP **el LT debe revisar el repositorio en busca de ramas que no hayan sido eliminadas y se deben eliminar**.