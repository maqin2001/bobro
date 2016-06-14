# **BOBRO1.0** #
## Introduction ##
**BOBRO1.0** is an algorithm for prediction of cis regulatory motifs in a given set of promoter sequences. The algorithm substantially improves the prediction accuracy and extends the scope of applicability of the existing programs based on two key new ideas: (i) a highly effective method for reliably assessing the possibility for each position in a given promoter to be the (approximate) start of a conserved sequence motif; and (ii) a highly reliable way for recognition of actual motifs from the accidental ones based on the concept of 'motif closure'. These two key ideas are embedded in a classical framework for motif finding through finding cliques in a graph but have made this framework substantially more sensitive as well as more selective in motif finding in a very noisy background. A comparative analysis shows that the performance coefficient was improved from 29% to 41% by our program compared to the best among other six state-of-the-art prediction tools on a large-scale data sets of promoters from one genome, and also consistently improved by substantial margins on another kind of large-scale data sets of orthologous promoters across multiple genomes. The power of BOBRO1.0 in dealing with noisy data was further demonstrated through identification of the motifs of the global transcriptional regulators by running it over 2390 promoter sequences of Escherichia coli K12. The related data sets and results can be found at http://csbl.bmb.uga.edu/~maqin/motif_finding/.

## Citing us ##
Guojun Li, Bingqiang Liu, Qin Ma, Ying Xu, _A new framework for identifying cis-regulatory motifs in prokaryotes_, **Nucleic Acids Res.** 2011 Apr;39(7):e42

# **BOBRO2.0** #
## Introduction ##
**BOBRO2.0** is an integrated toolkit for prediction and analysis of cis regulatory motifs. This toolkit can (a) reliably identify statistically significant cis regulatory motifs at a genome scale; (b) accurately scan for all motif instances of query motifs in specified genomic regions using a novel method for p-value assessment; (c) provide highly reliable comparisons and clustering of identified motifs, which takes into consideration of the weak signals from the flanking regions of the motifs; and (d) analyze co-occurred motifs in the regulatory regions. We have carried out systematic comparisons between motif predictions by BOBRO2.0 and by the MEME package. The overall performance comparisons on E. coli K12 genome and the Human genome show that BOBRO2.0 can identify the statistically significant motifs at a genome scale more efficiently, identify motif instances more accurately and get more reliable motif clusters than MEME. In addition BOBRO2.0 provides correlational analyses among the identified motifs to facilitate the inference of joint regulation relationships of transcription factors.

## Citing us ##
Qin Ma, Bingqiang Liu, Chuan Zhou, Yanbin Yin, Guojun Li, Ying Xu, _BoBro2.0: An integrated toolkit for accurate prediction and analysis of cis regulatory elements at a genome scale_. **Bioinformatics**, 10.1093/bioinformatics/btt397, 2013

## Function ##
| **Functions**|	**BoBro2.0**|	**Unique feature**|
|:-------------|:------------|:------------------|
|Motif Refining|	BBR	|Strong  ability in filtering out noises at a genome scale|
|Motif Scanning|	BBS	|p-value assessment for all the scanned candidate motifs|
|Motif Comparison|	BBC|	Utilization of weak conserved signals of motifs’ flanking regions when comparing motifs; A motif clustering algorithm|
|Motif Annotation|	BBA|	Motifs’ co-occurrence annotation|

## Contact ##
Any questions, problems, bugs are welcome and should be dumped to Qin Ma <**_qin.ma@sdstate.edu_**>
