

COMANDOS DOCKER 
---------


Instalar Docker Desktop y ejecutarlo para usarlo.
Cuando estemos en la línea de comandos, luego abrimos la terminal y ponemos:

Para descargar la última versión de docker::

	docker pull node

Para mostrar imágenes y su información::

	docker images

Descargar específicamente la versión 18::

	docer pull node:18

Mostrar las dos imágenes con etiquetas diferentes::

	docker images

Descargar mysql::

	docker pull mysql

Si aparece un error usar::

	docker pull --platform linux/x86_64 mysql

Eliminar la versión 18 de node::

	docker image rm node=18

Para hacer nuestra propia imagen de contendor, hacemos lo siguiente:
Descargar una imagen de mongo::

	docker pull mongo

Crear el contenedor con nombre mongo::

	docker create mongo

La forma larga de hacerlo es::

	docker container create mongo

En id ponemos la línea de números y letras que obtuvimos cuando creamos mongo::

	docker start id

Para solicitar información del contenedor y su estado y hasta su puerto::

	docker ps

Detener el contenedor, podemos usar el id abreviado que nos aparece cuando usamos docker ps, si volvemos a correr docker ps no nos va a aparecer porque no está corriendo::

	docker stop id

Si queremos verlo debemos usar::
	
	docker ps -a

Eliminar el contenedor utilizando el nombre que haía sido asignado y que podíamos ver con 'ps'::

	docker rm name

Crea un contenedor con nombre monguito::

	docker create --name monguito mongo

	docker stop monguito
	docker rm monguito

Crear el contenedor con un puerto específico::

	docker create -p27017:27017

Mostrar los logs que emite nuestro contenedor::

	docker logs monguito

	docker rm monguito
	docker image

El comando run, busca la imagen, la instala, crea un nuevo contenedor y corre la imagen. Todo en un mismo comando.

	docker run mongo

Para hacer lo mismo pero sin mostrar los logs y dovolviendonos a la línea de comandos::

	docker run -d mongo

Todos los comandos previos se pueden apolicar a 'run', ej::

	docker run --name monguito -p27017:27017 -d mongo
	docker stop monguito
	docker rm monguito

NO DEJAR A DOCKER PONER EL PUERTO QUE QUIERA,  poner el que nosotros queremos.

