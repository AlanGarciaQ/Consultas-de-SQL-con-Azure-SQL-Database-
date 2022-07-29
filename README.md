# Consultas de SQL con Azure SQL Database 
**Objetivo:** Realizar una consulta de base de datos utilizando el recurso de SQL Database de Azure.   

![](/imagenes/virtual%20machine.png)

**Requisitos**
- Cuenta de Azure con una suscripción activa
- Equipo de cómputo con sistema operativo: Windows, Linux o MacOs.

**Pasos**  
Se inicia sesión en Portal.Azure.com  
Consultamos el siguiente [repositorio](github.com/josejesusguzman/acordeon-az900-innovaccion/blob/main/res/consultas-sql.md)(Dar clic en este enlace) que el Sherpa Jesús nos compartió, para hacer esta práctica y copiamos el siguiente comando que se observa en la imagen.  
![Imagen 1](/imagenes/Imagen1.png)

En Azure damos clic en el botón de Cloud Shell, el icono que está al lado de la barra de búsqueda. Si nos aparece que no tenemos un almacenamiento montado seleccionaremos la opción de crear.  
Se nos abrirá una ventana de comandos, en la parte superior izquierda de esa ventana, seleccionaremos la opción de Bash (Este sería el SSH), en la línea de comandos pegaremos el comando que copiamos anteriormente y daremos enter.  
Este comando lo que va a hacer es crear un repositorio dentro de Azure.  
![](/imagenes/Imagen2.png)

Ahora del repositorio que estamos consultando copiamos los siguientes comandos que se observan en la siguiente imagen. El primer comando es para acceder a una carpeta, el segundo son instrucciones para crear una base de datos SQL en Azure.  
![](/imagenes/Imagen3.png)  
![](/imagenes/Imagen4.png)

Una vez creada nuestra base de datos buscaremos dentro de nuestros grupos de recursos la base de datos dentro de uno de estos, ya que el comando anterior crea la base de datos en el último grupo de recursos que hicimos y seleccionamos el recurso de base de datos SQL.  
![](/imagenes/Imagen5.png)

En el menú de la parte de arriba le damos clic en la opción de establecer firewall del servidor.  
Buscamos la opción de agregar la dirección ipv4 del cliente y la seleccionamos.  
Damos clic en guardar.
![](/imagenes/Imagen6.png)

Regresamos a el recurso de base de datos SQL.  
En el menú de la parte de la izquierda le damos clic en la opción de editor de consultas.  
Los datos para iniciar sesión se encuentran en el acordeón un poco más debajo de los comandos que copiamos anteriormente. Esos los pegamos en sus respectivos lugares e iniciamos sesión.  
![](/imagenes/Imagen7.png)  
![](/imagenes/Imagen8.png)

Realizaremos una consulta con el siguiente código: SELECT * FROM (nombre de la tabla que queremos consultar. Por ejemplo, SELECT * FROM Inventory y le damos en ejecutar y nos mostrara todos los datos que contiene esa tabla.  
![](/imagenes/Imagen9.png)

Si queremos agregar un elemento a la fila necesitamos utilizar el siguiente comando: INSERT INTO nombre de la tabla (nombre de la columna 1, nombre de la columna 2 y así dependiendo de cuentas columnas tengamos) valúes(datos de la primer columna, datos de la segunda columna, datos de la demás columnas que falten); por ejemplo, si en inventory queremos agregar una fila seria así, INSERT INTO Inventory (Id, Inventory.Name, Stock) values (7, ‘Watermelon’,500); y le damos en ejecutar. Nota: Para poder poner el valor Name, antes tuvimos que poner el nombre de la tabla, así Inventory.Name, esto para hacer referencia a que queremos agregar este valor, ya que la palabra Name es una palabra reservada y no nos dejaría hacer la inserción por esto. Nota 2: En los datos de tipo String como Name necesitamos que vallan entre comillas simples el valor que queremos agregar.  
![](/imagenes/Imagen10.png)

