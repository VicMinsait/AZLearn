# Ejemplos de solicitudes a los endpoints de clasificación de texto
## CustomSingleLabelClassification

```json
{
    "projectFileVersion":"<API-VERSION>",
    "stringIndexType":"Utf16CodeUnit",
    "metadata": {
        "projectName":"<PROJECT-NAME>",
        "storageInputContainerName":"<CONTAINER-NAME>",
        "projectKind":"CustomSingleLabelClassification",
        "description": "Trying out  custom multilabel text classification",
        "language":"en",
        "multilingual":true,
        "settings":{}
    },
    "assets":{
        "projectKind":"customSingleLabelClassification",
        "classes":[
            {"category":"Class1"},
            {"category":"Class2"},
            {"category":"Class3"}
        ],
        "documents":[
            {
                "location":"<DOCUMENT-NAME>",
                "language":"en",
                "dataset":"<DATASET-NAME>",
                "class":{
                    "category":"Class1"
                }
            }
        ]
    }
}
```
