# Temario de Estudio: Ingeniería de Datos para AWS DEA-C01

## 1. Fundamentos y Arquitectura de Datos
*   **Ciclo de Vida del Dato:** Generación, ingesta, almacenamiento, procesamiento, servicio y archivado/destrucción.
*   **Modelado de Datos:**
    *   Diseño de bases de datos relacionales vs. NoSQL (Clave-Valor, Documentos, Grafos).
    *   Modelado analítico: Esquema en Estrella (*Star Schema*) y Esquema en Copo de Nieve (*Snowflake Schema*).
    *   Tablas de Hechos (*Fact Tables*) vs. Tablas de Dimensiones (*Dimension Tables*).
*   **Sistemas de Almacenamiento:**
    *   **Data Lake:** Concepto, almacenamiento masivo desacoplado, almacenamiento de objetos, *Schema-on-Read*.
    *   **Data Warehouse:** Almacenamiento relacional estructurado, almacenamiento columnar, *Schema-on-Write*.
    *   **Data Lakehouse:** Arquitecturas híbridas utilizando formatos de tabla abiertos (Apache Iceberg, Delta Lake).

---

## 2. Ingesta de Datos (Data Ingestion)
*   **Estrategias de Ingesta:**
    *   **Procesamiento por Lotes (Batch):** Transferencia de grandes volúmenes de datos a intervalos programados.
    *   **Tiempo Real (Streaming):** Captura y procesamiento continuo de eventos con baja latencia.
*   **Mecanismos de Captura:**
    *   **CDC (Change Data Capture):** Identificación y captura de inserciones, actualizaciones y eliminaciones en bases de datos origen.
    *   Inyecciones basadas en archivos, APIs de terceros y Webhooks.
*   **Conceptos de Streaming:** Ventanas de tiempo (*Tumbling, Sliding, Session windows*), particionamiento de streams y manejo de datos tardíos.

---

## 3. Procesamiento y Transformación de Datos (ETL/ELT)

*   **Patrones de Pipeline:**
    *   **ETL (Extract, Transform, Load):** Transformación en tránsito antes del almacenamiento definitivo.
    *   **ELT (Extract, Load, Transform):** Carga directa al Data Lake y uso del poder de cómputo del destino para transformar.
*   **Formatos de Archivos e Inmutabilidad:**
    *   Formatos de fila (CSV, JSON, Avro) vs. Formatos columnares (Parquet, ORC).
    *   Compresión de datos (Gzip, Snappy, Bzip2) y su impacto en el rendimiento de lectura.
    *   Estrategias de Particionamiento y Distribución de datos en sistemas de archivos.
*   **Procesamiento Distribuido:**
    *   Conceptos de **Apache Spark / PySpark** (DataFrames, RDDs, transformaciones *lazy*, acciones, optimización de queries).
    *   Conceptos de motores SQL federados (Presto / Trino).

---

## 4. Orquestación y Automatización
*   **Flujos de Trabajo (Workflows):**
    *   Concepto de **DAG (Directed Acyclic Graph)** o Grafo Acíclico Dirigido para definir dependencias de tareas.
    *   Manejo de reintentos (*retries*), alertas por fallas y manejo de estados.
    *   Orquestación programada (*cron-based*) vs. Orquestación basada en eventos (*event-driven*).

---

## 5. Gobernanza, Calidad y Seguridad de Datos
*   **Gobernanza:**
    *   **Catálogo de Datos y Metadatos:** Diccionarios de datos, linaje del dato (*data lineage*) para saber de dónde viene y a dónde va un dato.
*   **Calidad del Dato (Data Quality):**
    *   Validación de esquemas, detección de valores nulos o corruptos, perfiles de datos (*data profiling*).
*   **Seguridad:**
    *   Cifrado de datos en reposo (at rest) y en tránsito (in transit).
    *   Enmascaramiento de datos, tokenización y anonimización de datos sensibles (PII).
    *   Control de acceso granular: RBAC (Acceso basado en roles) y ABAC (Acceso basado en atributos) a nivel de fila y columna.