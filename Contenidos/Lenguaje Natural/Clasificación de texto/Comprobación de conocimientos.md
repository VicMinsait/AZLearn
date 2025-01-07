1. Desea entrenar un modelo para clasificar resumentes de libros por su género, y algunos de sis libros favoritos son de "misterio y thriller". Qué tipo de proyecto debería construir?

- [ ] Un proyecto de clasificación de una sola etiqueta
- [ ] Un proyecto de clasificación de varias etiquetas
    - [X] Correcto. Use un proyecto de clasificación múltiple para etiquetar libros en múltiples géneros.
- [ ] Un proyecto de clasificación de etiquetas variadas

2. Recibió una notificación de que la tarea de entrenamiento está completa. ¿Cuál es el sigiuente paso?

- [ ] Etiquetar más datos.
- [ ] Desplegar el modelo
- [X] Revisar los detalles del modelo
    - [X] Correcto. REvise los resultados del modelo para determiar cómo se desempeñó. La distribución de clasificaciones, y dónde necesita ser mejorado.

3. Quiere emitir una solicitud de clasificación via API. ¿Cómo obtiene los resultados de la clasificación?
- [ ] El resultado está en la respuesta de la solicitud.
- [ ] Llamar un endpoint con el nombre del deployment para obtener la clasificación más reciente.
- [X] Llamar a la url provista en el header de la respuesta.
    - [X] La respuesta es correcta. El valor del header en la clave "operation-location" se puede usar para recuperar los resultados de una solicitud de clasificación.
