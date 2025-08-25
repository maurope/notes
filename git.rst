
COMANDOS GIT
---------

Crear un fichero::

	touch hellogit.py

Iniciar git donde nos encontramos::

	git init

Cambiar el nombre master por main::

	git branch -m main

Agregar el archivo hellogit.py::

	git add hellogit.py

Mostrar el estado de los ficheros::

	git status

Agregar los ficheros pendientes::

	git add .

Generar un comentario para guardar::

	git commit

Dejar un comentario::

	git commit -m 'Primer commit'

Mostrar los commits y su información::

	git log

Moverse a un commit en específico::

	git checkout nombre

Resetear las versiones::

	git reset

Hacer un gráfico::

	git log --graph

