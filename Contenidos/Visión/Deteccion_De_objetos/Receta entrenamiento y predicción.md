# Pasos para crear un modelo de detección de objetos

## Creación de un recurso de visión

1. En el portal de Azure hay que crear un recurso de **[[Custom Vision]]**.
    Es importante seleccionar la opción: **Create options: Both**

## Crear un proyecto de visión

1. Entrar al [Portal de Custom Vision](https://www.customvision.ai/).
2. Crear un proyecto haciendo uso del recurso que se creó en el paso anterior.

## Agregar y etiquetar imágenes

1. Agregar las imágenes al proyecto.
2. La herramienta de azure Custom Vision detecta autoáticamente objetos (sin etiquetas) de forma genérica. Si es necesario se puede ajustar un recuadro a la región de interés.
3. Ya que se tienen las regiones de interés, se pueden etiquetar las imágenes.

## Usar la API de entrenamiento
