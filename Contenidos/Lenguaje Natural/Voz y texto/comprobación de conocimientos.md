1. ¿Qué información neceita el recurso del servicio de voz de azure  para consumirla mediante el SDK de voz de azure AI?
    - [X] Región y clave de suscripción
        - [X] Correcto. El sdk de voz de azure requiere la ubicación y una clave para conectarse al servicio de voz de Azure AI.
    - [ ] Zonas principales y secundarias
    - [ ] El endpoint y una de las claves

2. Qué objeto debe usar para especificar que la entrada de voz proviene de un archivo de audio?
    - [ ] SpeechConfig
    - [X] AudioConfig
        - [X] Correcto- AudioConfig se usa para definir el origen de entrada del audio.
    - [ ] SpeechRecognizer

3. Cómo se puede cambiar la voz usada en la sítesis de voz?
    - [ ] Especifique una enumeración SpeechSynthesisOutputFormat en el objeto SpeechConfig.
    - [X] Establezca la propiedad SpeechSynthesisVoiceName en el objketo SpeechConfig en el nombre de voz deseado.
        - [X] Correcto. Para establecer una voz, establezca la propiuedad SpeehsynthesisVoiceName de SpeechConfig en un nombre de voz como "en-GB-George".
    - [ ] Especifique un nombre de archiov en el objeto AudioConfig.
