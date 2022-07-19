# Gesuita_et_al_2022
This repository contains a script used in Gesuita et al. 2022, *Microglia contribute to the postnatal development of cortical somatostatin positive inhibitory cells and to whisker-evoked cortical activity*.

The script refers to the computational pipeline presented in figure 2A. Details are reported in the paragraph "Computational screening of transcriptomic data" in the STAR Methods section.

**HOW TO RUN THE CODE**

1. Choose a folder on your computer and set it as your working directory (wd).

2. Copy the "datasets" folder in your working directory. This folder already contains:
 - RNAseq data from Matcovitch-Natan et al., 2016 - GEO DataSets accession number GSE79812
 - RNAseq data from Favuzzi et al., 2019 - GEO DataSets accession number GSE120161
 - 3 lists of ligands and receptors downloaded from www.uniprot.org [^1]
 - a *ENSMUSG-Gene name* conversion table (Gene_list.txt)
 - a list of cytokine protein-protein interactions annotated on www.uniprot.org (ManualSTRING_Cytokine.txt)
 
3. Go to https://version-11-0.string-db.org/cgi/download.pl?sessionId=99uSZMsNLaTe, select "Mus usculus" from the "choose an organism" menu, download the following files and put them in the datasets folder:
 - 10090.protein.actions.v11.0.txt
 - 10090.protein.aliases.v11.0.txt
 - 10090.protein.links.detailed.v11.0.txt

4. Run the code. The output will be three .csv files reporting all interacting proteins between microglia and SST+ interneurons, PV+ interneurons or pyramidal cells.


[^1]: To download ligand and receptor lists, the following commands were inserted into the search bar of the Uniprot website (www.uniprot.org): for **CellMembrane_ExtracellularDomain_NotReceptor.txt** insert *locations:(location:"Cell membrane [SL-0039]") annotation:(type:topo_dom extracellular) NOT keyword:"Receptor [KW-0675]" reviewed:yes organism:"Mus musculus (Mouse) [10090]"*; for **Secreted.txt** insert *locations:(location:"Secreted [SL-0243]") AND reviewed:yes AND organism:"Mus musculus (Mouse) [10090]*; for **CellMembrane_ExtracellularDomain_Receptor.txt** insert *locations:(location:"Cell membrane [SL-0039]") annotation:(type:topo_dom extracellular) keyword:"Receptor [KW-0675]" AND reviewed:yes AND organism:"Mus musculus (Mouse) [10090]"*.
