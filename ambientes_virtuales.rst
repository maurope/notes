
COMANDOS DE AMBIENTES VIRTUALES
------

Mostrar el album de librerías instalado::

	pip3 freeze

Instalar paquete para entornos virtuales::

	sudo apt install -y python3 -venv

Crear un ambiente en un directorio (env es el nombre que le damos)::

	python3 -m venv env

Activar el ambiente (cuando esta activo, muestra env en la consola)::

	source env/bin/activate

Salir del ambiente virtual::

	deactivate

Si corremos 'which' nos muestra que python3 y pip3 están lanzandose desde nuestro directorio. Si corremos pip freeze n nos mostrará nada porque no hay nada. Vamos a instalar por ejemplo Matplotlib::

	pip3 install matplotlib

Guardar todo lo instalado en un archivo txt para que otro usuario lo pueda ver::

	pip3 freeze > requirements.txt

Mostrar el contenido de este archivo::

	cat requirements.txt

Instalar el contenido de este archivo requirements.txt::

	pip3 install -r requirements.txt

Llamar librerías de otras partes::

	pip3 install request

Instalar librería para webserver::

	pip3 install fastapi

Librería para webserver::

	pip3 install "uvicorn[standard]"

Cuando ya estoy corriendo la API en la terminal, el reload hace que se recargue cada vez que genero un cambio::

	uvicorn main: ap --reload