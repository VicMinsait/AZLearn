# Intenciones, Expresiones y Entidades (Intents, Utterances and Entities)
Una expresión es una frase que un usuario puede escribir/decir/pensar al interactuar con una aplicación. Es la forma en que un usuario podría hacer una petición en lenguaje natural. Como preguntar por la hora, o pedir indicaciones para llegar a un lugar.

Un modelo de entendimiento de lenguaje se entrena mediante la definición de intenciones y su asociación a una o más expresiones.

### **Ejemplos de intenciones:**
- ConocerHora
- ConocerTiempo
- EncenderDispositivo

**Y las expresiones con las que se asocian:**

- ConocerHora:
    - ¿Qué hora es?
    - ¿Me puedes decir la hora?
    - ¿Podrías decirme la hora?
- ConocerTiempo:
    - ¿Cómo está el clima?
    - ¿Qué tiempo hace?
    - ¿Podrías decirme el pronóstico del tiempo?
- EncenderDispositivo:
    - Enciende la luz
    - Activa el ventilador
    - Prende la televisión

### Expresiones sin intención:
- None
    - Hola
    - Adiós

## Entidades

Las entidades son los elementos de una expresión que están asociados a valores o conceptos específicos. Por ejemplo en la inteicón *EncenderDispositivo* las entidades podrían ser *luz*, *ventilador* y *televisión*.

### **Ejemplos de entidades:**

| Expresión | Intención | Entidades |
| --- | --- | --- |
| ¿Qué hora es? | ConocerHora | None |
| Cuál es la hora en Nueva York | ConocerHora | Nueva York |
| Cuál es la previsión meteorológica de París? | ConocerTiempo | París |

Las entidades pueden ser de varios tipos:

* **Aprendizaje** Son entidades que el modelo no conoce y que se le enseñan para que las reconozca en el futuro.
* **De Lista** Son entidades que se definen en conjuntos específicos, y pueden tener sinónimos. Por ejemplo, los nombres de los días de la semana; La entidad de lista *DiaDeLaSemana* podría tener los valores *Lunes*, *Martes*, *Miércoles*; y los sinónimos *Lun*, *Mar*, *Mie*.
* **Precompiladas** Son entidades que ya están definidas en el modelo, como *Fecha*, *Hora*, *Número*, *CorreoElectrónico*, etc.
