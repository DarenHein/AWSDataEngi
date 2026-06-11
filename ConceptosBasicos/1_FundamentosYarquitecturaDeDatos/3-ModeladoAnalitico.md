
### MODELADO ANALITICO 

Imagínate que estamos en los años 90. Ya sacamos los datos de las bases de datos operativas de producción (OLTP) mediante un pipeline y ahora los tenemos en nuestro Data Warehouse (Almacén de Datos). El objetivo de este lugar no es registrar compras segundo a segundo, sino hacer consultas analíticas gigantescas muy rápido (OLAP)

Para que estas consultas no tarden horas, el científico de datos o el analista de BI necesitan que los datos estén ordenados bajo un modelo específico. Aquí es donde entran los dos reyes del modelado analítico creados por Ralph Kimball: el Esquema en Estrella (Star Schema) y el Esquema en Copo de Nieve (Snowflake Schema).

ANTES DE VER LOS ESQUEMAS DEBEMOS COMPRENDER DOS CONCEPTOS : 

    * TABLAS DE HECHOS (FACT TABLES)
    * TABLAS DE DIMENCIONES 


NOTA MENTAL : EL MODELADO ANALITICO ES COMO QUEDARAN EL DISEÑO O PLANOS DE LAS TABLAS EN EL OLAP 

## Tablas de hechos 

son tablas que guardan historial numerico cuantificable resultado de un evento 
es la tabla que guarda cuando : __"pasa algo en la empresa"__ 

__ANALOGIA__ 

imgaminemos que tenemos una cafeteria cada vez que llega un cliente pide un cafe y paga se genero un __evento__ (o __hecho__), nuestra tabla de hechos es la lista enorme donde se van acumulando esos eventos uno tras otro hacia abajo 

__Una tabla de hechos se compone unicamente de dos cosas__

* Metricas(numeros): 

son datos nuemericos cuantitativos que se pueden realizar operaciones con ellos 
Ejemplo :

    * CANTIDAD DE CAFES VENDIDOS 
    * MONTO TOTAL PAGADO EN DINERO
    * IMPUESTOS COBRADOS 
    * DESCUENTO APLICADO 

* LAS LLAVES (LOS IDES DEL CONTEXTO) 

una tabla de hechos __NO__ guarda texto (no escribe el nombre del usuario) , si no numeros de identificacion que sirven como flechas para conectar con las tablas de dimenciones 

    * id_cliente
    * id_producto
    * id_sucursal 
    * id_tiempo 


## RESUMEN 

la tabla de hechos es el centro de tu modelo analitico por que guarda la historia __numerica__ de lo que ocurrio 


## TABLAS DE DIMENCIONES 

si las tablas de hechos guardan el historical numerico las __tablas de dimenciones__ guardan todo el contexto los detalles y la historia que complementan la tabla de hechos 

responde estas preguntas : quien ?? , que ?? , donde ?? , y cuando ?? 

# DE QUE SE COMPONE UNA TABLA DE DIMENCIONES 

literial es un catalogo de infomacion descriptiva se compone de dos cosas 

* Llave primaria : 
es el numero o flecha que conecta la __tabla de dimenciones__ con la __tabla de hechos__ es el punte 

* Los Atributos 
aqui es donde va todo el texto descriptivo del negocio son , palabras , textos o fechas que nosotros como DEngenering ocupamos para Ordenar , filtrar , agrupar datos 

### DATO EXTRA 

tablas de hechos : cortas en su shcema pero con millones de datos 
tablas de dimenciones : largas en su schema pero con pocos datos 

![Ejemplo]("IMG/IMG.png")