``` markdown
<pre>
 ____  _            _ _            
|  _ \(_)_ __   ___| (_)_ __   ___ 
| |_) | | '_ \ / _ \ | | '_ \ / _ \
|  __/| | |_) |  __/ | | | | |  __/
|_|   |_| .__/ \___|_|_|_| |_|\___|
        |_|                        
</pre>

## QUE ES UN PIPELINE DE DATOS : 

un pipe-line de datos o tuberia de datos su unico trabajo es mover informacion de punto a a punto b aplicadoles el codigo necesario para tranfromarlos o limpiarlos 

## LOS 3 PASOS DE UN PIPELINE (ETL)

    * EXTRAER 
    * TRANSFROMAR 
    * CARGAR 

UN PIPELINE  **es un proceso hecho codigo y automatizado** : 

    * Lotes (Batch) :       el processo se despierta a una hora en especifico y se vuelve a apagar 
    * Tiempo Real (Streming) : la tuberia siempre esta abierta cunado el usuario agrega infromacion esta pasas por el pipeline 

## EN EL MUNDO DE AWS QUIEN CONSTRUYE LAS TUBERIAS (PIPELINES)

    es una combinacion de varias tecnologias : 

        * El motor del pipeline (El código que transforma): AWS Glue (usando scripts de Python/PySpark) o Amazon EMR
        * El operador (El que abre y cierra las llaves): AWS Step Functions o Amazon MWAA (Airflow). Estos servicios se encargan de decir: "Primero ejecuta el código A, si termina bien, ejecuta el código B".