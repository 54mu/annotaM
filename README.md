# annot.aM
## table of contents
[ TOC ]
## introduction
This is a fast and extendible transcriptome annotation pipeline. It searches each transcript in multiple databases with multiple software. The final output consists in two tables, one for transcripts (the main one) and one for the translated transcripts. It is based on Snakemake, which grants a high degree of parallelism. It also makes a large use of web APIs. 
## dependendecies
### Software
* Python
* Snakemake
* Pandas
* diamond
* HMMER
* signalp
### Databases
* Uniprot-Swissprot
* PFAM
* orthoDB (from the desired taxa)
## how to use annot.aM
