# Pipeline de enriquecimiento

El indizador o indexador es un proceso iterativo. Cada paso del proceso de indexación se encarga de un aspecto específico del contenido del índice. 

1. Inicialmente un documento iniciado es una estructura json  con los campos extraídos directamente , por ejmplo: 

* document 
    - metadata_storage_name # Nombre del archivo
    - metadata_author # Autor del documento
    - content # Contenido del documento

2. Si los documentos contienen imágenes, se puede configurar el indexador para extraer los datos de las imágenes y colocar cada imagen en una colección: 

* document
    - metadata_storage_name
    - metadata_author
    - content
    - normalized_images
        - image1
        - image2
        - image3

3. En seguida, cada aptitud agrega campos al documento, por ejemplo:

* document
    - metadata_storage_name
    - metadata_author
    - content
    - normalized_images
        - image1
        - image2
        - image3
    - language (1. Aptitud de lenguaje)
    - merged_content (2. Una aptitud de extraccion del texto en imagenes que comnina el texto de las imagenes con el texto del documento)
    - key_phrases (3. Una aptitud de frases clave)
    - Etc.
