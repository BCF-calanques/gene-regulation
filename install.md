Linux install instructions for non packaged programs used by gene-regulation 
============================================================================
*Author - Edlira Nano*

## PREREQUISITES

For the workflows of this program to run you will need to install the following software :

* R 3+ (debian packaged)
* Python 2.7/3.4 (debian packaged)
* Snakemake 3.4+ (debian packaged)

Depending on the rules and workflow you will use on your analysis, you may also need to install the following :

* [SRA Toolkit](http://www.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=software) (debian packaged)
* [Sickle](https://github.com/najoshi/sickle) (debian packaged)
* BWA (debian packaged)
* Bowtie (debian packaged)
* [Bowtie 2](http://bowtie-bio.sourceforge.net/) (debian packaged)
* [SAMtools 1.3+](http://samtools.sourceforge.net/) (debian packaged)
* [FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/) (0.11.2+) (debian packaged)
* [bedtools](http://bedtools.readthedocs.org/) (debian packaged)
* [HOMER](http://homer.salk.edu/homer/index.html), blast, weblogo/seqlogo (see below for install instructions)
* [SARtools](https://github.com/PF2-pasteur-fr/SARTools) (packaged for R or bioconda, see below)
* MACS 14 (1.4.3)
* [MACS2](https://github.com/taoliu/MACS/)
* [SWEMBL](http://www.ebi.ac.uk/~swilder/SWEMBL/)
* ...

## Installation of non debian-packaged software

### [Homer install](http://homer.salk.edu/homer/introduction/install.html)

Homer needs `seqlogo` and `blat` programs to run, both not packaged:

#### To install `blat` on Linux:   
1 take the latest blatSrcXX.zip archive from https://users.soe.ucsc.edu/~kent/src/  
2 install it on /usr/local following instruction from 
http://nix-bio.blogspot.fr/2013/10/installing-blat-and-blast.html  
3 to avoid the "jkweb.a no rule" problem compile it with make MACHTYPE=$MACHTYPE  

#### To install `seqlogo`:
You have to install the `weblogo` archive  from http://weblogo.berkeley.edu/
The archive already contains the seqlogo binary file ready for use.  

### [SARtools install](https://github.com/PF2-pasteur-fr/SARTools)
On the [SARtools GitHub page](https://github.com/PF2-pasteur-fr/SARTools) follow the install instructions on the README file, to install it either within `R`, or using `bioconda`.
