# Entrenar un detector de objetos

La diferencia más importante entre entrenar un modelo de clasificación de imágenes y un modelo de detección de objetos es el formato del conjuto de datos. En el caso de la clasificación de imágenes, los datos requieresn la aplicación de una o varias marcas a toda la imagen. LA detección de obketos requiere que cada etiqueta conste de una marca y una región que defina el rectángulo delimitador de cada objeto en la imaegn.


## Etiquetado

Se pueden utilizar las siguientes alternativas para el etiquetado de las imágenes: 
1. La interfaz gráfica de del portal de Custom Vision de Azure AI. 
2. Herramientas de etiquetado proporcionadas por Microsoft como [Microsoft Visual Object Tagging Tool (VoTT)](https://github.com/microsoft/VoTT/blob/master/README.md) (actualmente descontinuado). 

En caso de usar una herramienta de etiquetado de terceros, es necesario ajustar la salida para que coincida con las unidades de medida que espera Custom Vision de Azure AI API. Los rectángulos delimitadores se definen mediante cuatro valores: 
* Coordenada Izquierda (X) (de la esquina superior izquierda)
* Coordenada Superior (Y) (de la esquina superior izquierda)
* Ancho
* Alto

Los valores se expresan como valores proporcionales, relativos al tamaño del archivo de imagen original.

Por ejemplo, 

```json
{
    "tags": [{
        "tag": "apple",
        "left": 0.1,
        "top": 0.1,
        "width": 0.5,
        "height": 0.5
    },
    {
        "tag": "banana",
        "left": 0.4,
        "top": 0.4,
        "width": 0.3,
        "height": 0.3
    }]
}
```
