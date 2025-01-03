# Descripción de "Question Answering"

SE hace uso de una base de conocmieento (_knowledge base_) para responder a preguntas de forma automática.

Este servicio puede ser útil en los siguientes escenarios: 
- Sitios web que contienen documentación de preguntas frecuentes.
- Archivos que contienen teto estructurado como folletos o guías de usuario.
- Pares de preguntas y respuestas de _charla_ integrados que encapsulan intercambios conversacionales comunes.

# Qué es Question Answering y cómo es distinto a Language Understanding?


Los dos servicios son similares, pero tienen diferencias clave:

| | Question Answering | Language Understanging | 
| --- | --- | --- |
| Caso de uso | Un usuario hace una pregunta esperando una respuesta | Un usuario hace una petición, esperando una acción |
| Procesamiento | Este servicio hace uso de Language Understanding para identificar la respuesta (predefinida) en la base de conocimiento | Se interpreta la petición y se identifica una acción |
| Respuesta | Es una contestación estática a la pregunta conocida | La respuesta indica la intención más probable y las entidades referenciadas. | 
| Lógica en el cliente | Típicamente este cliente presenta la respuesta al susuario | La aplicación cliente responde en consecuencia basandose en la intención y las entidades detectadas |



