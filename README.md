## quarantine-time-tcga

Here we will walk through several TCGA analyses in R.  They are ordered by date:

## Colon cancer analysis focused in circadian gene oscillation
The TCGA data was downloaded from UCSC Xena: https://xenabrowser.net/datapages/
The Sequencing data is too large to store on github, but the filenames and respective downlaoded locations are:
Colon_cancer_Seq.gz
https://xenabrowser.net/datapages/?dataset=TCGA-COAD.htseq_fpkm.tsv&host=https%3A%2F%2Fgdc.xenahubs.net&removeHub=https%3A%2F%2Fxena.treehouse.gi.ucsc.edu%3A443

colon_cancer_phenotypes.gz
https://xenabrowser.net/datapages/?dataset=TCGA-COAD.GDC_phenotype.tsv&host=https%3A%2F%2Fgdc.xenahubs.net&removeHub=https%3A%2F%2Fxena.treehouse.gi.ucsc.edu%3A443

GO Terms used were obtained from uniprot, for purposes of clarity, there are also provided as: Human_all_GO_terms.tab.gz

The scripts provided should detail the analysis.  Breifly, the steps are listed below:

1. we read in the datasets and chose samples which are informative (remove non-tumor and replicate samples based on barcode).  Information on how TCGA barcodes are specified can be found here: https://docs.gdc.cancer.gov/Encyclopedia/pages/TCGA_Barcode/

2. Retain only the genes of interest from assignment in "circadian" pathways, inspect their relative expression level and 
