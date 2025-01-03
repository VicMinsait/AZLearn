# Claves y accesos

El acceso a los servicios de Azure AI se concede a través de claves de suscripción. 

## Regeneración de claves

**Recomendaciones**: 

Regenere las claves de acceso de forma regular.
- Esto se puede hacer mediante Azure Portal, o a través de la CLI (Command Line Interface): 
    - ```az cognitiveservices account keys regenerate```

Cada servicio está provisto con dos claves de seguridad, para asewgurar la regeneración de claves sin interrupciones en el servicio.

**Proteja sus claves de acceso mediante Azure Key Vault**:

1. Cree un Azure Key Vault.
2. en el panel de secretos (En la sección de "Objetos"), cree un nuevo secreto.
3. En el botón "Generate/import" agregue un nuevo secreto.


**Crear una identidad de servicio (Service Principal)**:
Este proceso se puede realizar a través de la CLI de Azure, o mediante el portal de Azure. 
1. Desde la CLI, se ejecuta la siguiente instrucción:
    ```bash	
    az ad sp create-for-rbac -n "api://<spName>" --role owner --scopes subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>
    ```
2. Se obtienen metadatos con la información de la identidad de servicio creada, incluyendo el ID de la aplicación, el ID del objeto, la contraseña de la aplicación y el id de la subscriptción, (Tenant). Estos valores no se volverán a mostrar, por lo que es importante guardarlos en un lugar seguro.
3. Se consulta el ID de la identidad de servicio.
4. Se asigna permiso al ID de la identidad de servicio para acceder a los recursos de Azure AI.
