# Gesuita_et_al_2022
This repository contains a script used in Gesuita et al. 2022, *Microglia contribute to the postnatal development of cortical somatostatin positive inhibitory cells and to whisker-evoked cortical activity*.

The script refers to the computational pipeline presented in figure 2A. Details are reported in the paragraph "Computational screening of transcriptomic data" in the STAR Methods section.

**HOW TO RUN THE CODE**

1. choose a folder and set it as your working directory (wd).

2. copy the "datasets" folder in your working directory. This already contains:
 - RNAseq data from Matcovitch-Natan et al., 2016 - GEO DataSets, accession number GSE79812
 - RNAseq data from Favuzzi et al., 2019 - GEO DataSets, accession number GSE120161
 - 3 lists of ligands and receptors downloaded from www.uniprot.org (details are reported in the STAR Methods section)
 - a *ENSMUSG-Gene name* conversion table (Gene_list.txt)
 - a list of cytokine protein-protein interactions annotated on www.uniprot.org (details are reported in the STAR Methods section)
 
3. go to https://version-11-0.string-db.org/cgi/download.pl?sessionId=99uSZMsNLaTe, select "Mus usculus" from the "choose an organism" menu, download the following files and put them in the datasets folder:
 - 10090.protein.actions.v11.0.txt
 - 10090.protein.aliases.v11.0.txt
 - 10090.protein.links.detailed.v11.0.txt

4. run the code: the output will be three .csv files reporting all interacting proteins between microglia and SST+ interneurons, PV+ interneurons or pyramidal cells.
