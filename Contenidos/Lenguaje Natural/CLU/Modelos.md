# Creación de un modelo (CLU) en Azure

Para hacer uso de un modelo de lenguaje conversacional (CLU) en Azure es necesario seguir el path:

1. Creación de un recurso de Azure Language AI, 
2. Crear un proyecto de lenguaje conversacional (CLU) en Language Studio.
3. Importar datos de entrenamiento.
4. Entrenar el modelo.
5. Desplegar el modelo.
6. Usar el modelo.

Para cada uno de estos pasos es posible usar la API REST o la interfaz de usuario de Azure Language Studio.

Al crear el recurso y con él el endpoint se pueden hacer solicitudes HTTP. 

### Ejemplo de body

```json
{
    "kind":"Conversation",
    "analysisInput":{
        "conversationItem":{
            "id":"1",
            "participantId":"1",
            "text":"Sample text"
        }
    },
    "parameters":{
        "projectName":"{PROJECT-NAME}",
        "deploymentName":"{DEPLOYMENT-NAME}",
        "StringIndexType":"TextElement_V8"
    }
}
```

### Ejemplo de respuesta:

```json
{
    "kind":"ConversationResult",
    "result":{
        "query":"String",
        "prediction":{
            "topIntent":"Intent1",
            "projectKind":"Conversation",
            "intents":[
                {"category":"intent1","confidenceScore":1},
                {"category":"intent2","confidenceScore":0}
            ],
            "entities":[
                {
                    "category":"entity1",
                    "text":"text",
                    "offset":7,
                    "length":4,
                    "confidenceScore":1
                }
            ]
        }
    }
}
```
