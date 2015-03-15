# Usage #
The script called **'BBA.pl'** is designed for motif 'co-occurrence Analysis'.
**Note**: The computer you use should have R installed.

# Installation #
Simply put "BoBro2.0.tar.gz" in any directory,
  * $ tar zxvf BoBro2.0.tar.gz
enter the folder "BoBro2.0/" and type
  * $ ./INSTALL

# CMD line #
Simply run the following cmd to get a brief guide.
  * $ perl BBA.pl
BBA can do co-occurrence Analysis for file 'Input' by CMD:
  * $ perl BBA.pl Input SequenceNum

# Inputs #
The input file include TF name and the sequence lables which contain binding sites of this TF(see '**Motif\_position\_for\_BBA**' for example).
The format of input file:

> >AcrR

> _2251_

> _1650_

Here is a motif information for the TF AcrR: its name should have a prefix '>'; the number 2251 means there is a motif occurrence for AcrR in the 2251st promoter sequence.

# Outputs #
There are two output files: '**Input.BBA**' and '**Input.BBA.all**';

The significantly co-occurred TF pairs are collected in "Input.BBA";
Co-related scores for all TF pairs are stored in "Input.BBA.all";

The data in result file have 7 columns with means:

(1) TF1

(2) TF2

(3) Hyper-geometric p-value

(4) Total sequences number

(5) The number of sequences contain binding sites of TF1

(6) The number of sequences contain binding sites of TF2

(7) The number of sequences contain binding sites for both TF1 and TF2

# Contact #
Any questions, problems, bugs are welcome and should be dumped to

Qin Ma <maqin@uga.edu>

Bingqiang Liu <bingqiangsdu@gmail.com>

Creation: DEC. 18, 2012