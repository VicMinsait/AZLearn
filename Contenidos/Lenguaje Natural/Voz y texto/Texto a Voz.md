# Uso de la API de Conversión de texto a voz

Se disponibilizan dos servicios de conversión de texto a voz en Azure:
- **Text-to-Speech**: Convierte texto en habla.
- **Batch Synthesis**: Admite operaciones por lotes (grandes volumenes de texto a audio)

## Uso del SDK
1. **SpeechConfig**: encapsula los accesos (región y clave de subscrición)
2. **AudioConfig**: Define la salida de audio.
3. **SpeechSynthesizer**: Cliente proxy para la api **TextToSpeech**.
4. **SpeechSynthesizer** tiene un método **speakTextAsync** que recibe el texto a convertir en habla y devuelve un objeto **SpeechSynthesisResult** con la siguiente información:
    - AudioData: Datos de audio en formato WAV.
    - Duration: Duración del audio.
    - Reason: Motivo por el que se detuvo la conversión.
    - ResultID: Identificador único de la conversión.
    - SpeechSynthesisResult: Resultado de la conversión.
    - Text: Texto convertido en habla.
