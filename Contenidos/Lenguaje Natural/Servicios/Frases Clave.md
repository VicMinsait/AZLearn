# Extracción de frases clave

Es el proceso de evaluar el texto de uno o varios documentos e identificar los puntos principales. 

## Límites de la api

La api de Azure Language para extracción de frases clave:

- Acepta hasta 5120 caracteres por documento. 
- Permite enviar uno o varios documentos para su análisis.

# Ejemplo de solicitud 

```json
{
    "kind":"KeyPhraseExtraction",
    "parameters":{
        "modelVersion":"latest"
    },
    "analysisInput":{
        "documents":[
            {
                "id":"1",
                "language":"en",
                "text":"You must be the change you wich to see in the world."
            },
            {
                "id":"2",
                "language":"en",
                "text":"The journey of a thousand miles begins with a single step."
            }
        ]
    }
}
```

# Ejemplo de respuesta en json
```json
{
    "kind":"KeyPhraseExtractionResults",
    "results":{
        "documents":[
            {
                "id":"1",
                "keyPhrases":[
                    "change",
                    "world"
                ],
                "warnings":[]
            },
            {
                "id":"2",
                "keyPhrases":[
                    "miles","single step","journey"
                ],
                "warnings":[]
            }
        ],
        "errors":[],
        "modelVersion":"2021-06-01"
    }
}
```
