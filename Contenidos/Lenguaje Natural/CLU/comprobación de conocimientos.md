1. La aplicación debe detectar un comando como "activar la luz" o "Encender la luz". ¿Qué representan estas frases en un modelo de lenguaje"?

- [ ] Intenciones
- [X] Expresiones
    - [X] Correcto. Las expresiones son frases de ejemplo que indican una intención específica.
- [ ] Entidades

2. La aplicación debe interpretar un comando para reservar un vuelo a una ciudad específicada, como "Reservar un vuelo a parís". ¿Cómo se debe modelar el elemento "city" (ciudad) del comando?

- [ ] Como una intención
- [X] Como una entidad
    - [X] Correcto. La ciudad es una entidad a la que se le debe aplicar la intención.
- [ ] Como una expresión

3. El modelo de lenguaje debe detectar un correo electrónico cuando está presente en una expresión. ¿Cuál es la manera más sencilla de extraer ese correo electrónico?

- [ ] Usar una expresión regular
- [X] Uso de componentes de entidad pregenerados
    - [X] Correcto. Cuando un modelo de lenguaje necesita detectar una entidad común, use componentes creados previamente para que el servicio de lenguaje de azure AI detexte la entidad.
- [ ] Uso de componentes de entidad aprendidos
