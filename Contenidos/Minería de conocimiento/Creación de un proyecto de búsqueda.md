# Cómo crear un prooyecto de búsqueda en Azure Cognitive Search

Para ver los pasos detallados, visíte la [documentación oficial](https://microsoftlearning.github.io/mslearn-knowledge-mining/Instructions/Exercises/01-azure-search.html)
## Requisitos

1. Recurso: Azure AI Search 
2. REcurso: Azure AI Services
3. Recurso: Azure Storage Account
4. Datos: Documentos de los que se desea crear un índice

## Pasos

1. Creación de los recursos en Azure
    * Azure AI Search: Este recurso se encarga de crear el índice y a través de él se realiza la búsqudda.
    * Azure AI Services: Este recurso se encarga de realizar el enriquecimiento de los datos, haciendo uso de los servicios cognitivos de Azure.
    * Azure Storage Account: Este recurso se encarga de almacenar los datos que se van a indexar.
2. Subir documentos a Azure Storage. 
    ESto se puede hacer a través del portal de azure, o a través de solicitudes HTTP.
3. Indexar los documentos
    1. Desde el recurso de Azure Search: Conectar los datos 
    2. Agregar las aptitudes (Skills) en Attach Azure AI Services -> add enrichments 
    3. configurar las características de los documentos, índices, y campos



4. Buscar

# Búsqueda con Azure AI Index

En la **Overview** del recurso de búsqueda existe una pestaña/tab bajo el nombre **Search explorer**. 
En la sección **JSON View** se puede ver en formato JSON la forma de hacer búsqueda con json. Por ejemplo, para una búsqueda de todos los documentos (*), el JSON correspoindinte es:

```json
{
    "search":"*"
}
```
