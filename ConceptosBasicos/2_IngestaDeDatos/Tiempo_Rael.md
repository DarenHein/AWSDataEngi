
### PROCESAMIENTO EN TIEMPO REAL (Streaming Processing)

Es lo contrario a el _procesamiento por lotes_ en este todo el proceso se hace en milisegundos 

El dato se : procesa , limpia y transforma desde que nace de forma individual 

### Caracteristicas de un Streming Pipeline 

1- _El origin continuo_
2- _Datos en movimiento_
3- _Baja Latencia_

### Cuestionario 

### Pregunta 1: La disponibilidad del pipeline

Estás diseñando la arquitectura para una aplicación de entrega de comida a domicilio (tipo Uber Eats o Rappi). El pipeline debe recibir constantemente las coordenadas GPS de miles de repartidores para actualizar el mapa de los clientes en vivo.

¿Cómo debe comportarse la ejecución de este pipeline de ingeniería de datos?

* A) Debe programarse para ejecutarse cada hora en punto mediante un cron-job.
* B) Debe mantenerse encendido las 24 horas del día, los 7 días de la semana (siempre activo).
* C) Debe encenderse únicamente cuando el volumen de coordenadas supere los 100 Gigabytes.
* D) Debe ejecutarse en la madrugada para no saturar los servidores del mapa.

---

### Pregunta 2: Tipo de datos y movimiento

Una plataforma de inversiones en la bolsa de valores genera alertas instantáneas cuando el precio de una acción sube o baja drásticamente. El pipeline procesa los precios en el milisegundo exacto en que ocurren y los datos fluyen como un río sin fin.

¿Con qué tipo de datos trabaja este pipeline de streaming?

* A) Datos estáticos y congelados del mes anterior.
* B) Fotografías históricas guardadas en cintas de archivado.
* C) Datos en movimiento (Data in motion) de volumen infinito y continuo.
* D) Bloques fijos de texto estructurado invariables.

---

### Pregunta 3: Requerimiento de latencia

Trabajas para una empresa de ciberseguridad. Te piden construir un pipeline que analice los intentos de inicio de sesión de los usuarios. Si un bot intenta atacar un servidor realizando 500 inicios de sesión falsos en 3 segundos, el sistema debe bloquear la dirección IP inmediatamente para evitar el hackeo.

¿Qué nivel de latencia exige este escenario de negocio?

* A) Alta latencia (el bloqueo puede esperar un par de horas).
* B) Latencia extendida por lotes quincenales.
* C) Baja latencia (milisegundos o pocos segundos para reaccionar al vuelo).
* D) Latencia acumulada asíncrona.

---

### Pregunta 4: Identificando el caso de Streaming

De las siguientes necesidades de una organización, ¿cuál de ellas **SÍ** requiere una solución basada en **Streaming / Tiempo Real**?

* A) Generar el reporte de pérdidas y ganancias que los contadores revisan al final de cada trimestre.
* B) Calcular el promedio de calificaciones de los estudiantes de una universidad una vez que terminaron los exámenes finales.
* C) Monitorear la temperatura de un reactor en una planta química para activar una alarma visual si supera los 180°C.
* D) Respaldar todos los archivos PDF de contratos de la empresa en una bodega digital una vez al año.

---

### Pregunta 5: La analogía multimedia

Si conectamos los conceptos de ingeniería de datos con la forma en que consumimos entretenimiento, ¿cuál de las siguientes opciones describe perfectamente un proceso de **Streaming**?

* A) Descargar una película completa de 4GB en el disco duro de tu computadora por la noche para verla el fin de semana.
* B) Ver una transmisión de un partido de fútbol en vivo por internet donde el video te llega en un flujo continuo de fragmentos y lo ves al instante.
* C) Comprar una colección de películas en formato Blu-ray físico y guardarlas ordenadamente en un estante de la sala.
* D) Imprimir las portadas de tus series favoritas en papel para armar un catálogo visual en tu escritorio.
