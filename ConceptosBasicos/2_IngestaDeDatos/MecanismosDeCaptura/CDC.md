

# CDC (Change data capture)

el _CDC_ es una tecnica de la ingeniria de datos donde movmos informacion de punto a a punto b pero _solamente la infromacion __nueva__ !_ 

## ANALOGIA 

un estudiante cuando falta un dia de clases , pide a su amigo la libreta de matematicas y sacarles fotocopias , en ves de fotocopiar todo el ucaderno de matematicas con infromacion desde que inicio el curso simplemente toma la infomacion del dia que falto 

## ***Como Funciona el CDC***

en las empresas existen bases de __datos trancsaccionales__ (_OLTP_) donde los clientes estan comprando todo el tiempo nosotros necesitramos llevar esa infomacion a nuestro _data lake_ o a nuestro _data Where house_ 

el cdc se encarga de de vigilar esa base de datos en el mismo segundo que ocurre el sacado de informacion el _CDC_ genera un reporte con 3 eventos 

### EVENTOS CDC :

_1 Insert_ : se creo un nuevo registro (el cdc toma ese registro y lo manda al destino) 

_2 update_ : luis cambio su domicilio (el cdc solo manda el aviso del cambio)

_3 delete_ : Luis cancelo su cuenta (el cdc avisa que se debe de borrar o poner en incativo)

### __Cuestionario__

¡Listo! Vamos a poner a prueba el concepto de **CDC (Change Data Capture)** con este cuestionario de 5 preguntas de opción múltiple. Las preguntas están diseñadas como escenarios reales a los que te vas a enfrentar como ingeniero de datos.

Lee con atención cada caso:

---

### Pregunta 1: El mecanismo interno del CDC

Estás configurando una herramienta de CDC para replicar los datos de una base de datos transaccional hacia tu Data Lakehouse. El administrador de la base de datos (DBA) te pregunta si tu proceso va a saturar el servidor lanzando consultas de tipo `SELECT * FROM tablas` a cada rato.

¿Cuál es la respuesta técnicamente correcta para tranquilizar al DBA?

* A) Sí, el CDC bloquea las tablas cada 5 minutos para poder leer los datos nuevos.
* B) No, el CDC no toca las tablas operativas; se limita a leer de reojo el archivo Log de Transacciones (WAL) de la base de datos.
* C) No, porque el CDC convierte automáticamente la base de datos origen en un archivo CSV estático.
* D) Sí, pero el impacto se reduce porque el CDC borra los datos viejos de producción conforme los va leyendo.

---

### Pregunta 2: Eficiencia en la transferencia

Una base de datos de producción pesa **2 Terabytes**. Durante las últimas 2 horas, los usuarios solo han registrado 10 compras nuevas y han actualizado 2 direcciones de envío.

Si tienes activado un sistema de **CDC**, ¿qué información se va a transferir a través de la red hacia tu destino analítico?

* A) El archivo completo de 2 Terabytes para asegurar que no se pierda nada.
* B) Únicamente los datos correspondientes a las 10 compras nuevas y las 2 actualizaciones.
* C) Una copia de la estructura o esquema de las tablas, pero sin ningún dato adentro.
* D) Las 10 compras nuevas, pero las actualizaciones de direcciones se ignoran por completo.

---

### Pregunta 3: Los tres tipos de eventos esenciales

El software de CDC está vigilando la tabla de `Usuarios`. En un lapso de un minuto, ocurren tres acciones: Carlos se registra en la app, Ana cambia su número de teléfono, y Pedro elimina su cuenta.

¿Qué combinación de eventos registrará y enviará el CDC al Data Lake?

* A) BATCH, STREAMING y ARCHIVE.
* B) READ, WRITE y UPDATE.
* C) INSERT, UPDATE y DELETE.
* D) EXTRACT, TRANSFORM y LOAD.

---

### Pregunta 4: La alternativa ineficiente (Enfoque Antiguo)

Antes de que existiera el CDC, ¿cuál era la práctica común (e ineficiente) que usaban los ingenieros de datos para actualizar un Data Warehouse por las noches?

* A) Hacer un volcado o copia completa de toda la base de datos (Full Dump), borrando y reescribiendo todo el destino cada día.
* B) Apagar la aplicación web durante todo el día para que nadie pudiera meter datos nuevos.
* C) Contratar analistas para que transcribieran los datos manualmente fila por fila.
* D) Aplicar una política de inmutabilidad que prohibiera a los usuarios hacer cambios en sus perfiles.

---

### Pregunta 5: Ventaja competitiva para el negocio

El director de operaciones de una empresa de logística necesita un tablero de control que muestre la ubicación y el estado de los paquetes casi al instante (con pocos segundos de retraso) respecto a los sistemas de los repartidores.

¿Por qué el **CDC** es la estrategia ideal para resolver esta necesidad de negocio?

* A) Porque obliga a los repartidores a usar bases de datos tipo Schema-on-Read.
* B) Porque permite tener los sistemas analíticos actualizados en tiempo real o cuasi-tiempo real al capturar el dato en cuanto el cambio ocurre en producción.
* C) Porque destruye de forma automática los registros de los paquetes que ya fueron entregados para ahorrar espacio.
* D) Porque transforma los datos de geolocalización en archivos de audio de alta fidelidad.

