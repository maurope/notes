
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

En el anterior comando intentamos agregar un valor a la base de datos de animales. Sin embargo, nos dá un error porque no le hemos dicho a la tabla que los registros van a ser autoincrementales, por lo que tendremos que modificar la tabla que ya creamos para agregar esta característica::

 	ALTER TABLE animales MODIFY COLUMN id int auto_increment;

Ahora si podemos ejecutar la línea "INSERT INTO"

Mostrar los comandos necesarios para recrear la tabla animales que ya habíamos creado. Ejemplo::

	CREATE TABLE 'animales'(
	'id' int NOT NULL AUTO_INCREMENT,
	'tipo' varchar (255) DEFAULT NULL,
	'estado' varchar(255) DEFAULT NULL,
	PRIMARY KEY (id)
	);


En SQL los comentarios se hace con -- y no con #::

	--Vamos a agregar nuevos valores a la tabla
	INSERT INTO animales ('tipo', 'estado') VALUES ('chanchito', 'feliz');
	INSERT INTO animales ('tipo', 'estado') VALUES ('dragon', 'feliz');
	INSERT INTO animales ('tipo', 'estado') VALUES ('felipe', 'triste');

Para seleccionar los registros ingresados::

	SELECT * FROM animales;