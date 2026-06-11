
### QUE ES LA IND DE DATOS 

La __ing de datos__ es la diciplina que se encarga de __diseñar , construir , y mantener las tuberias (pipeline)__ para que los datos crudos y sucios de una empresa se transformen en infomracion limpia confiable y rapida al usar 

### El camino del dato : Las 4 Etapas que dominamos 

## PASO 1 : LA INGESTA 

se generan datos en tieempo real (OLTP)
__nuestra chamba__ es tomar esos datos crudos de una base de datos sin tirar produccion

## PASO 2 : LA TRASNFORMACION 

LOS DATOS viene en mal estado sucios con duplicados las fechas mal etc 
mediante herramientas de programacion nuestro trabajo es limpiar esos datos (python,scala)

## PASO 3 : ALMACENAMIENTO 

necesiramos guardar los datos limpios que acabamos de limpiar 
ahora diseñamos un __data WhereHouse__ (almacen de datos) y desidicmos como almacenar los datos 
__esquema estrella__ o __Copo de Nieve__

## PASO 4 : EL CONSUMO 

el negocio decide ocupar dichos datos para EJEMPLO : 
entrenar modelos de Machine learning 
nuestra chamba es que cunado ellos necesiten esos datos los datos ya estan limpios y purificados 
