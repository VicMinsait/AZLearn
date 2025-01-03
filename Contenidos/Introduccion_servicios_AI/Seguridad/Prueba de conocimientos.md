1. Debe regenerar la clave de suscripción principal para un recurso de Azure AI Services que usa una aplicación. ¿Qué debe hacer primero para minimizar la interrupción del servicio de la aplicación? 

- [x] Cambiar la aplicación para usar la clave secundaria
    - [x] Correcto. La aplicación puede usar la clave secundaria para acceder al recurso.
- [ ] Cambiar el punto de conexión del recurso
- [ ] Habilitar un firewall
  

2. Quiere almacenar las claves de suscripción de un recurso de Azure AI Services de forma segura, para que las aplicaciones autorizadas puedan recuperarlas cuando sea necesario. ¿Qué tipo de recurso de Azure debe aprovisionar? 

- [ ] Azure Storage
- [ ] Azure Key Vault
    - [x] Correcto. Use Azure Key Vault para almacenar las credenciales de forma segura.
- [x] Azure App Service

3. Al ejecutar el código en el equipo que se conecta a Azure AI Services, recibirá un error que le informará de que se denegó el acceso debido a las reglas de firewall o de red virtual. ¿Qué configuración debe establecer en la instancia de Azure AI Services? 

- [ ] En las propiedades de Redes, configure las redes seleccionadas y los puntos de conexión privados.
- [x] En las propiedades de Redes, agregue la dirección IP del cliente a la lista de firewalls permitidos.
  - [x] Correcto. Se puede permitir el acceso a la dirección IP pública del equipo en la configuración de Firewall.
- [ ] En Control de acceso, agregue su cuenta de usuario de Microsoft Entra ID a un rol.
