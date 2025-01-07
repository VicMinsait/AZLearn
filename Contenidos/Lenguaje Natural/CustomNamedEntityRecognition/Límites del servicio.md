# Límites del proyecto:

EL servicio de lenguaje de Azure AI aplica las siguientes restricciones; 

* **Entrenamiento**: Mínimo 10 archivos y máximo 100000. 
* **Implementaciones**: 10 implementaciones por proyecto.
* **APIs**: 
    - **Authoring**: Esta api crea un proyecto, entrena y despliega/implementa un modelo. Está limitada a 10 solicitudes POST y 100 solicitudes GET por minuto.
    - **Analyze**: Esta es la API que extrae entidades con modelos ya implementados. Está limitada a 20 POST o GET por minuto.
* **Proyectos**: Una sóla cuenta de almacenamiento por proyecto, y un máximo de 500 proyectos por recurso.
* **Modelos**: 50 modelos entrenados por proyecto.
* **Entidades**: Cada entidad puede tener un máximo de 500 caracteres, y se pueden tener 200 diferentes tipos de entidades.


