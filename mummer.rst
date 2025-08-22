
COMANDOS MUMMER
------

Alinear con nucmer::

	nucmer -maxmatch -c 100 -p name genome1.fa genome2.fa # name es el nombre que le damos


Alinear secuencias con mas de 500 pb::

	nucmer -maxmatch -c 100 -l 500 -p name genome1.fa genome2.fa

Filtrar el archivo delta::

	delta-filter -q -r name.delta > name.filter

Extraer coordenadas::

	show-coords -r -c -l name.delta > name.coords # puede usarse también el archivo filtrado name.filter


Extraer snps::

	show-snps -C name.delta > name.snps # puede usarse también el archivo filtrado name.filter

Visualizar alineamiento::

	mummerplot -p name_plot --filter --png name.delta  # puede usarse también el archivo filtrado name.filter