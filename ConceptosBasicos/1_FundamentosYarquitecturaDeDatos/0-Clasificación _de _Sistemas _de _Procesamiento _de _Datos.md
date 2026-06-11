
## Clasificación de Sistemas de Procesamiento de Datos.

En la informatica y las bases de datos exosten dos grandes reinos , __todo software en el mundo se divide en OLTP y OLAP__ 

## OLTP (online transaction processing)

proceso que esta __en vivo__ que da la cara al usuario o al negocio

### Objetivo 

es registrar operaciones segundo a segundo de forma ultra rapida sin que el sistema se caiga 

## para que sirve ?? 
para insertar actualizar o borrar registros individuales muy rapido 
## El tipo de consultas 
son micro consultas Ejemplo : de un cajero sacamos 10 pesos o agregamos 10 pesos 
## prioridad 
velocidad de escritura , y que no se dupliquen la infomracion (muy normalizada)
## El usuario 
el cliente de la app , el cajero , el repartidor 

### OLAP (online analitycal processing)
aqui es donde le damos sentido ala informacion del OLTP ya que se junto un lago de informacion mediante un tuberia (pipeline) la mandamos al OLAP que aqui es donde el negocio hace predicciones o formulas con los datos 

## para que sirve 
para interrogar ala historia del negocio para tomar deciciones no necesitamos un dato si no los datos de 5 años para analizarlos tomar deciciones etc 

## que tipo de consultas 
son macro consultas osea tomamos todo el historico del negocio 

## prioridad 
velocidad de lectura masiva 

## usuario 
el director de la empresa cientificos de datos y analistas de negocio 


[ REINO OLTP ]                 [ PIPELINE ]                 [ REINO OLAP ]
┌────────────────────┐        ┌───────────────────┐        ┌────────────────────┐
│ Bases de Datos     │        │    Proceso ETL    │        │   Almacenamiento   │
│ Transaccionales    │ ─────> │  (Extract, Load,  │ ─────> │     Analítico      │
│ (MySQL, Postgres)  │        │    Transform)     │        │   (Data Warehouse) │
└────────────────────┘        └───────────────────┘        └────────────────────┘
  Registra las compras         Mueve y limpia los datos       Contiene el Modelo
  segundo a segundo.           para que no pesen.             Dimensional (Estrella)
                                                              para predecir el futuro.