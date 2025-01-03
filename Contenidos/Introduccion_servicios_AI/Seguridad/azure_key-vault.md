# Azure key vault

Azure Key Vault es un servicio de azure que permite almacenar y gestionar secretos, tales como claves de acceso, contraseñas, certificados y otros datos sensibles.

Se le concede acceso a los secrtetos almacenados en Azure Key Vault a una identidad de servicio (Service Principal) que se utiliza para autenticar la aplicación con Azure a través de [[Microsoft Entra ID]]. 

Para conceder acceso a una aplicación, el desarrollador asigna a esta un Security Principal (asignado recibe el nombre de service principal) que luego la aplicación usa para acceder a los secretos almacenados en azure key vault. Controlando el acceso de esta forma se reduce el riesgo de exposición de secretos.
