# Entendiendo contenedores

Un servicio de software generalmente se aloja (Hosts) en un entorno que provee el hardware, el sistema operativo, y componentes que soportan la ejecución del software. Azure ofrece la posibilidad de hostear servicios y desarrollos en contendores, que son una forma de encapsular los componentes que soportan la ejecución de un servicio o software. 

El despliegue de servicios de Azure AI en contendores, es útil cuando se requiere de un ambiente que no permita la salida de datos a openweb, o cuando se requiere de un ambiente aislado para la ejecución de un servicio.


El desarrollo en contenedores resulta en dow grandes beneficios: 
- **Portabilidad**: Los contenedores pueden ser ejecutados en diferentes ambientes y sistemas operativos. Facilitando la migración de servicios entre diferentes ambientes.
- **Multiplicidad**: Un mismo host puede ejecutar múltiples contenedores, permitiendo la ejecución de múltiples servicios en un mismo host.

## **Despliegue de contenedores**

Para desplegar y usar un servicio de Azure AI en un contendor se requiere de los siguientes pasos:

1. La imagen que se desea desplegar se descarga y despliega en un *Container Host* (Alojador de contenedores), como un servidor de Docker, una instancia de Azure Container Instance (ACI),  o un servicio de Kubernetes en Azure Kubernetes Service (AKS).
2. Las aplicaciones cliente sirven datos al endpoint que el contenedor expone.
