1. ¿Qué objeto de SDK debe usar para especificar los idiomas a los que desea traducir la voz?
    - [ ] SpeechConfig
    - [X] SpeechTranslationConfig
        - [X] Correcto. Los idiomas de destino se especifican en el objketo SpeechTranslationConfig
    - [ ] AudioConfig

2. ¿Qué objeto de SDK debe usar como proxy para translation API del servicio de Voz de Azure AI?
    - [X] TranslationRecognizer
        - [X] Correcto. Debe usar TranslationRecognizer para llamar a Translation API del servicio de voz de azure AI.
    - [ ] SpeechRecognizer.
    - [ ] SpeechSynthetizer.

3. Al traducir voz, ¿en qué casos ppuede usar  el evento synthetizing para sintetizar las traducciones y la voz?
    - [X] Solo al trducir un udioma de destino único.
        - [X] Correcto. sólo puede usar la síntesis basada en eventos al traducir un idioma de destino único.
    - [ ] Sólo al traducir a varios idiomas de destino
    - [ ] Al traducir uno o varios idiomas de destino.
