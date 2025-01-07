1. You want to include a sentiment score for each document in an index. What should you do? 
    - [ ] Create a custom skill that uses an Azure Machine Learning model to predict the sentiment for a document
    - [ ] Create a custom skill that calls the Azure AI Language service and predicts the sentiment of each document.
    - [X] Add the built-in Sentiment skill to the skillset used by the indexer.
       - [X] Corrrecto. La habilidad Sentiment es una habilidad integrada que puede agregar a un skillset para calcular el sentimiento de un documento.

2. You implemented a custom skill as an Azure function. You want to include the custom skill in your Azure AI Search indexing process. What should you do? 
    - [X] Add a WebApiSkill to a skillset, referencing the Azure function's URI
        - [X] Correcto. Para integrar una habilidad personalizada en un pipeline de enriquecimiento, debe agregar un WebApiSkill a un skillset y especificar el URI de la función de Azure. 
    - [ ] Create a JSON document with the input schema for your function, and save it in the folder where the documents to be indexed are stored.
    - [ ] Submit each document to the function, and store the output in a separate data source. Then use the Merge skill to add the results to the index.

3. When you create an Azure AI Language project, if you let the model automatically split your training data, what percentage of the documents will it use to train the model, by default? 

    - [ ] 20%
    - [ ] 50%
    - [X] 80%
        - [X] Correcto. De forma predeterminada, el modelo dividirá el 80% de los documentos en el conjunto de entrenamiento y el 20% restante en el conjunto de validación.
4. When you create an Azure Machine Learning custom skill, what type of endpoint does the URI have to use? 

- [X] The URI has to use an HTTPS endpoint
    - [X]  Correcto. El URI de un servicio de aprendizaje automático personalizado debe usar un punto de conexión HTTPS.
- [ ] The URI has to use an HTTP endpoint
- [ ] The URI has to use an FTP endpoint
