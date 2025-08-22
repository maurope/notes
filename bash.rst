
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


Búsqueda y filtros
------

Buscar archivos y directorios::

  find directorio -name 'archivo'

Buscar archivo mediante base de datos::

  locate 'archivo'

Buscar patrones de text rápido::

  ag patron

Muestra donde esta instalado el programa::

  pip show


Información del sistema
------

Mostrar procesos en ejecución::

  top

Versión mejorada de top::

  htop

Mostrar espacio en el disco::

  df -h

Mostrar el uso del espacio por directorio::

  du -h

Mostrar memoria libre y utilizada::

  free

Red y conectividad
------

Verificar conectividad con el servidor::

  ping dominio.com

Mostrar información de red::

  ifconfig 

Mostrar conexiones red::

  netstat -tulpn


Comandos generales
------

Mostrar manual del comando::

  man comando

Mostrar historial de comandos::

  history

Limpiar consola::

  clean
























