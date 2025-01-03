# Extracción de entidades

Se identiican las identidades que se mencionan en un texto. LAs entidades se agrupan en las siguientes categorías:
- Person
- Location
- DateTime
- Organization
- Address
- Email
- URL

## Ejemplo

```json
{
    "kind":"EntityRecognition",
    "parameters":{
        "modelVersion":"latest"
    },
    "analyisInput":{
        "documents":[
            {
                "id":"1",
                "language":"en",
                "text":"Joe went to London on Saturday"
            }
        ]
    }
}
```

## Respuesta:

```json
{
    "kind":"EntityRecognitionResults",
    "results":{
        "documents":[
            {
                "entities":[
                    {
                        "text":"Joe",
                        "category":"Person",
                        "offset":0,
                        "length":3,
                        "confidenceScore":0.62
                    },
                    {
                        "text":"London",
                        "categody":"Location",
                        "offset":12,
                        "length":3,
                        "confidenceScore":0.88
                    },
                    {
                        "text":"Saturday",
                        "category":"DateTime",
                        "subcategory":"Date",
                        "offset":22,
                        "length":8,
                        "confidenceScore":0.8
                    }
                ],
                "id":"1",
                "warnings":[]
            }
        ],
        "errors":[],
        "modelVersion":"2021-01-15"
    }
}
```
