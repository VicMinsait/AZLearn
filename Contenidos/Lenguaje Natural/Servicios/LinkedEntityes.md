# Extracción de Entidades Ligadas

Para los casos en que una palabra posea varios significados, se hace uso de Linked Entities. Este servicio se usa para eliminar la ambigüedad respecto de entidades con el mismo nombre. Esto se logra a través de una referencia a un artículo de Wikipedia. 


# Ejemplo: 

```json
{
    "kind":"EntityLinking",
    "parameters":{
        "modelVersion":"latest"
    }
    "analysisInput":{
        "documents":[
            {
                "id":"1",
                "language":"en",
                "text":"I saw Venus shining in the sky."
            }
        ]
    }
}
```

# REspuesta

```json
{
    "kind":"EntityLinkingResults",
    "results":{
        "documents":[
            {
                "id":"1",
                "entities":[
                    {
                        "bingID":"some-id",
                        "name":"Venus",
                        "matches":[
                            {
                                "text":"Venus",
                                "offset":6,
                                "length":5,
                                "confidenceScore":0.01
                            }
                        ],
                        "language":"en",
                        "id":"Venus",
                        "url":"https://en.Wikipedia.org/wiki/Venus",
                        "dataSource":"Wikipedia"
                    },
                ],
                "warnings":[],
            }
        ],
        "errors":[],
        "modelVErsion":"latest"
    }
}
```
