``` markdown
<pre>
 ____        _           __        ___                         _   _       
|  _ \  __ _| |_ __ _    \ \      / / |__   ___ _ __ ___      | | | | ___  
| | | |/ _` | __/ _` |____\ \ /\ / /| '_ \ / _ \ '__/ _ \_____| |_| |/ _ \ 
| |_| | (_| | || (_| |_____\ V  V / | | | |  __/ | |  __/_____|  _  | (_) |
|____/ \__,_|\__\__,_|      \_/\_/  |_| |_|\___|_|  \___|     |_| |_|\___/ 
                                                                           
                
 _   _ ___  ___ 
| | | / __|/ _ \
| |_| \__ \  __/
 \__,_|___/\___|

</pre>

## QUE ES UN DATA WHERE HOUSE 

### solo datos limpios y estructurados 
### en un data Where House NO SE PUEDEN ALMACENEAR DATOS SEMI/NO ESTRUCTURADOS 

UN DWH O ALMACEN DE DATOS es lo contratio a un data lake mientras que en el datalake tenemos los datos sin estrutura o en su estado puro en el dwh tiene que pasar por un proceso de **ETL** antes de entrar 

## ETL 

    * Extract (extraer)             -> se sacan de apps o dataLake 
    * Transform (Transformar)       -> se limpian : (eli . duplicados , formato fechas , se estructuran )
    * Load (cargar )                -> se almacenan en el DWH 

## EL MAXIMO REFERENTE EN AWS ES -> AWS REDSHIFT 

es una base de datos masiva que utiliza la tecnologia **almacenamiento columnar**
(guarda los datos en columnas en lugar de filas)

## SCHEMA-ON-WRITE 

Antes de que el dato entre debe de tener un schema definido osea tablas filas y columnas 