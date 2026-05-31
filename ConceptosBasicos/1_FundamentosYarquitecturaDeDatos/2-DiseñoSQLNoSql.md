
### DISEÑO SQL , NOSQL (Clave-valor , grafos)

El como elegir como guardar nuestra informacion deoendiendo de como la va a usar negocio 

las bases de datos se dividen en dos grandes 
__RElacionales -> SQL__ y las __NOSQL no relacionales__

### __BASES DE DATOS RELACIONALES__

estas son las base de datos tradicionales que se rijen por filas y columnas (LLAVES PRIMARIAS Y LLAVES FORANEAS)

Ejemplo : 

    * postgre SQL 
    * MySQl 
    * Oracle 

funcionan bajo el imperio del __SCHEMA-ON-WRITE__ 

## CUANDO USARLAS 

las bases de datos relacionales mayormanete. se ocupan cunado nuestro schema es fijo y nunca se cambiara 

__EJEMPLO__ : 

|-------------------------------|
|  Llave    |  Valor            |
|-------------------------------|
|  mascota  |  {                | 
|           |    nombre: Laika  |
|           |  }                |
|-------------------------------|

## Recurda no podemos leer el json la base de datos lo toma como texto plano no como formato json o bson 

## __BASE DE DATOS NO RELACIONALES (NO SQL)__

Las bases de datos no sql o no relacionales rompen el esquema tradiconal de las filas y columnas nacieronn para solucionar errores de big data son datos __semi Estructurados__ quiere decir que son json , xmk etc 

en lugar de tablas rigidas , estas se dividen en varios ripos 

# A) CLAVE VALOR KEY_VALUE
Es una BASE DE DATOS DE DOS COLUMNAS : una llave y un valor ok 

guarda los datos en parejas tenesmoc una clave como una llave unica y esta tiene asociada un valor puede ser cualquier coas (numero , string , img) para leer ese valor tenemos que llmar a la clave 

__ejemplo : REDIS__

# B) BASE DE DATOS DE DOCUMENTOS  __Document Store Database__

es la evolucion de la base de datos __clave valor__ pero con una gran diferencia en estasi es capaz de ver que hay dentro del json y no lo toma como texto plano como el __clave valor__

__a que se refiere con documento ?__

en las bases de datos relaciones todo lo acumulamos en tablas con filas y columnas en este caso como MongoDB almacenamos en archivos individaules llamados __Documentos__

la mayor parte de los casos los documentos estan escritos en formato __JSON__ (javascript object notation) o en su version binaria y ultra rapida el __BSON__

Ejemplo de un JSON : 

__Documento 1__

{
    "nombre" : "Luis", 
    "Edad" : 30 
}

__la cracteristica estrella : Esquema Flexible__

en una base de datos relaciones la que se basa en filas y columnas todas las filas estab obligadas a tener exxactamente las mismas columnas si una columna esta vacia se rellena con __null__ 

en los __Documents Stores__ reina la flexibilidad absoluta cada documento puede tener su propia estructura totalmente diferente a los demas aunque vivan en la misma coleccion (qie es el equivalente a una tabla)

# C) GRAFOS (Graph Databases)

Estas bases de datos se olvidan por completo de las tablas y documentos se enfocan %100 en las relaciones entre las cosas 

HERRAMIENTA MAS FAMOSA : __Neo4j__

Fisicamente un grafo es como un mapa o una telaraaña 

__Elementos Fundamentales__

__NODOS__ (nodes) : son los circulos del mapa que representan las cosas o entendades 

ejemplo  : 
(Nodo)                 [Borde / Relación]                (Nodo)
 [Kevin] ─────────────────── ES_AMIGO_DE ──────────────────> [Luis]
 [Kevin] ───────────────── TIENE_LA_CONSOLA ───────────────> [PS5]
  [Luis] ────────────────────── JUEGA ─────────────────────> [Silent Hill]

__Bordes__ o Relaciones (edges/Relationships) : son las lineas o flechas que unen a los __nodos__
esto es lo mas importante de un grafo ya que que el __borde__ es quien marca la relacion o como se relacionan ambos __nodos__ que une 

ejemplo  : 

  (Nodo)                 [Borde / Relación]                (Nodo)
 [Kevin] ─────────────────── ES_AMIGO_DE ──────────────────> [Luis]
 [Kevin] ───────────────── TIENE_LA_CONSOLA ───────────────> [PS5]
  [Luis] ────────────────────── JUEGA ─────────────────────> [Silent Hill]

-------------------------------------------------

### CUESTIONARIO 

## Cuestionario: Diseño y Selección de Bases de Datos (SQL vs. NoSQL)
## Bloque 1: Filosofía SQL vs. NoSQL y Schema-on-Write

1. ¿Cuál es la principal característica de las bases de datos relacionales (SQL) tradicionales como PostgreSQL o MySQL al momento de guardar información?
A) Guardan los datos de forma lineal en archivos de audio de alta fidelidad.
B) Almacenan la información en tablas rígidas estructuradas estrictamente por filas y columnas mediante llaves primarias y foráneas.
C) Permiten que cada fila tenga columnas totalmente diferentes sin importar el diseño inicial.
D) No permiten realizar uniones o relaciones entre diferentes conjuntos de datos.

2. ¿A qué se refiere el imperio del "Schema-on-Write" bajo el cual se rigen las bases de datos SQL?
A) A que puedes escribir cualquier dato deforme y la base de datos creará el esquema después.
B) A que el esquema o estructura de la tabla debe estar previamente definido y el dato debe adaptarse obligatoriamente a él antes de poder ser escrito/guardado.
C) A que la base de datos borra el esquema cada vez que un usuario realiza una nueva escritura.
D) A que el programador debe escribir el código de la base de datos a mano en papel antes de usar la computadora.

3. Las bases de datos NoSQL nacieron principalmente para resolver errores y retos de la era del Big Data. ¿Qué tipo de datos manejan mayormente estas tecnologías?
A) Datos tabulares planos binarios analógicos.
B) Datos estrictamente fijos que nunca cambian de tamaño ni de formato.
C) Datos semiestructurados (como archivos JSON o XML) y no estructurados.
D) Únicamente hojas de cálculo de Microsoft Excel antiguas.

## Bloque 2: NoSQL Clave-Valor (Key-Value)

4. ¿Cuál es la estructura física fundamental de una base de datos NoSQL de tipo Clave-Valor?
A) Un mapa tridimensional de árboles binarios en cascada.
B) Conceptualmente, es una tabla simple de dos columnas: una columna para la Llave única y otra para el Valor.
C) Una red compleja de círculos conectados por líneas direccionales.
D) Una carpeta de archivos de texto donde no existen las contraseñas ni las llaves.

5. Si guardas un JSON dentro de la columna de "Valor" en una base de datos Clave-Valor como Redis, ¿cómo interpreta el motor de la base de datos ese contenido?
A) Como un documento inteligente del cual puede leer e indexar sus propiedades internas de forma nativa.
B) Como un error de sintaxis que bloquea el servidor de inmediato.
C) Como texto plano o un bloque de bytes ciego; no puede leer lo que hay dentro del JSON.
D) Como una nueva tabla relacional con llaves foráneas automáticas.

6. ¿Cuál es la única forma nativa y eficiente de recuperar un dato en una base de datos Clave-Valor?
A) Lanzando una consulta de filtrado sobre los atributos internos del valor.
B) Solicitando el dato directamente a través de su Clave o Llave única.
C) Realizando un JOIN entre múltiples colecciones en memoria RAM.
D) Escaneando secuencialmente toda la base de datos desde el primer registro hasta el último cada vez.
Bloque 3: NoSQL Documentos (Document Store)

7. ¿Cuál es la evolución y gran diferencia de las Bases de Datos de Documentos (Document Stores) respecto a las de Clave-Valor?
A) Que las de documentos eliminan por completo la columna de la llave principal.
B) Que en los Document Stores el motor sí tiene "ojos" y es capaz de ver, indexar y buscar por los campos internos del JSON.
C) Que los Document Stores guardan la información únicamente en archivos PDF de solo lectura.
D) Que obligan a que todos los JSON tengan exactamente el mismo tamaño en bytes.

8. ¿Cómo se le conoce a la característica estrella de herramientas como MongoDB donde cada documento JSON puede tener una estructura totalmente diferente a los demás dentro de la misma colección?
A) Esquema Rígido (Schema-on-Write).
B) Inmutabilidad de Datos Relacionales.
C) Esquema Flexible o Libre de Esquema (Schemaless).
D) Particionamiento de Relaciones de Red.

9. En una base de datos relacional (SQL), si una fila no tiene datos para una columna específica, el sistema la rellena con un valor NULL. ¿Cómo resuelve esta situación un Document Store como MongoDB?
A) Te obliga a inventar un dato falso para poder guardar el archivo.
B) Simplemente no incluye ese campo en el JSON de ese documento específico, manteniendo la flexibilidad absoluta.
C) Borra todo el documento de forma automática por estar incompleto.
D) Detiene la aplicación web y manda una alerta de error crítico al administrador.
Bloque 4: NoSQL Grafos (Graph Databases)

10. ¿En qué se enfocan al 100% las bases de datos de Grafos (Graph Databases) como Neo4j?
A) En almacenar archivos de imágenes y gráficos vectoriales de alta velocidad.
B) En las relaciones y conexiones entre las cosas, tratando a la relación como un elemento tan importante como el objeto mismo.
C) En simular tablas de Excel interconectadas por macros automáticas.
D) En guardar listas ordenadas de números enteros en la memoria caché del procesador.

11. ¿Cuáles son los dos elementos fundamentales que componen físicamente la estructura de un Grafo?
A) Filas y Columnas.
B) Llaves y Valores ciegos.
C) Nodos (círculos que representan entidades) y Bordes/Relaciones (líneas que los conectan).
D) Documentos JSON y Colecciones XML.

12. En un Grafo que mapea una red social, tienes un nodo [Kevin] y un nodo [Luis]. ¿Qué elemento se encarga de 
marcar la conexión "ES_AMIGO_DE" entre ambos?
A) La Llave Primaria del nodo Kevin.
B) El Borde o Relación (Edge / Relationship) que une a ambos nodos.
C) Un campo de texto oculto dentro de un documento JSON secundario.
D) Un archivo Log de Transacciones (WAL).
Bloque 5: Toma de Decisiones según el Negocio

13. El equipo de Finanzas de una empresa te pide diseñar la base de datos para el sistema de transferencias de dinero. Exigen consistencia absoluta, seguridad matemática y aseguran que los datos de las transacciones (origen, destino, monto) nunca van a cambiar de estructura. ¿Qué arquitectura debes elegir?
A) NoSQL de Grafos.
B) NoSQL Clave-Valor.
C) Base de Datos Relacional (SQL).
D) NoSQL de Documentos.

14. Una aplicación móvil de e-commerce necesita que cuando un usuario inicie sesión, su perfil y los artículos guardados en su carrito de compras aparezcan instantáneamente en microsegundos. El sistema sólo buscará esta información usando el ID único del usuario. ¿Qué tipo de base de datos es la óptima para esta capa de caché?
A) NoSQL Clave-Valor (Key-Value Store).
B) Base de Datos Relacional tradicional (SQL).
C) NoSQL de Grafos (Graph Database).
D) Un archivo CSV guardado en el disco duro.

15. Un banco internacional te contrata para diseñar un sistema capaz de detectar fraudes complejos. Necesitan analizar de forma visual y rápida cómo se conectan los clientes sospechosos entre sí, qué cuentas comparten el mismo número de teléfono y si pertenecen a una red organizada de lavado de dinero. ¿Qué base de datos resuelve esto eficientemente?
A) NoSQL Clave-Valor (Key-Value Store).
B) Base de Datos de Grafos (Graph Database).
C) Base de Datos Relacional (SQL).
D) NoSQL de Documentos (Document Store).

### 🔑 Hoja de Respuestas y Justificaciones Técnicas
Pregunta	Respuesta Correcta	Justificación Técnica
1	B	Las bases de datos relacionales organizan los datos en estructuras bidimensionales (tablas) compuestas por registros (filas) y atributos (columnas), usando llaves para garantizar la integridad referencial.
2	B	Schema-on-Write significa que el motor valida la estructura del dato contra el esquema de la base de datos antes de permitir la inserción. Si no coincide, la transacción falla.
3	C	Big Data requiere manejar formatos que no encajan en tablas rígidas, como JSON, XML o texto libre, conocidos como datos semiestructurados o no estructurados.
4	B	El modelo Clave-Valor es conceptualmente un diccionario o mapa asociativo de dos columnas, optimizado para indexar por una única llave.
5	C	Para un almacén Clave-Valor puro, el "Valor" es una cadena opaca de bytes. El motor no procesa ni entiende la sintaxis interna de un JSON guardado ahí.
6	B	Al no tener índices internos sobre el contenido del valor, la única forma eficiente (O(1)) de extraer la información es proveyendo la clave exacta.
7	B	A diferencia de Clave-Valor, un Document Store interpreta la estructura del documento (JSON/BSON), permitiendo indexar y consultar campos anidados individuales.
8	C	La filosofía Schemaless permite polimorfismo de datos: múltiples documentos con diferentes atributos pueden coexistir en la misma colección.
9	B	En NoSQL de documentos, la ausencia de un atributo simplemente significa que el campo no se escribe en el JSON, evitando el desperdicio de espacio y la rigidez del NULL de SQL.
10	B	Las bases de datos de grafos están optimizadas matemáticamente para recorrer redes de datos interconectados sin sufrir la penalización de rendimiento de los múltiples JOINs en SQL.
11	C	Los Nodos representan las entidades u objetos del dominio, y los Bordes (o relaciones) representan las conexiones dirigidas con propiedades entre ellos.
12	B	El borde (Edge) almacena el tipo de relación y dirección, permitiendo al motor de grafos "caminar" de un nodo a otro de forma nativa.
13	C	Para sistemas transaccionales críticos (OLTP) donde se requiere cumplimiento estricto de propiedades ACID (Consistencia y Seguridad) y estructuras fijas, SQL es el estándar industrial.
14	A	Para arquitecturas de almacenamiento en caché de alta concurrencia y baja latencia que operan por ID único, Clave-Valor en memoria (como Redis) es la opción ideal.
15	B	Los problemas de análisis de redes, recomendaciones jerárquicas y detección de fraudes dependen de encontrar patrones en las relaciones, lo cual es el caso de uso nativo de las bases de datos de Grafos.