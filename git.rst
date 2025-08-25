
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

	git log --graph --pretty=oneline

	git log --graph --decorate --all --oneline

Renombrar los comandos y hacerlos menos complejos. De esta forma solo se usa git y el alias::

	git config --global alias.tree 

Crear un fichero donde vamos a poner todo lo que no queramosque nos salga cuando hacemos git status. El ignore se crea en la raíz del proyecto y ahí ponemos todo lo que no queramos ver. Dentro de este archivo escribimos **/. nombre del archivo y así indicamos que archivo no será tomado en cuenta por git::

	touch .gitignore

Actualiza la misma rama en que estamos trabajando::

	git push origin head

Borrar todos los commits posteriores donde nos paremos. Para que funcione tenemos que poner el ID después de hard. Así el head será donde hicimos el hard::

	git reset --hard 

Muestra todo el historial así hayamos borrado con hard::

	git reflog


Poner nombre en minúscula y con _ por buenas prácticas. Se usa para guardar versiones::

	git tag nombre_del_tag

Mostrar solo los tags que hay en el master::

	git tag

Combinar los cambios en las diferentes ramas::

	git merge main

Cambiar de rama sin hacer commit, normalmentese hace commit de algo que funciona, sino funciona no debería hacerse commit::

	git stash

Fijar la url de github para nuestro repositorio (Esto lo extraemos del home del proyecto que creamos en github). Pulsamos SSH en la sección de Quick Set up y allí podemos encontrar la dirección::

	git remote set-url origin git@github.com:maurope/hello-git.git

Fijar el nombre de tu rama::

	git push -U origin main

Subir los cambios al github::

	git push

Descargar el github el historial de cambios pero sin descargarse los cambios. Así podemos revisar si los cambios que alguien hizo nos sirven o no::

	git fetch

Descargar el historial y también los cambios::

	git pull


