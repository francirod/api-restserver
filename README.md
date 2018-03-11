# api-restserver
Primeros pasos con una API REST con codeigniter

En este proyecto el objetivo es ver como funciona una API REST en codeigniter.
Para ello partimos de la base de https://github.com/chriskacerguis/codeigniter-restserver.

Con unas modificaciones he logrado que la API funcione a mi gusto.

Para probarla debemos tener instalado:
- Apache
- Php
- Mysql
- Curl
 y por suspuesto las librerias y modulos correspondientes como:
 libapache2-mod-php, curl-php y php-mysql
 
 Importante, debemos crear una base de datos de esta forma:
 
 CREATE DATABASE boxeo;
 USE boxeo;
 CREATE TABLE boxeo (id CHAR(1),nombre VARCHAR(20),descripcion VARCHAR(20));
 
 Y si quisieramos agregar algun dato:
 INSERT INTO boxeo (id,nombre,descripcion) VALUES (id,"nombre","descripcion");
 
 Ahora si quisieramos trabajar con CURL, podemos usar estos comandos:
 
 Obtener datos: - $ curl -X GET -H 'Content-Type:application/json' localhost/codeigniter/index.php/boxeo
 
 Enviar datos POST: - $ curl -X POST -H 'Content-Type:application/json' -d '{"nombre":"nombre","descripcion:"descripcion"}' localhost/codeigniter/index.php/boxeo
 
 Actualizar: $ curl -X PUT -H 'Content-Type:application/json' -d '{"nombre":"nombre","descripcion:"descripcion"}' localhost/codeigniter/index.php/boxeo
 
 Borrar datos: $ curl -X DELETE  -H 'Content-Type:application/json' localhost/codeigniter/index.php/boxeo/id
 
 Por ultimo para acceder via web:
 localhost/codeigniter/index.php/boxeo
 
 Y si queremos ver un dato concreto:
localhost/codeigniter/index.php/boxeo/id
 
