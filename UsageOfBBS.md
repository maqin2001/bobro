#motif scanning

# BBS Usage #
This software provides a BoBro Based Searching/Scanning (**BBS**) tool capable of searching motifs in a set of sequences using known motif patterns.

# Installation #
Simply put "BoBro2.0.tar.gz" in any directory,
  * $ tar zxvf BoBro2.0.tar.gz
enter the folder "BoBro2.0/" and type
  * $ ./INSTALL

# Inputs and outputs #
The major program in the provided package is `*BBS*`, it can search motifs in a fasta file using known alignment, matrix format or consensus of motifs, and example files are provided (example\_alignment, example\_matrix and example consensus).

## For basic usage of motif scanning ##
Use packed PERL script BBS.pl by
  * basic usage:
> _$ perl BBS.pl_
  * Search motif in alignment format:
> _$ perl BBS.pl motif\_alignment promoters 1_
  * Search motif in matrix format:
> _$ perl BBS.pl motif\_matrix promoters 2_
  * Search motif in consensus format
> _$ perl BBS.pl motif\_consensus promoters 3_
  * Search motif considering background genome:
> _$ perl BBS.pl motif\_consensus promoters 1/2/3 background_

## For advanced usage of motif scanning ##
Use the program **BBS**
  * basic usage:
> _$ ./BBS -h (./BBS)_

  * To search motif base on alignment
> _$ ./BBS -i example -j example\_alignment_
> _$ ./BBS -i example -j example\_alignment -D (output seed only)_

**note**: the minimal length of sequences in example should not be less than the minimal motif length in example\_alignment

  * To search motif base on frequency matrix
> _$ ./BBS -i example -m example\_matrix_
> BBS generates a output file, namely, '**.motifinfo**' file. In '.motifinfo' file, it generates a closures corresponding to each alignment (matrix) in example\_alignment (example\_matrix), in the increasing order of closure's pvalue.

  * To calculate the zscore compare to the background
> _$ ./BBS -i example -j example\_matrix -z example -u .95_

  * To transfer consensus format to matrix
> _$ ./BBS -p example\_consensus -i example > example\_consensus\_matrix_

  * To compare similarity between any pair of input motifs
> _$ ./BBS -i example -j example\_alignment -C_
> _$ ./BBS -i example -j motif.txt -C (uninformative cloumn example)_

  * To change alignment to matrix and consensus
> _$ ./BBS -i example -j example\_alignment -a_

  * Furthermore, we can control the output result mainly by controlling four parameters
|-e| [1,3]| the larger the e value the more searched TFBSs  |
|:-|:-----|:------------------------------------------------|
| -t| (0.3,0.9)| the smaller the t value the more searched TFBSs|
| -n| (0,0.3]| when e>1, the larger of n the stricter of searching strength|
|-E|  | if you want to get more searched TFBSs, adding -E|

# Input Formats #
**Matrix**
|A|    5   6   4   5   4   1   0   4   4   3   5   1   2   4   3   3   0   0   3   4   3   3   3   3   3|
|:|:----------------------------------------------------------------------------------------------------|
|C |    5   0   2   2   1   2   1   5   1   0   0   1   5   0   0   0   0   7   0   0   0   4   4   1   0|
|G |    0   1   0   4   6   5   2   1   5   8   6   8   0   5   8   8   2   2   7   7   8   4   4   4   8|
|T |    1   4   5   0   0   3   8   1   1   0   0   1   4   2   0   0   9   2   1   0   0   0   0   3   0|

**Alignment**
|ATCAACTGAAACAAAACGAAAGATT|
|:------------------------|
|GAAAACCATTATCTTTCGTTTTATT|
|GACTTTCATTATGTTTCTTTTGTGA|
|ACCAAGTGAAATGAAACGAAAGGCA|
|AACTTTCAGTTTCTTTTCTATAGAT|
|AAATTTCGTTTTATTTCTTTTTTCT|
|GCAATCCCTTTTGCTTCCTTTATCT|
|GCCTTTCTTTTTCTTTCGTTTTGAT|
|CAGGGTCAATTAGCTTCGTTTTGAT|
|GCAAAACGAAATGAAACGAAAGTTT|
|AAGGTGGGCTTGCATTTGCTTAATA|

**Consensus**
|AGGRKTTBCCGA|
|:-----------|


# NeedToDo #
  1. Adopt the output format of BoBro as input.
  1. Add the function of analysis motif with gap


# Contact #
Any questions, problems, bugs are welcome and should be dumped to

Qin Ma <maqin@uga.edu>

Chuan Zhou <zhouchuan121@gmail.com>

Creation: July. 26, 2009