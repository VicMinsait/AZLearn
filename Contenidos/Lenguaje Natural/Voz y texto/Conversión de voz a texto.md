# Uso de la API de conversión de voz a texto de Azure

Se disponibilizan dos servicios de conversión de voz a texto en Azure:
- **Speech-to-Text**: Convierte el habla en texto.
- **Speech to text Short Audio**: Optimizada para convertir el habla en texto en audios cortos.

## Uso del SDK

1. Use el objeto **SpeechConfig** para configurar la región y la clave de suscripción.
2. Use el objeto **AudioConfig** para definir el origen de entrada del audio (por defecto micrófono).
3. Use **SpeechConfig** y **AudioConfig** en conjunto para crear un objeto **SpeechRecognizer**: un cliente proxy para la api **SpeechToText**.
4. Use los métodos de **SpeechRecognizer** para llamar las funciones de la api. 
5. El resulato del método **recognizeOnceAsync** es un objeto **SpeechRecognitionResult** que contiene el texto reconocido y las siguiente propiedades:
    - Duration: Duración del audio.
    - OffsetInTicks: Tiempo en que se reconoció el texto.
    - Properties: Propiedades adicionales.
    - Reason: Motivo por el que se detuvo el reconocimiento.
    - ResultID: Identificador único de la transcripción.
    - Text: Transcripción del habla.
