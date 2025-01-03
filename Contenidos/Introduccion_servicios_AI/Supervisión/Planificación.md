# Supervisión de costos

Antes de desarrollar servicios que usen los servicios de Azure AI, es una buena práctica hacer una proyeccción de costos haciendo uso de la herramienta de Azure, [Calculadora de Precios Azure](https://azure.microsoft.com/pricing/calculator/)

# Planificación de costos

Para visualizar los costos de los servicios de Azure AI,  se accede a la pestaña análisis de costos. A través de la aplicación de filtros se pueden restringir los datos para reflejar los costos de servicios específicos.

# Visualización de Métricas

Para visualizar las métricas de uso de los servicios de Azure AI, se accede al recurso y se selecciona la pestaña **Métricas**. **En esta sección no se visualizan costos.**

# Registors de diagnóstico

Para capturar registros de diagnóstico, es neceario configurar un servicio de almacenamiento en el cual alojar los registros de los servicios de Azure AI.

* **Azure Log Analytics**: Permite almacenar, consultar y visualizar los datos de regirstro en Azure Portal.
* **Azure Storage**: Servicio de Almacenamiento que permite almacenar archivos de regristro.

Una vez establecido el servicio de almacenamiento, se debe configurar el diagnóstico especificando *Nombre de la configuración de diagnóstico*, *Categorías de datos de eventos de registro* y *Destino de almacenamiento*.	
