# Ejercicio 1

Partiendo del archivo “Datos_Ejemplos_ETL.csv” que está en un bucket de Amazon S3, el objetivo es realizar un proceso ETL para transformar los datos y cargarlos en un nuevo archivo. 

Utiliza Python para completar las tareas descritas a continuación. Si es necesario, utiliza la biblioteca boto3 para interactuar con Amazon S3. 

Tareas: 
1. Descarga el archivo Datos_Ejemplos_ETL.csv desde Amazon S3. 
2. Realiza una transformación en los datos. En este caso, supongamos que deseas cambiar todas las letras en el archivo a mayúsculas y eliminar las filas duplicadas.
3. Guarda los datos transformados en un nuevo archivo llamado transformed_data.csv.
4. Sube el archivo transformed_data.csv de vuelta a Amazon S3.
5. Ordenar las respuestas de forma descendente a partir de la fecha. 

Partiendo de la base identifica las siguientes características:

 1. ¿Cuántos usuarios tienen más de 5 cuentas abiertas?
 2. ¿Cuántos usuarios tienen un score arriba de 650?
 3. ¿Cuántos usuarios tuvieron una respuesta en el mes de noviembre?
 4. ¿Cuántos usuarios tienen por lo menos 2 tarjeta de crédito y sin saldo actual?


# Respuesta

Se debe de tener un archivo llamado **pipeline.conf** con la siguiente estructura:

    [aws_boto_crentials]
    access_key = XXXXXXXXXXXXXXX
    secret_key = XXXXXXXXXXXXXXX

donde se deben colocar las credenciales correspondientes para hacer la interaccion con S3

dentro del archivo main.py hay que modificar el nombre del bucket y el archivo segun corresponda

    # Nombre del bucket donde esta el archivo
    bucket_name = "nombre del bucket"
    
    # Nombre del archivo a descargar
    file_key = "Datos_Ejemplos_ETL.csv"

Instala las dependencias con:

    pip install -r requirements.txt
 
Ejecuta el archivo main.py, se creara una carpeta logs en la cual entregara la respuesta a las preguntas


## Respuestas a las preguntas planteadas:

Hay 15 usuarios únicos que tienen más de 5 cuentas abiertas
Hay 33 usuarios únicos que tienen un score en el buró de crédito mayor a 650.
Hay 2 usuarios únicos que tuvieron una respuesta en el mes de noviembre..
Hay 18 usuarios únicos que tienen por lo menos 2 tarjetas de crédito y no tienen saldo.
