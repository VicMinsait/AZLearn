# Skills/Aptitudes/Capacidades personalizadas.

El servicvio de Azure AI ofrece capacidades/aptitudes/Skills predeterminadas para enriquecer los índices de búsqueda. Estas aptitudes son comunes, generales, y son limitadas. Si se desean generar aptitudes que atiendan las necesidades específicas de datasets específicos, se pueden crear skills personalizadas con Azure AI

## Modus integrandi;

En general la forma de integrar aptitudes personalizadas, es la siguiente;

1. Establecer un dataset para crear un índice.
2. Crear un recurso de búsqueda (Azure Search)
3. crear recursos cognitivos (servicios de Azure) que se integrarán al skillset
4. Crar funciones (Con Azure Functions, Azure Function App) para alinear esquemas de entrada y salida entre los recursos y los skillsets
5. Integrar Azure functions app en el pipeline de enriquecimiento.

# requisitos que se deben cumplor al integrar

Los reuisitos que se deben cumplir son los siguients:

1. La Skill personalizada debe adoptar los esquemas esperados para entrada y salida:
2. Especificar el URI del punto de conexión de la API web. 
3. Establecer un contexto: Especificar la jerarquía y el orden en el cual se debe llamar la skill en el pipeline de enriquecimiento
4. asignar valores de entrada.
5. Asignar en la salida en un campo nuevo su resultado.


## Esquema de entrada de datos
El esquema de entrada contiene un **registro**(recordID) para cada documento que se va a procesar. Cada documento tiene un identificador único y una ***carga de datos*** (data) con una o varias entradas:
```json
{
    "values":[
        {
            "recordId":"<unique_identifier>",
            "data":{
                "<input1_name>":"<input1_value>",
                "<input2_name>":"<input2_value>",
                "...":"..."
            }
        },
        {
            "recodId":"<unique_identifiewr_2",
            "data":{
                "<input1_name>":"<input1_value>",
                "...":"..."
            }
        }
    ]
}
```

## ESquema de salida

El esquema de salida refleja el esquema de entrada.:

```json
{
    "values":[
        {
            "recordId":"<unique_identifier_from_input>",
            "data":{
                "<output1_name>":"<output1_value>"
            },
            "errors":[],
            "warnings":[]
        }
    ]
}
```
