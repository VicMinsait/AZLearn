# Uso de una base de conomiento

AL crear una base de conomiento en el portal de Azure, se puede desplegar en un enpoint para su consumo. La forma de consimirla: 

```json
{
    "question":"What do I need to cancel a reservation?",
    "top":2,
    "ScoreThreshold":20,
    "strictFilters":{
        {
            "name":"category",
            "vlaue":"api"
        }
    }
}
```
| Propiedad | Descripción |
|-----------|-------------|
| question | Pregunta que se va a enviar a la base de conocimiento |
| top | Número máximo de respuestas que serán devueltas |
| scoreThreshold | Umbral de puntuación para las respuestas identificadas |
| strictFilters | Restricciones para que las respuestas contengan sólo la metadata especificada |

## respuestas
La respuesta incluye las preguntas más cercanas identificadas, junto con la respuesta.

```json
{
    "answers":[
        {
            "score":27.74,
            "id":20,
            "answer":"Call us on 555-555-5555 to cancel a reservation.",
            "questions":[
                "How can I ancel a reservation?"
            ],
            "metadata":[
                {
                    "name":"category",
                    "value":"api"
                }
            ]
        }
    ]
}
```
