1. ¿Qué API sería mejor para este escenario? Es necesario leer una gran cantidad de archivos con alta precisión. El texto son secciones cortas del texto manuscrito, algunas en inglés y otras en varios idiomas.

- [ ] Una API de lenguaje personalizada.
- [ ] API de document intelligence.
- [X] API de análisis de imágenes. 
    - [X] Correcto. LA característica OCR del serviico de análisis de imágenes es más adecuada para secciones cortas de texto manuscrito.

2. ¿Qué niveles de división devuelven los resultados de OCR?
- [ ] Sólo el contenido total y las páginas del texto.
- [X] Bloques, palabras y líneas de texto. 
    - [X] Correcto. Los resultados contienen bloques, palabras y líneas, así como cuadros de límite para cada palabra y línea.
- [] Contenido total, etiquetas de imágenes, páginas, palabras, y líneas de texto.
    - Incorrecto. Los resultados contienen bloques, palabras y líneas, así ocmo cuadros límite para cada palabra.
3.  Ha digitalizado una carta en formato PDF y necesita extraer el texto que contiene. ¿Qué tiene que hcaer?

- [ ] uso del servicio Azure AI Custom Vision.
- [ ] Uo de Image Analysis del servicio de Visión de Azure AI.
    - Incorrecto. El servicio de análisis de imágenes no es adecuado para extraer texto de documentos PDF.
- [X] Uso de la API de DocumentIntelligence.
    - [X] Correcto. LA api de inteligencia de documentos se puede usar para procesar archivos en formato PDF.
