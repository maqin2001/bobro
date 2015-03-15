#motif finding and refinement by filtering out noises at a genome scale

# Usage #
The software called '**BBR**' has the following functions:
  1. De-nove Motif finding in a fasta format promoter file.
  1. De-nove Motif finding with background sequences (if have) in fasta format.
  1. Motif finding with a comparative genomic framework.

# Installation #
Simply put "BoBro2.0.tar.gz" in any directory,
  * $ tar zxvf BoBro2.0.tar.gz
enter the folder "BoBro2.0/" and type
  * $ ./INSTALL

# CMD line #
  * Simply run the following cmd to get a brief guide.
> _$ perl BBR.pl_
  * To do De-nove Motif finding in a fasta format promoter file:
> _$ perl BBR.pl 1 promoters_
  * To do De-nove Motif finding with background sequences (if have) in fasta format:
> _$ perl BBR.pl 2 promoters background\_file_
  * To do Motif finding with a comparative genomic framework:
> _$ perl script/bbr\_cmp\_method.pl_


# Inputs and outputs #
## When used to do De-nove motif finding ##
  * The promoter file and background\_file should be in standard fasta format,(see promoter and background file in this folder for example).

  * The output file will be named promoters.closures, (see promoters.closures for example). Basically, it contains
  1. input data summary
  1. command line summary
  1. for each motif candidate found, there will be detailed information:
    * motif seed: the seed sequence used to find this motif(which is a 'core' of the motif);
    * motif position weight matrix and consensus;
    * a table show all the aligned motif.

## When used to do Motif finding with a comparative genomic framework ##
For the target genome and reference genomes, three kinds of data is needed:
  1. the genome data (which could be downloaded from ncbi genebank);
  1. the operon data (which could be downloaded or predicted from DOOR database);
  1. the orthology relationship between the target and references (which could be predicted use RBH method or GOST);
**NOTE**: Please see the the contents of folder example for details.

Take _E. coli_ as the target genome, two other species as reference.

  * target\_list: a list of gi from Ecoli;
  * Ecoli.opr: operon structure of Ecoli;
  * Escherichia\_coli\_K\_12\_substrMG1655\_uid57779: Ecoli data from NCBI;
  * ncbi\_data: the directory contains the species reference information downloaded from NCBI;

All the output files are stored in the folder example\_output, which contains:

  1. result.txt: same as the a De-nove prediction;
  1. motif.alignment: all alignments of predicted motif;
  1. motif.alignment.similarity: similarity score between each motif, (same as the output of BBC);
  1. Logos foreach motif are also given.

## Data format ##
  * peron: operon structure from DOOR;

|1:|16077069 |
|:-|:--------|
|2:| 16077070 |
|3:| 16077071 16077072 255767014 |
|4: |16077074 |

  * ortholog: orthology information between Ecoli and reference: (stanard output of GOST)
|145698239,|187933779| 5e-90,|6e-90|
|:---------|:--------|:------|:----|
|145698257,|187933775| 2e-05,|3e-05|
|145698262,|187935634| 1e-27,|6e-27|
|145698268,|187932476| 2e-25,|9e-23|
|145698269,|187933610| 5e-05,|7e-05|

# Contact #
Any questions, problems, bugs are welcome and should be dumped to

Qin Ma <maqin@uga.edu>

Chuan Zhou <zhouchuan121@gmail.com>

Creation: June. 27, 2012