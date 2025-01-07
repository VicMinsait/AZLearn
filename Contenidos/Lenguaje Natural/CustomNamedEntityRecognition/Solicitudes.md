# Cómo extraer entidades.

Se puede consumir un modelo ya implementado a través de una API REST, con el siguiente esquema:

```json
{
    "displayName":"string",
    "analysisInput":{
        "documents":[
            {"id":"doc1", "text":"string"},
            {"id":"doc2","text":"string"}
        ]
    },
    "tasks":[
        {
            "kind":"CustomEntityRecognition",
            "taskName":"MyRecognitionTaskName",
            "parameters":{
                "projectName":"MyProject",
                "deploymentName":"MyDeployment"
            }
        }
    ]
}
```
