# LIMST
The ***LIMST*** used for building **landscapes of immune microenvironment for solid tumors**.

## Table of Contents
1. System requirements
2. Installation guide
3. Codes
4. Dataset
5. Contact

## System requirements
The following are the version numbers of the software or algorithms used in this study.

	AUCell 1.12.0
	GSVA 1.38.2
	Seurat 4.3.0.1
	scFEA 1.1
	Palantir 1.3.3
	scanpy 1.10.1
	monocle3 1.3.1
	CellphoneDB 5.0.0
	TCGAbiolinks 2.26.0
	survival 3.2-10
	Python 3.9
 	Ubuntu 18.04
	R 4.0.5, 4.1.0 and 4.3.1(only for SENIC analysis)

## Installation guide
Python libraries can be installed in a shell environment using the "pip install" command. 

	pip install "library_name"

R packages can be installed in the R environment using the "install.packege()" or "BiocManager::install()" commands.

	install.packege("packege_name")

	if(!"BiocManager"%in%installed.packages()){ 
	install.packages("BiocManager")}
 	if(!"packege_name"%in%installed.packages()){ 
	BiocManager::install("packege_name")}

	if (!"devtools" %in% installed.packages()) {
  	install.packages("devtools")}
   	devtools::install_github("packege_name")



## Codes
Specific descriptions of the codes can be found in the corresponding documents.
### 1. Download data
"1_SRRraw data download.txt" is used to download the single-cell SRR raw file and decompress it into a "fastq.gz" file, and finally execute the SARTsolo command to get the processed file.
	 
"2_FASTQ raw data download.txt" is used to download the single-cell "fastq.gz" and execute the SARTsolo command to get the processed file.
### 2. Quality control and subgroup
"1_pancancer_data_python_process.txt" is used to import the processed data into the python environment and perform quality control to eliminate low quality cells and genes and finally perform dimensionality reduction clustering on the data.

"2_pan-cancer huge group analysis.txt" was used to define overall cellular subpopulations and plot subpopulation umap plots, cell scale plots, and other plots

### 3. NKT cell
"1_NKT cell extraction code (marker).txt" was used to extract NKT cell subclusters.

"2_T_celL_DEGs.txt" was used to plot the umap of T-cell subpopulations, cell scale plots, and other graphs.

"3_AddModule.txt" was used to score T cell subpopulations (e.g., TEFF and TEX scores).

"4_palantir.txt" was used for pseudotiming analysis of T cell subclusters.

### 4. Myeloid cell
"1_Extracellular matrix scoring.txt" was used to score extracellular matrix remodeling for subclusters of cells between samples.

"2_M1M2score.txt" was used to assess the M1/M2 polarization phenotype of myeloid cell subpopulations by scores.

"3_scFEA.txt" was used for the analysis of cellular metabolic reprogramming.

"4_Prognostic analysis.txt" was used for prognostic analysis of cell subpopulations in the joint the TCGA database.

### 5. B cell
"1_SCENIC.txt" was used to analyze the expression levels of transcription factors in cellular subclusters among different sample groups.

"2_monocle3.txt" was used to characterize the developmental trajectory of B cells.

"3_Gene_Trajectory.txt" was used to analyze gene trajectory activity in B cells.

"4_cellphoneDB.txt" was used to analyze ligand-receptor pairs between different cell types.

### 6. Generic analysis
"1_OR.txt" was used to show the dominance ratio of cell subpopulation distribution in each tissue.

"2_GSVA.txt" was used to explore enrichment pathways in cellular subclusters.
### 7. Spatial transcriptome
"TESLA.txt" was used to verify the presence of specific cells in the spatial transcriptome.

## Dataset
The dataset for this study is maintained in the [_zenodo_](https://zenodo.org/) database under the registration number: [_11577432_](https://zenodo.org/records/11577432). 
The dataset includes processed single-cell sequencing data from 25 types of solid tumors and 3 normal tissues.

## Contact
If you have any questions or feedback, feel free to contact me at zouzhuan@sr.gxmu.edu.cn.
