# Análisis de sentimientos /Opinión

La api de Azure califica un texto como positivo, negativo o neutral. El sentimiento se basa en las puntuaciones de confianza para estas tres clasificaciones.
## Ejemplo de solicitud
```json
{
    "kind":"SentimentAnalysis",
    "parameters":{
        "modelVersion":"latest"
    },
    "analysisInput":{
        "documents":[
            {
                "id":"1",
                "language":"en",
                "text":"good morning!"
            }
        ]
    }
}
```

# Ejemplo  de respuesta
```json
{
    "kind":"SentimentAnalysysResult",
    "results":{
        "documents":[
            {
                "id":"1",
                "sentiment":"positive",
                "confidenceScores":{
                    "positive":0.89,
                    "neutral":0.10,
                    "negative":0.01
                },
                "sentences":[
                    {
                        "sentiment":"positive",
                        "confidenceScores":{
                            "positive":0.89,
                            "neutral":0.10,
                            "negative":"0.01"
                        },
                        "offset":0,
                        "length":13,
                        "text": "good morning!"
                    }
                ],
                "warnings":[]
            }
        ],
        "errors":[],
        "modelVersion":"2022-11-01"
    }
}
```
