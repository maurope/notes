

DOCKER COMMANDS
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