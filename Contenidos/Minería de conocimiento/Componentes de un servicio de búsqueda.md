# Origen de datos

LAs soluciones de búsqueda comienzan definiendo un origen de datos. Este contiene los datos que se requieren indexar. Pueden ser: 
- Archivos no estructurados.
- tbalas de zure SQL DataBase
- Documentos de cosmos DB.

# Conjunto de aptitudes.

En Azure Search AI se peuden integrar aptitudes de Inteligencia Artificial para  enriquecer los datos del índice. Los ejemplos de información que puede extraer una apititud de Azure IA incluyen:
- Lenguaje 
- Frasess clave
- Calificación positiva o negativa
- ubicaciones
- Descripciones de imágenes generadas por ia.
- Aptitudes personalizadas.

# Indizador

Es el componente que lee los datos a indexar y asigna los campos de los datos a los campos de un índice. 


# Índice

- Es el almacén de datos que se crea a partir de los datos indexados.
- Es el que se consulta para recuperar información. 
- Consta de una colección de documentos JSON. cada campo de índice se puede configurar con los siguientes atributos
    - key: clave única para los registros del índice
    - searchable: campos que se pueden consultar mediante la búsqueda de texto completo.
    - filterable: campos que se pueden usar para filtrar resultados.
    - Sortable: campos que se pueden usar para ordenar resultados.
    - facetable: campos que se pueden usar para agrupar resultados.
    - Retrievable: campos que se pueden recuperar en los resultados de la consulta. (verdadero por defecto)
