1. Ha entrenado un modelo de NER y detecta que no está reconociendo sus entidades. ¿Cuál es la métrica que probablemente tenga un valor bajo?
- [ ] Precisión
- [X] Recall
    - [X] Correcto. La Sensibilidad (recall) Indica qué tan bien el modelo extrae entidades, independientemente de qué entidad es.
- [ ] F1-Score

2. Acaba de terminar de etiquetar sus datos. ¿Cómo y dónde se encuentra almacenado el archivo para entrenar su modelo?
- [X] En un archivo JSON en el contenedor de la cuenta de almacenamiento (Storage Account) asociada al proyecto.
    - [X] Correcto. El archivo JSON se encuentra en el contenedor al mismo nivel que su conjunto de datos, para ser usado en el proceso de entrenamiento.
- [ ] En un archivo XML en mi folder local.
- [ ] En un archivo YAML, disponible desde cualquier lugar de mi suscripción de AZURE.

3. Entrenó un modelo con una sola fuente de documentos, a pesar de que la extracción real proviene de múltiples fuentes. ¿Qué métrica de calidad de datos debe mejorar?
- [ ] Distribución
- [ ] Precisión.
- [X] Diversidad.
    - [X] Correcto. La diversidad de los datos es importante para que el modelo pueda generalizar y reconocer entidades en diferentes contextos.
