# Detección de objetos con Azure Custom Vision

Se conoce como detección de objetos a la tarea de identificar múltiples objetos en una imagen haciendo uso de un modelo de visión de aprendizaje profundo. Generalmente una predicción de detección de objetos tiene dos componentes: 

1. Etiqueta de la clase de cada objeto detectado en una imagen.
2. Coordenadas de la caja delimitadora que rodea a cada objeto detectado.

Para hacer uso de la detección de objetos en [[Azure Custom Vision]], se necesitan los siguientes elementos:

1. Un recurso de entrenamiento de Custom Vision. (Custom Vision de Azure AI (entrenamiento))
2. Un recurso de predicción (Custom vision de Azure AI (predicción))
