# Evaluación de modelos

La evaluación de los modelos de NER es similar a la evaluación tradicional de modelos de clasificación en machine learning. La evaluación es un paso crítico en el proceso de desarrollo de modelos NER; ya que permite determinar la calidad del modelo y reentrenar si es necesario, con el conocimiento de las deficiencias del modelo y de las necesidades de mejora.

En el portal de Azure Language Studio se pueden visualizar las métricas de evaluación: 

- **Precision (Precisión)**: La proporción de entidades identificadas correctamente en relación con todas las identificaciones de entidad.
- **Recall (Sensibilidad)**: La proporción de entidades identificadas correctamente en relación con el número todal de identidades en el texto que tenían que ser identificadas.
- **F1 Score**: La media armónica de la precisión y la sensibilidad.

## Interpretación

- **Baja presición y baja sensibilidad**: Las identificaciones que el modelo hace no corresponden a las entidades reales. Y de las entidades reales, el modelo no identifica todas.
- **Alta presición y baja sensibilidad**: El hace un buen trabajo seleccionando la clase para la entidad, pero no identifica todas las entidades.
- **Baja presición y alta sensibilidad**: El modelo identifica un alto porcentaje de entidades reales, pero además asigna etiquetas en texto que no son entidades. 


