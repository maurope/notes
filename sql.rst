
COMANDOS SQL
-------

Crear base de datos holamundo::

	CREATE database holamundo;

Muestra las bases de datos::

	SHOW databases;

Usar la base de datos de holamundo::

	USE holamundo;

Crea una tabla llamada animales::

	CREATE TABLE animales (
		id int,
		tipo varchar(),
		estado varchar(),
		PRIMARY KEY (id)
		);

En el anterior comando intentamos agregar un valor a la base de datos de animales. Sin embargo, nos dá un error porque no le hemos dicho a la tabla que los registros van a ser autoincrementales, por lo que tendremos que modificar la tabla que ya creamos para agregar esta característica. 