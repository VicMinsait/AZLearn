1. Tiene previsto usar un contenedor de servicios de Azure AI en un host de Docker local. ¿Cuál de las afirmaciones siguientes es cierta? 

- [ ] Las aplicaciones cliente deben pasar una clave de suscripción al punto de conexión de recursos de Azure antes de usar el contenedor.
- [x] El contenedor debe poder conectarse al punto de conexión de recursos de Azure para enviar datos de uso para la facturación.
  - [x] Correcto. Las métricas de uso de contenedores se envían al recurso de Servicios de Azure AI en Azure para calcular la facturación.
- [ ] Todos los datos pasados desde la aplicación cliente al contenedor se reenvían al punto de conexión del recurso de Azure.
1. ¿Cuál de los parámetros siguientes debe especificar al implementar una imagen de contenedor de Servicios de Azure AI? 

- [x] EULA (End User Licence Agreement)
  - [x] Correcto. Debe especificar un parámetro EULA con el valor "yes" para aceptar explícitamente el contrato de licencia.
- [ ] ResourceGroup
- [ ] SubscriptionName

1. Tiene previsto usar la funcionalidad de detección de idioma de Lenguaje de Azure AI en un contenedor. ¿Qué imagen de contenedor debe implementar? 

- [ ] mcr.microsoft.com/azure-ai-services/textanalytics
- [ ] mcr.microsoft.com/azure-ai-services
- [x] mcr.microsoft.com/azure-ai-services/textanalytics/language
  - [x] Correcto. Debe implementar la imagen específica de la detección de idioma.
