# Pasos para la creación de un proyecto de clasificación de texto

- **Definir etiquetas**: 
- **Etiquetar datos**
- **Entrenar modelo**
- **Revisar resultados de entrenamiento**
- **Ajustar modelo**
- **Desplegar modelo**
- **Clasificar texto**

El servicio de Azure AI Language provee herramientas para pptimizar el proceso de creación de un modelo:

# Opciones para particionar 

- **Particion automática**: Azure aplica algoritmos de partitición de datos de forma automática. Esta opción es más útil si los datos son suficientemente grandes, son naturalmente consistentes, o la distribución de los datos es uniforme.
- **Particion manual**: El usuario puede especificar la partición de los datos. Esta opción es más útil si los datos son pequeños, no son consistentes, o la distribución de los datos no es uniforme.

# Facilidades de despliegue

Azure permite crear multiples modelos y multiples despliegues de un mismo modelo. Esto permite: 

- Probar modelos paralelamente
- Comparar el impacto del estilo de entrenamiento
- Desplegar diferentes versiones del modelo
