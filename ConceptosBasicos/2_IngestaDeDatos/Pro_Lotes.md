
### PROCESO POR LOTES (Batch Processing)

Es una forma de procesar informacion donde los datos no se procesan uno por uno si no que se acumulan en grupos (lotes) y esos se procesan todos juntos en un momento en especifico 

** ANALOGIA **

_es como lavar la ropa sucia no lavamos solo un calcetin si no que espereamos que se junte bastante ropa y la lavamos un viernes en la noche_

__Como funciona el flujo de un Pipeline Batch__

    * __Disparador por tiempo o Volumen__
    * __Datos Historicos__
    * __Alta Latencia__

### CUESTIONARIO 

### Pregunta 1: El disparador del proceso

Una empresa de e-commerce tiene un pipeline que analiza el comportamiento de los usuarios. El sistema está configurado para que todos los días a las **3:00 AM** el código se ejecute de forma automática, lea los archivos de texto acumulados en el Data Lake y genere un resumen de métricas.

¿A qué concepto del funcionamiento Batch hace referencia esta configuración de las 3:00 AM?

* A) Alta latencia de entrega.
* B) Disparador por tiempo (Scheduled Trigger).
* C) Procesamiento en tiempo real por ráfagas.
* D) Inmutabilidad de la base de datos de producción.

---

### Pregunta 2: El estado de los datos

Un pipeline Batch se enciende para calcular las comisiones de los vendedores utilizando los registros de ventas del mes pasado. Mientras el código está sumando los montos, un cliente realiza una nueva compra en la aplicación web. El pipeline ignora por completo esta nueva compra y termina su ejecución con éxito.

¿Por qué el pipeline ignoró este nuevo registro?

* A) Porque los procesos Batch trabajan con datos estáticos (una "fotografía" fija del pasado).
* B) Porque el sistema detectó un error de esquema y rechazó el dato.
* C) Porque las compras web usan un "Schema-on-Read" que el pipeline no puede descifrar.
* D) Porque el pipeline sufrió una caída de latencia a la mitad del proceso.

---

### Pregunta 3: El concepto de Latencia

El departamento de Finanzas te pide diseñar un reporte que les muestre la salud financiera de la empresa de forma mensual. Te comentan que no les importa si los datos tardan 6 u 8 horas en procesarse durante la madrugada del primer día del mes, siempre y cuando los números finales sean exactos.

¿Qué característica de la latencia en procesos Batch se alinea perfectamente con este requerimiento?

* A) Latencia cero (Zero latency).
* B) Baja latencia (Baja espera).
* C) Alta latencia (Alta espera aceptable para el negocio).
* D) Latencia fluctuante en milisegundos.

---

### Pregunta 4: Identificando el escenario correcto

De los siguientes escenarios de una empresa, ¿cuál debería resolverse obligatoriamente con **Procesamiento Batch** en lugar de Streaming (tiempo real)?

* A) Un sistema de seguridad bancaria que debe bloquear una tarjeta de crédito en menos de 2 segundos si detecta un patrón de fraude.
* B) Un algoritmo que calcula el pago de la nómina y utilidades de 5,000 empleados al final de la quincena.
* C) Una aplicación de mapas que necesita actualizar el tráfico en vivo cada vez que un conductor avanza una cuadra.
* D) Un chat de soporte técnico que debe enviar alertas instantáneas cuando un cliente escribe la palabra "queja".






