# annot.aM
## table of contents
[ TOC ]
## introduction
This is a fast and extendible transcriptome **annotation** pipeline. It searches each transcript in multiple databases with multiple software. The final output consists in two tables, one for transcripts (the main one) and one for the translated transcripts. It is based on Snakemake, which grants a high degree of parallelism. It also makes a large use of web APIs.
## How annotaM works
annotaM is like [King Crimson] it just works.  
The input transcriptome is searched in a blastx searche against UniprotSprot, allowing the assignation of uniprot ids to the transcripts via the best hit. Such uniprot ids are then used to query the Gene Ontology in order to obtain GO terms and are used to retrieve relevant pathways from reactome database.  
The input transcriptome is also translated with transdecoder and the resulting sequences are used for a HMMER search against the PFAM database in order to retrieve functional domains.  
Signalp5 (optional) is used to identify signal peptides in order to identify eventual secreted peptides. _[opportunità di integrazione con toxline]_.
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
