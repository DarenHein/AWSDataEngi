
## ⏳ Acto 1: Los años 70 y 80 – El Nacimiento del Orden (La Era SQL)

Antes de los años 70, guardar datos en una computadora era el viejo oeste: cada programa guardaba archivos de texto a su manera y si querías cruzar información, tenías que picar código de bajo nivel durante días.

Todo cambió en **1970** gracias a un matemático de IBM llamado **Edgar F. Codd**. Él publicó un artículo revolucionario donde inventó el **Modelo Relacional** (sí, las tablas, filas, columnas y llaves que acabamos de estudiar). A finales de los 70 nació **SQL** como el lenguaje universal para hablarle a esas tablas.

* **El problema de la época:** El almacenamiento era ridículamente caro. Guardar un megabyte costaba una fortuna. Por eso, el diseño relacional se enfocó en la **normalización** (reglas estrictas para no duplicar ni una sola palabra y ahorrar espacio).
* **Quién mandaba aquí:** El **Administrador de Bases de Datos (DBA)**. Él era el dios del centro de cómputo; cuidaba el servidor con su vida y decidía quién podía hacer un `INSERT` o un `SELECT`.

---

## 📈 Acto 2: Los años 90 – Nace el "Business Intelligence" (OLAP y Data Warehouses)

Para los años 90, las empresas ya tenían computadoras en todas sus sucursales. Las bases de datos transaccionales (OLTP) estaban llenas de ventas, pero los directores empezaron a preguntar: *"Oye, ¿cuánto vendimos en total el año pasado en toda la región norte comparado con la región sur?"*.

Si el DBA corría esa consulta pesada en la base de datos de producción, **el sistema del banco o de la tienda se congelaba** y los clientes no podían comprar.

Aquí es donde entra el padre de los datos modernos, **Ralph Kimball** (y Bill Inmon), quienes dijeron: *"Hay que separar la iglesia del estado"*. Crearon los **Data Warehouses** (Almacenes de Datos).

* **El nacimiento del ETL:** Nació el concepto de **E**xtraer los datos de las tiendas, **T**ransformarlos (limpiarlos) y **L**oad (Cargarlos) en un servidor gigante diseñado solo para hacer reportes (OLAP).
* **La herramienta reina:** El software comercial cerrado (Informatica PowerCenter, IBM DataStage). Eran herramientas visuales de arrastrar cajitas.
* **El rol de la época:** El **Desarrollador BI (Business Intelligence) o Desarrollador ETL**. Su trabajo era hacer que los cubos de datos alimentaran reportes de Excel para los jefes.

---

## 💥 Acto 3: Los 2000s – La Explosión del Big Data (El internet rompe el molde)

A finales de los 90 y principios de los 2000, llegaron unos monstruos llamados **Google, Yahoo! y Facebook**.

El internet explotó. Ya no solo se guardaban facturas de banco; ahora la gente subía fotos, daba clicks, mandaba mensajes y buscaba cosas por millones cada segundo. Las bases de datos relacionales tradicionales de Oracle o PostgreSQL **simplemente tronaron**. No podían aguantar ese volumen de datos semiestructurados ni de chiste, y comprar un servidor más grande costaba millones de dólares.

Google resolvió el problema primero y, como de costumbre, publicó su secreto al mundo en unos artículos científicos (Whitepapers) entre 2003 y 2004: inventaron el **GFS (Google File System)** y **MapReduce**.

En 2006, un ingeniero llamado Doug Cutting leyó esos artículos y creó un proyecto Open Source (código abierto) basado en ellos. Lo nombró como el elefante de juguete de su hijo: **Hadoop**.

* **La revolución de Hadoop:** En lugar de comprar un supercomputador carísimo, Hadoop permitía conectar 100 computadoras baratas normales en un "Cluster" (un equipo) y guardar archivos gigantescos repartidos entre todas (HDFS), procesando los datos en paralelo.
* **Nace NoSQL:** En esta misma década nacen **MongoDB, Cassandra y Redis**. Las empresas se dieron cuenta de que para la velocidad de internet, necesitaban romper las tablas rígidas y usar Clave-Valor o Documentos.

---

## 🚀 Acto 4: De 2010 a la Actualidad – El nacimiento oficial del "Data Engineer"

A principios de 2010, trabajar con Hadoop era un dolor de cabeza horrendo. Tenías que escribir cientos de líneas de código en Java (MapReduce) solo para hacer un conteo simple de palabras. Los científicos de datos pasaban el 80% de su tiempo peleándose con la infraestructura en lugar de hacer modelos de Inteligencia Artificial.

En **2014**, la Apache Software Foundation adoptó un proyecto nacido en la Universidad de Berkeley que mandó a Hadoop al museo: **Apache Spark**. Spark procesaba los datos en la memoria RAM en lugar de escribir todo el tiempo en el disco duro, siendo hasta 100 veces más rápido.

Fue en este punto medio de la década de 2010 cuando las empresas de Silicon Valley (como Facebook, Netflix y Airbnb) se dieron cuenta de que necesitaban un rol especializado. Ya no bastaba con el desarrollador ETL que arrastraba cajitas, ni con el DBA. Necesitaban a un **Ingeniero de Software que supiera de sistemas distribuidos, código (Python, Scala), infraestructura en la nube y pipelines**.

> 💡 **Ahí nació oficialmente el término: Data Engineer (Ingeniero de Datos).**

---

## 🌌 El día de hoy (2026) y hacia dónde vas:

Hoy en día, el almacenamiento es tan barato que ya no hacemos ETL puro; hacemos **ELT** (guardamos todo en crudo en un *Data Lake* en la nube como AWS, Azure o GCP y luego lo transformamos usando el poder de cómputo de herramientas modernas).

Tú estás estudiando exactamente la cúspide de esta evolución:

* Sabes por qué elegir **SQL vs NoSQL** (porque entiendes la crisis de los 2000s).
* Entiendes **Batch vs Streaming** (porque el negocio ya no quiere esperar al reporte nocturno de los 90s, quiere ver los datos fluir como un río en vivo).
* Usas **Orquestadores (DAGs)** para que el pipeline no dependa de un simple script manual.
