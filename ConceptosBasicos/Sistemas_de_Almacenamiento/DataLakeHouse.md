
<pre>
 ____        _              _          _        _   _                      
|  _ \  __ _| |_ __ _      | |    __ _| | _____| | | | ___  _   _ ___  ___ 
| | | |/ _` | __/ _` |_____| |   / _` | |/ / _ \ |_| |/ _ \| | | / __|/ _ \
| |_| | (_| | || (_| |_____| |__| (_| |   <  __/  _  | (_) | |_| \__ \  __/
|____/ \__,_|\__\__,_|     |_____\__,_|_|\_\___|_| |_|\___/ \__,_|___/\___|
                                                                           
</pre>

es una arquitectura moderna que nos da los precios baratos algunas de sus mejoras caracteristicas son : 

    * flexibilidad y el almacenamiento de un dataLake 
    * orden y limpieza de un data where house 

## ventajas 

## esquema cunado lo necestias (schema enforcement) : 
    
    * se pueden meter datos crudos como un dato-lake pero se peude crear una carptea especificamente para un reportes oficiales una ** capa intermedia ** se activara el schema on write , y se comportara como datos de un data where house 

    * transacciones ACID : si tratamos de gaurdas un archivo grande y se va la luz el archivo entra corrcupto con acid se borra el proceso que lleve 

    * time travel : como git un controlador de versiones de los datos 

## la capa intermedia 

    la capa intermedia que indica que un directorio sera un data where house es pomedio de software y se ocupan : 

        * delta lake 
        * apache icerberg 