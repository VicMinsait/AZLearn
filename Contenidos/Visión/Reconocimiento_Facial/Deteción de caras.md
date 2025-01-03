# Detección de caras con el servicio Visión de Azure AI

Para detectar y analizar caras con el servicio visión de Azure AI Se hace una solicitud (mediante SDK o REST) especificando **_people_** como una de las características a detectar.

# Uso de Face

El servicio Face puede detectar: 

* **Caras** (ubicación)
* **Análisis de rasgos faciales**:
    - Posición de la cabeza (inclinada, ladeada y girada en 3D)
    - Gafas
    - Desenfoque
    - Exposición (baja, normal, alta)
    - Ruido visual
    - Oclusión (cubierta por un objeto)
    - Accesorios (sombrero, gafas, etc.)
    - Calidad de reconocimeinteo (baja, media, alta)

* **Ubicación del punto de referencia facial**: Coordenadas de los punbtos de referencia clave en relación con los rasgos faciales.
* **Comparación de caras**: Comparación de caras por similitud.
* **Reconocimiento facial**: Identificación de caras en un grupo de personas dadas.

Se puede aprovisionar **Face** como un recurso único o usar la api de Face en un recurso de varios servicios *Servicios de Azure AI*.

SE debe solicitar la [directiva de acceso limitado](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-limited-access) y obtener aprobación
