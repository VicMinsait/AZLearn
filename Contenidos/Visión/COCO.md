# COCO

Un archivo COCO es un conjunto de json's en un formato específico, que incluye información sobre imágenes, anotaciones, categorías. Se crean etiquetando las imágenes de entrenamiento en un proyecto de etiquetado de datos de Azure Machine Learning. Un JSON en un archivo COCO tiene el siguiente aspecto: 


```JSON
{
  "images": [
    {
      "id": 1,
      "width": 1024,
      "height": 768,
      "file_name": "abc.jpg",
      "coco_url": "AmlDatastore://fruit/abc.jpg",
      "absolute_url": "https://myBlobStorage.blob.core.windows.net/fruit/abc.jpg",
      "date_captured": "<date>"
    },
    {
      "id": 2,
      "width": 1024,
      "height": 768,
      "file_name": "xyz.jpg",
      "coco_url": "AmlDatastore://fruit/xyz.jpg",
      "absolute_url": "https://myBlobStorage.blob.core.windows.net/fruit/xyz.jpg",
      "date_captured": "<date>"
    },
    <...>
  ],
  "annotations": [
    {
      "id": 1,
      "category_id": 1,
      "image_id": 1,
      "area": 0.0
    },
    {
      "id": 2,
      "category_id": 1,
      "image_id": 2,
      "area": 0.0
    },
    <...>
  ],
  "categories": [
    {
      "id": 1,
      "name": "apple"
    },
    {
      "id": 2,
      "name": "orange"
    },
    {
      "id": 3,
      "name": "banana"
    }
  ]
}
``` 

Una vez que hay imagenes en un blob storage container, se puede crear un dataset de entrenamiento, a través de una solicitud http. La solicitud REST se ve de la siguiente manera: 

```bash
curl -X PUT https://<endpoint>/computervision/datasets/<dataset-name>?api-version=<version>\
    -H "Content-Type: application/json" \
    -H "Ocp-Apim-Subscriptsion-Key" <subscription-key> \
    --data-ascii \
    "{
    'annotationKind': 'imageClassification',
    'annotationFileUris':['<URI>']
    }"
```

Este método también está dispoinible desde Azure Vision Studio.
