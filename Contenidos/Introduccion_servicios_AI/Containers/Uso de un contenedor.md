# Despliegue de un servicio containerizado

En el portal de Azure, se puede crear un servicio de Azure AI containerizado. Para ello es necesario contar con un recurso de Azure del caracter correspondiente. Luego se pueden seguir los pasos:

1. En el portal de Azure se crea un nuevo recurso del tipo: **Container Instances**.
2. Se selecciona la suscripción y el grupo de recursos en el que se ha provisionado el recurso correspondiente.
3. Se completan los datos del contenedor a discreción, como se necesite para la aplicación que se desea desplegar.
4. SE ejecuta el contenedor y se obtiene la dirección IP del contenedor para acceder a la aplicación.
```bash
 docker run --rm -it -p 5000:5000 --memory 8g --cpus 1 mcr.microsoft.com/azure-cognitive-services/textanalytics/sentiment:latest Eula=accept Billing=<yourEndpoint> ApiKey=<yourKey>
```
