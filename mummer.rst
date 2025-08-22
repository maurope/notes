
COMANDOS MUMMER
------

Alinear con nucmer::

	nucmer -maxmatch -c 100 -p name genome1.fa genome2.fa # name es el nombre que le damos


Alinear secuencias con mas de 500 pb::

	nucmer -maxmatch -c 100 -l 500 -p name genome1.fa genome2.fa

Filtrar el archivo delta::

	delta-filter -q -r name.delta > name.filter


Para las siguientes acciones puede también usarse el archivo filtrado name.filter

Extraer coordenadas::

	show-coords -r -c -l name.delta > name.coords 


Extraer snps::

	show-snps -C name.delta > name.snps 

Visualizar alineamiento::

	mummerplot -p name_plot --filter --png name.delta  