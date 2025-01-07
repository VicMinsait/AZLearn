# Consejos para etiquetado de datos

- Consistencia: Etiquete sus datos de manera consistente a través de todos los documentos para entrenamiento.
- Precisión: etiquete sus entidades sin palabras extra, y asegúrese de que cada palabra esté etiquetada.
- Completitud: Etiquete todas las entidades en un documento. 

# Etiquetado de datos. 

La forma más sencilla de hacer el etiquetado de las entidades en un documento es a través del portal de azure. Language Studio proporciona una interfaz que permite seleccionar texto y asignar etiquetas a entidades.

Al identificar las identidades en un texto, se genera de forma automática un archivo JSON que contiene las entidades y sus etiquetas. Este archivo se puede descargar y reusar (por ejemplo si se desea entrenar un modelo en un proyecto distinto.)

El formato de este JSON es el siguiente: 

```json
{
    "projectFileVersion":"{DATE}",
    "StringIndexType":"Utf16CodeUnit",
    "metadata":{
        "projectKind":"CustomEntityRecognition",
        "storgaeInputContainerName":"{ContainerName}",
        "projectName":"{PROJECT-NAME}",
        "multilingual":false,
        "description":"Project-Description",
        "language":"en-us",
        "settings":{}
    },
    "assets":{
        "projectKind":"CustomEntityRecognition",
        "entities":[
            {
                "category":"Entity1",
            },
            {
                "category":"Entity2"
            }
        ],
        "documents":[
            {
                "location":"{document_location}",
                "language":"en-us",
                "dataset":"{DATASET}",
                "entities":[
                    {
                        {
                            "regionOffset":0,
                            "regionLength":500,
                            "labels":[
                                {
                                    "category":"Entity1",
                                    "offset":25,
                                    "length":10
                                },
                                {
                                    "category":"Entity2",
                                    "offset":120,
                                    "length":8
                                }
                            ]
                        }
                    }
                ]
            },
            {
                "location":"{Document-NAME}",
                "lanuage":"en-us",
                "dataset":"{DATASET}",
                "entities":[
                    {
                        "regionOffset":0,
                        "regionLength":100,
                        "labels":[
                            {
                                "category":"Entity1",
                                "offset":20,
                                "length":5
                            }
                        ]
                    }
                ]
            }
        ]
    }
}
```

De donde:

| Campo | Descipción |
|-------|------------|
| documents | Arreglo de documentos etiquetados |
| location | Path al documento, dentro del contenedor asociado al proyecto |
| language | Lenguaje del documento |
| entities | Arreglo de entidades en el documento |
| regionOffset | La posición (inclusiva) del primer caracter de la entidad |
| regionength | Largo en caracteres de los datos usados para entrenar |
| category | Nombre de la entidad a extraer |
| labels | Arreglo de entidades etiquetadas en los archivos |
| offset | Posición (inclusiva) del primer caracter de la entidad |
| length | largo en caracteres de la entidad |
| dataset | El dataset al cual el documento pertenece |
