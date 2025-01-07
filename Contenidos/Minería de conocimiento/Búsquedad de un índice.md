# Búsqueda y técnicas 

## Full Text Search, FTS (Búsqueda de texto completo)

Es común que se busque un texto específico en un conjunto de documentos. FTS es una técnica que permite buscar texto basado en el elnguaje _Lucene_ en las siguientes modalidades: 

- **Simple**: Busca palabras completas.
- **FUll**: Una sintaxis extendida que permite hacer búsqueda por filtrado, expresiones regulares, y otras formas sofisticadas.

Las aplicaciones cliente envían solicitudes especificando una expresión (en formato [Lucene] mediante [[FTS]]) junto con otros parámetros  que determinan cómo se evalua la expresión y los resultados obtenidos. 
- search: Expresión de búsqueda.
- queryType: El tipo de consulta lucene.
- searchFields: Campos en los que se busca.
- select: Campos que se devuelven en los resultados.
- searchMode: Modo de búsqueda (all, any, etc.)

El proceso de recuperación se segmenta en 4 procesos:
1. Query parsing: Se analiza y estructura la expresión de búsqueda, para incluír diferentes niveles de búsqueda (palabras únicas, frases, etc.)
2. lexical analysis: Se tokeniza el texto en palabras y se eliminan las palabras vacías.
3. Document Retrieval: Se recuperan los documentos que coinciden con la expresión de búsqueda.
4. Scoring: Se asigna un puntaje a cada documento recuperado, basado en la relevancia de la búsqueda.
