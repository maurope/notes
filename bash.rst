
COMANDOS BASH
-----------

Navegación y exploración de archivos
------
Listar archivos y directorios::

  ls

Cambiar de directorio::

  cd

Mostrar ruta del directorio actual::

  pwd

Crear nuevo directorio::

  mkdir nuevo_directorio

Copiar archivos o directorios::

  cp origen destino

Mover o renombrar archivos o directorios::

  mv origen destino

Eliminar archivos:: 

  rm archivo

Cambiar permisos de archivos::

  chmod <permisos> archivo

Cambiar el propietario de archivos::

  chown

Crear un archivo::

  touch nombre

Muestra el contenido de un archivo::

  cat


Manipulación de archivos de texto
------

Mostrar el contenido de un archivo::

  cat archivo

Editar archivos de texto en nano::

  nano archivo

Editar archivos de texto en vim::

  vim archivo

Editar archivos de texto en emacs::

  emacs archivo

Mostrar las primeras líneas de un archivo::

  head archivo

Mostrar las últimas lineas de un archivo::

  tail archivo

Mostrar las primeras 50 líneas de un archivo::

  head -n 50 archivo

Buscar patrones en un archivo::

  grep patron archivo

Editar y transformar texto::

  sed 's/old/new/' archivo

Procesar y analizar texto (scanning). Imprimir la primera columna de cada línea::

  awk '{print $1}' archivo
