# Pasos y requisistos para ejecutar el proyecto de NER

## requisistos

Para hacer inferencia con un modelo de NER de Azure AI se precisan los siguientes elementos:

1. Un recurso de lenguaje de Azure AI.
2. Una cuenta de almacenamiento de Azure (Storgae Account).
3. Un rol de acceso (Storgae Blob Data Contributor) para la cuenta de almacenamiento. (Con acceso a nivel de Usuario, Grupo o Aplicación (service principal))
4. Datos de muestra para el entrenamiento.
5. Un proyecto de NER con el recurso de Lenguaje en Azure Language Studio.


## Pasos

1. Crear un recurso de lenguaje en Azure AI.
    1. En este paso se puede crear también una cuenta de almacenamiento para asociarla al recurso de lenguaje.
2. Crear una cuenta de almacenamiento en Azure.
    1. Configurar el acceso anónimo (Anonymous acces level) a los contenedores de blobs.
    2. Crear un contenedor de blobs y configurar el nivel de acceso anómimo de lectura (Anonymous read access for containers and blobs).
3. Crear un rol de acceso para la cuenta de almacenamiento.
4. Agregar los datos de muestra
5. Crear un proyecto de NER en Azure Language Studio.
    * **Al crear el proyecto de NER se debe seleccionar el recurso de lenguaje y la cuenta de almacenamiento creados en los pasos anteriores.**
6. Etiquetar los datos en lla interfaz de azure language studio.
7. Entrenar el modelo.
8. Evaluar el modelo, reentrenar si es necesario.
9. Implementar/Publicar/Desplegar el modelo.
10. Hacer inferencia con el modelo desplegado. Es posible hacer inferencia con el SDK de Azure AI o con la API REST de Azure AI.

## Referencias

1. [Documentación de Azure AI](https://microsoftlearning.github.io/mslearn-ai-language/Instructions/Exercises/05-extract-custom-entities.html)

2. [SDK de AZURE AI para Python](https://learn.microsoft.com/en-us/python/api/overview/azure/ai-textanalytics-readme?view=azure-python)
