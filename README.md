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

