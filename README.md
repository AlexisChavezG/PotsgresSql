# PotsgresSql
Instalación y creación de tabla vacía en Postgres

Se descarga el instalador de la página de postgres dependiendo del sistema operativo
https://www.postgresql.org/download/

Instalador
<img width="300" alt="Captura de Pantalla 2022-06-13 a la(s) 19 51 23" src="https://user-images.githubusercontent.com/99348169/173470793-061a045d-8f34-4ca1-a02e-067f0ab2ae3c.png">

Al instalar se escribe una contraseña para poder acceder a nuestro servidor de base de datos.

Una vez instalado desde nuestra SQL Shell podemos acceder a nuestro servidor

<img width="400" alt="Captura de Pantalla 2022-06-13 a la(s) 19 46 49" src="https://user-images.githubusercontent.com/99348169/173470925-86ed95ea-8c4d-4614-8642-1a86d99d2d60.png">


# Comando \l  
El comando `\l` nos sirve para listar las bases de datos que tenemos en nuestro servidor  

<img width="400" alt="Captura de Pantalla 2022-06-13 a la(s) 19 57 27 1" src="https://user-images.githubusercontent.com/99348169/173471313-e06d94a8-19f2-47ed-950a-4c62faa4ce29.png">

# Creación de una base de datos  
Se procede a crear una base de datos denominada **launchx_nodejs** para esto ejecutaremos el comando  
`create database lauchx_nodejs;`  el punto y coma es muy importante para poder terminar la instrucción  

<img width="601" alt="Captura de Pantalla 2022-06-13 a la(s) 20 03 02" src="https://user-images.githubusercontent.com/99348169/173471848-653935c7-361e-44f1-ad9a-4c56a1a9e333.png">

Vuelvo a ejecutar el comando `\l` se muestra la nueva base de datos recién creada

<img width="575" alt="Captura de Pantalla 2022-06-13 a la(s) 20 04 15" src="https://user-images.githubusercontent.com/99348169/173471989-1e11b621-8cc5-416e-9107-568799d1840a.png">  

Seleccionamos la base lauchx_nodejs recién creada con el comando  
`\c launchx_nodejs;`  

<img width="577" alt="Captura de Pantalla 2022-06-13 a la(s) 20 10 33" src="https://user-images.githubusercontent.com/99348169/173472488-f6b41198-73c4-4135-823c-694ed48a5930.png">

Con este comando sabemos que podemos trabajar sobre la base que estamos seleccionando  

# Uso del comando \dt  
Con el comnado `\dt` una vez que tenemos selecciona la base de datos podemos desplegar las tablas que contiene la base.  

<img width="579" alt="Captura de Pantalla 2022-06-13 a la(s) 20 11 36" src="https://user-images.githubusercontent.com/99348169/173472554-dba1f1cd-2a7e-4d93-8eb9-7c1a50f99b2c.png">   
  
En el ejemplo anterior nos devuelve que la base de datos no contiene ningúna relación, esto es porque aún no tiene ninguna tabla  

# Crear una nueva tabla  
Para crear una nueva tabla dentro de la base de datos que ya tenemos selecciona es con el comando  

`CREATE TABLE explorers(id bigserial, username varchar(50));`  

el nombre de la tabla sera *explorers*  y que se encuentra entre parentesis son los campos que contendra nuestra tabla   

<img width="580" alt="Captura de Pantalla 2022-06-13 a la(s) 20 16 29" src="https://user-images.githubusercontent.com/99348169/173473008-42ca5f0f-4deb-4dfb-9398-a3d871c0ec63.png">  
Volviendo a ejecutar el comando `\dt` obtenemos la información    

<img width="574" alt="Captura de Pantalla 2022-06-13 a la(s) 20 17 25" src="https://user-images.githubusercontent.com/99348169/173473616-8a7ca467-0b95-4151-a8e6-936a683334e4.png">  

# Creando una nuevo registro
Las tablas almacenan registros para esto es necesario el comando  

`insert into explorers(id, username) values (1, 'Explorer1');`  

<img width="571" alt="Captura de Pantalla 2022-06-13 a la(s) 20 29 44" src="https://user-images.githubusercontent.com/99348169/173474263-56b2f2bc-f9b2-4484-8a51-4b96263c7218.png">

# Comando select  
El comando select se usa para seleccionar los registros de una tabla con el operador `*` nos devuelve todos los campos que tengan la tabla pero podemos seleccionar unicamente los campos que necesitemos  

<img width="563" alt="Captura de Pantalla 2022-06-13 a la(s) 20 34 02" src="https://user-images.githubusercontent.com/99348169/173474655-374ceb49-4792-4452-a3a1-a6ee10e829a3.png">

Ejemplo para selección de campos en especifico  

`select id from explorers`  

<img width="571" alt="Captura de Pantalla 2022-06-13 a la(s) 20 35 26" src="https://user-images.githubusercontent.com/99348169/173474806-e0333f53-96a6-44d2-864f-c7390f4f185a.png">

# Clausula WHERE

Con la clausula where podemos seleccionar un registro en especifico si nosotros difinimos el where debemos escribir que campos tomaremos de referencia en caso de no existir la clausula en el comando la tabla será afectada completa  

`select * from explorers where id = 1;`  

<img width="566" alt="Captura de Pantalla 2022-06-13 a la(s) 20 41 07" src="https://user-images.githubusercontent.com/99348169/173475422-adfa1293-80c5-457d-ac4c-45d8b7ca21b9.png">

# Editar registros
Existe el comando `update` que nos permite hacer actualizaciones sobre los registros de la tabla puede ser una actualización global en ese caso no llevara la clausula where o una actualización especifica  

<img width="573" alt="Captura de Pantalla 2022-06-13 a la(s) 20 44 13" src="https://user-images.githubusercontent.com/99348169/173475734-a904309f-36cd-4b1c-80a8-0041a5a0d4c7.png">

# Eliminar registros  
Para eliminar registros tenemos el comando `delete` al igual que el update es posible eliminar un registro espeficio o una tabla con todos sus registros con y sin el clausura `where`  

<img width="541" alt="Captura de Pantalla 2022-06-13 a la(s) 20 47 27" src="https://user-images.githubusercontent.com/99348169/173476098-8d149240-0189-46d7-b834-c274f670397b.png">

