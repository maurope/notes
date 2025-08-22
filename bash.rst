
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


Requirements
------------
Install the requirements by entering the following commands in the terminal:

Install biopython module::

  pip install biopython

Install Basic Local Alignment Search Tool (BLAST)::

  sudo apt update
  sudo apt install ncbi-blast+


Example
-------

The file **test.py**
contains an example that illustrates how to use the code to detect the 
centromere location in chromosome 01 of the *Oryza sativa* Indica Group cultivar:IR64.
Other IR64 chromosome sequences are available in the 
`NCBI Genome database <https://www.ncbi.nlm.nih.gov/genome>`_
under the accession number RWKJ00000000.

Below is a more detailed explanation of the same example:

Import module::

  import CentOFinder as cf

Input CentO fasta file path::

  CentO_path = 'input_data/CentO_AA.fasta'

Input chromosome fasta file path::

  chromosome_path = 'input_data/Osat_IR64_AGI_NSD_chrOK.id_chr01.fasta'

Input window size::

  size_w = 100_000

Instantiate the CentOFinder class::

  centromere = cf.CentOFinder(CentO_path, chromosome_path, size_w)

Call the method to detect the centromere::

  centromere.detect_centromere()

The above prints the following::

  Chromosome length: 44350042 base pairs
  Window size: 100000
  Total chromosome whindows: 443
  ----------------------------------------
  Approximate location of centromere:
  Window number: 178
  Window midpoint (base pair): 17850000
  2Mbp centromeric region prediction: [16850000,18850000]
  3Mbp centromeric region prediction: [16350000,19350000]

Plot the results

.. image:: Osat_IR64_chr01.png
  :width: 800
