
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
