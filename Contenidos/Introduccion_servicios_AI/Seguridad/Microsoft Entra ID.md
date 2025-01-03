# Microsoft Entra ID

Es un servicio de administración de identidades y acceso basado en la nube. Se usa para acceder a recursos externos, por ejemplo MS365, Azure Portal, [servicios de Azure AI](../Servicios%20de%20Azure%20AI.md), etc.

Hay diferentes formas de acceder a los servicos de Azure AI mediante Microsoft Entra ID, entre los que se encuentran: 


# **Mediante entidades de servicio**

1. Creación de un [[subdominio personalizado]]
   1. Vinculación de un recurso de Azure AI al subdominio personalizado.
2. Registrar una aplicación.
3. Asignación de una [[entidad de servicio]] (con Azure New-AzAdServicePrincipal).
4. Asigne el rol **Cognitive Services User** a la entidad de servicio.

# **Mediante identidades administradas**: 

- **Identidad Administrada por el sistema**: Se crea una identidad administrada y se vincula a un recurso específico como una máquina virtual que necesita acceder a los servicios de Azure AI. Cuando se elimina el recurso, también se elimina la identidad administrada.
- **Identidad Administrada por el usuario**: La identidad administrada se crea para que sea utilizable por varios recursos en lugra de estar vinculada a una sola. Existe independientemente de un recurso único.



 

