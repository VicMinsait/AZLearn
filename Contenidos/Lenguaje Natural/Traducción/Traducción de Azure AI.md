# Traductor de Azure AI

ESte servicio provee recursos (**[[Azure AI Translate]]**) para la traducción de texto en varios idiomas.
Este servicio permite: 
- [[Detección]] de idiomas: identifica el idioma de un texto.
- [[Traducción]] de uno a varios idiomas: traduce texto de un idioma a varios idiomas.
- [[Transliteración]] de scripts: convierte texto de un script a otro.

# Opciones y parámetros de la api

Dado que diferentes idiomas en diferentes scripts pueden tener diferentes longitudes, fuentes, scripts, codificaciones, etc., la API de traducción de texto de Azure AI proporciona una serie de opciones y parámetros para personalizar la traducción de texto.

## **Alineación**: 
Por ejemplo, la traducción de  "Smart Services" de en (inglés) a zh (chino simplificado) genera el resultado "智能服务", y si no se conoce el idioma de origen o si no se tiene experiencia en el idioma de destino, se puede usar la alineación para obtener una traducción más precisa. El parámetro **`includeAlignment`** se establece como true para obtener en la traducción el siguiente resultado:

```json
{
    {
        "translations":[
            {
                "text":"智能服务",
                "to":"zh-Hans",
                "alignment":{
                    "proj":"0:4-0:1 6:13-2:3"
                }
            }
        ]
    }
}
```

## Longitud de oración

Si se desea conocer la longitud de una oración traducida para ajustar y controlar el uso de la traducción (por ejemplo al ajustar una interfaz de usuario), se puede usar el parámetro **`includeSentenceLength=true`** para obtener:
```json
{
    "translations":[
        {
            "text":"Salut to le monde",
            "to":"fr",
            "sentLen":{"srcSentLen":[12],"transSentLen":[20]}
        }
    ]
}
```

## Filtrado de lenguae obsceno

Si se desea ocultar u omitir obscenidades en el texto de salida, puede controlar la salida usando el parámetro **`profanityAction`**; con uno de los siguientes valores: 
- **`NoAction`**: Las palabras obscenas se traducen junto con el resto del texto.
- **`Marked`**: Las palabras obscenas se identifican mediante la técnica indicada en el parámetro **`profanityMarker`**
- **`Deleted`**: Las palabras obscenas se eliminan del texto de salida.
