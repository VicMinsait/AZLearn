# Administración de los límites de los recursos de búsqueda

Al crear un recurso de búsqueda se selecciona un plan de tarifa. Cada plan de tarifa tiene un impacto en los límites de uso de los recursos:

- **Free (F)**: Este plan es reducido, generalmente para probar tutoriales y hacer exploración del recurso.
- **Basic (B)**: Búsqeuda a pequeña escala (Máximo de 15 índices y 5 GB de almacenamiento).
- **Standard (S)**: Escala empresarial
- **Storage Optimized (L)**: Índices de gran tamaño, a costa de una mayor latencia de consulta.

## Réplicas y particiones 

* Las réplicas:
    - Instancias del servicio de búsqueda (Como nodos de un cluster)
    - A mayor número de réplicas, mayor disponibilidad y rendimiento; mayor número de solicitudes de consulta simultáneas

* Las particiones:
    - Distribución de un índice en varias ubicaciones de almacenamiiento 

* Unidades de búsqueda:
    - Cada réplica y partición consume una unidad de búsqueda. ES decir, el número de unidades de búsqueda es el número de réplicas multiplicado por el númnero de particiones del servivio (SU = R*P)
    - El número de unidades de búsqueda determina el costo del servicio
    - 

