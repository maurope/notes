
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

Si queremos seleccionar solo un registro  en este caso donde id sea 1::

	SELECT * FROM animales WHERE id=1;

Si queremos seleccionar los que tenga estado feliz::

	SELECT * FROM animales WHERE estado = 'feliz';

Si queremos seleccionar por dos condiciones::

	SELECT * FROM animales WHERE estado = 'feliz' AND tipo = 'chanchito'

Si queremos actualizar el estado de triste a feliz para el id3 usamos::

	UPDATE animales SET estado = 'feliz' WHERE id=3;

Para buscar nuestros registros actualizados::

	SELECT * FROM ANIMALES;

Para eliminar registros de nuestra base de datos::

	DELETE from animales WHERE estado = 'feliz';

Nos va a arrojar el error 1175 para prevenir que borremos registros. Si queremos eliminar un registro necesariamente tenemos que indicar un id.

Para borrar un registro tenemos que indicar el id ::

	DELECTE from animales where id=3;

Para actualizar un registro también tenemos que indicar el id::

	UPDATE animales SET estado = 'triste' WHERE id= 3;

Vamos a ver en profundidad algunas condiciones. Para eso creamos una nueva tabla::

	CREATE TABLE user(
	id int not null auto-increment,
	name varchar(50) not  null,
	edad int not null,
	email varchar(100) not null,
	primary key (id)
	);

	INSERT INTO user (name, edad, email) values ('oscar', '25', 'oscar@gmail.com');
	INSERT INTO user (name, edad, email) values ('layla', '15', 'laylar@gmail.com');
	INSERT INTO user (name, edad, email) values ('Nicolas', '36', 'nico@gmail.com');
	INSERT INTO user (name, edad, email) values ('Chanchito', '7', 'chanchito@gmail.com');

Después de crear la base de datos e ingresar los datos, podemos ingresar instrucciones, ejemplo ver los datos ingresados::

	SELECT * FROM USER;

	SELECT * FROM Limit 1; -- Solo nos muestra el primer registro

	SELECT * FROOM user WHERE edad > 15;

	SELECT * FROM user WHERE edad >= 15;
	
	SELECT * FROM user WHERE edad > 20 AND email = 'nico@gmail.com';

	SELECT * FROM user WHERE edad > 20 OR email = 'layla@gmail.com';

	SELECT * FROM user WHERE email != 'layla@gmail.com';

	SELECT * FROM user WHERE edad BETWEEN  15 and 30;

	SELECT * FROM user WHERE email LIKE '%gmail%';

La consulta previa nos muestra todos los registros que contengan gmail, porque aparece dentro de dos %%, si lo que yo quiero es que me muestre solo los registros que terminan en gmail, debo consultar así '%gmail'. Si queremos por ejemplo buscar los correos electrónicos que comiencen con oscar, debemos poner 'oscar%'

Para ordenar los resultados de forma ascendente::

	SELECT * FROM user ORDER BY edad ASC;

Para ordenar los resultados de forma descendiente::

	SELCT * FROM user ORDER BY edad DESC;

Seleccionar el usuario de mayor edad::

	SELECT MAX(edad) AS mayor FROM user;

Seleccionar el usuario de menor edad::

	SELECT MIN(edad) AS menor FROM user;

También se puede cambiar el nombre de la columna que se muestra::

	SELECT id, name AS nombre FROM user;

Agrupación de datos, crearemos una tabla de productos::

	CREATE TABLE product(
	id int not null auto_increment,
	name varchar(50) not null,
	created_by int not null,
	marca varchar(50) not null,
	primary key(id),
	foreign key (created_by) references user(id))
	);

Para cambiar el nombre de la tabla::

	rename table products to product;

Para insertar varios datos al tiempo::

	insert into product (name, created_by, marca)
	values
	('ipad', 1, 'apple'),
	('iphone', 1, 'apple'),
	('watch', 2, 'apple'),
	('imac', 3, 'apple'),
	('ipad mini', 2, 'apple');

Para ver como quedó la tabla::

	select * from product;

Juntar las tablas y hacer que el id de la tabla de usuario sea igual al created_by de la tabla de producto::

	select u.id, u.email, p.name from user u 
	left join product p on u.id = p.created_by;

Hacerlo con rigth join::

	select u.id, u.email, p.name from user u 
	rigth join product p on u.id= p.created_by;

Para mostrar la intersección de las tablas::

	select u.id, u.name, p.id, p.name from user u 
	cross join product p;

Este comando hace un 'producto cruzado' entre todos los datos, puede ser peligroso porque puede dar muchos resultados::

	select u.id, u.name, p.id, p.name from user u 
	cross join product p;

Contar el número de registros por grupo::

	select count(id), marca from product 
	group by marca;

	select count(p.id), u.name from product p
	left join user u on u.id = p.created_by 
	group by  p.created_by;

Si quiero filtrar los resultados puedo usar having::

	select count (p.id), u.name from product p
	left join user u on u.id = p.created_by 
	group by p.created_by 
	having count(p.id) >=2;


Solo me mostrará los conteos iguales o superiores a 2

Para eliminar tablas usamos::

 drop tables product;
 drop table animales;
 drop table users;



