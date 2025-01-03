# Detección de idioma en Azure Language Services

Existe una API para envío texto y recepción de idioma detectado.
Los usos que sugiere Microsoft son:
- Análisis en almacenes de contenido en lenguajes arbitrarios.
- Bot de chat: detección del lenguaje arbitrario del usuario


## Límites de la api: 

- Tamaño del documento: 5,120 caracteres
- Número de documentos por colección (admitidos en la solicitud): 1000

# Formato de entrada de datos:

```json
{
    "kind":"LanguageDetection",
    "parameters":{
        "modelVersion":"latest"
    },
    "analysisInput":{
        "documents":[
            {
                "id":1,
                "text":"Hello world",
                "countryHint":"US"
            },
            {
                "id":2,
                "text":"Bonjour tout le monde"
            }
        ]
    }
}
```

# Formato de respuesta de la api

```json
{
    "kind":"LanguageDetectionResults",
    "results":{
        "documents":[
            {
                "detectedLanguage": {
                    "confidenceScore": 1,
                    "iso6391Name": "en",
                    "name": "English"
                },
                "id":1,
                "warnings":[]
            },
            {
                "detectedLanguage": {
                    "confidenceScore":1,
                    "iso6391Name":"fr",
                    "name":"French"
                },
                "id":2,
                "warnings":[]
            }
        ],
        "errors":[],
        "modelVersion":"2022-10-01"
    }
}
```
