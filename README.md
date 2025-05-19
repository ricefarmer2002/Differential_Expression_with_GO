# Genetics Exam - Transcriptomic Analysis Pipeline

#### Overview
This repository contains the code and analysis for transcriptomic analysis, specifically differential expression analysis, performed on RNA-seq data from mutant and control samples. The focus of this study is a single-nucleotide polymorphism (SNP) in the transcription factor, forkhead protein (FKHR) mRNA, suspected to cause a genetic disease by altering gene expression.

![image](https://github.com/user-attachments/assets/d7f41a58-7ebf-4e40-9413-03b10ec340df)
Figure 1. Integrative Genomics Viewer (IGV) visualising SNPs identified in the forkhead protein (FKHR) mRNA transcription factor coding sequence.

Mutation	Codon Change	Amino Acid (AA) Change	AA Property Change	Quality Score	Depth	Alternative Observations
C1103G	CCCCGC	Proline Arginine	Non-polar Positively Charged	101150	6809	6672
T1142C	TTCCTC	Phenylalanine Leucine	Aromatic  Aliphatic (hydrophobic)	107039	7130	7002
T1878A	TTCATC	Phenylalanine  Isoleucine	Aromatic  Aliphatic (hydrophobic)	106998	7214	7061

#### Key Findings
The most significant SNP (C1103G) leads to a Proline-to-Arginine amino acid change in FKHR.

Differential expression analysis identified thousands of differentially expressed genes (DEGs).

Gene Ontology (GO) enrichment analysis highlighted:

Upregulation of mitotic processes, chromosome segregation, and mRNA processing.

Downregulation of ion homeostasis and autophagy pathways.

#### Repository Structure
bash
Copy
Edit
├── DE_PIPELINE_UPLOAD_RDY.qmd
└── README.md             # This file

##### Prerequisites
R (version 4.0 or above)

R packages:

DESeq2

Tidyverse

pheatmap

EnhancedVolcano

clusterProfiler

org.Hs.eg.db

Biostrings


### Visualizations:

MA plot for differential expression overview.

Volcano plot for significant genes.

PCA for sample clustering.

Heatmap for sample distances.

Gene Ontology Analysis: GO enrichment using clusterProfiler to identify affected pathways.

Example Plots
1. MA Plot

2. Volcano Plot

3. PCA Plot

4. Heatmap

#### Notes
The GAI (Generative AI) Declaration: ChatGPT 3.5 was used for interpreting error messages and improving code annotations.

The full report on the analysis and findings can be found in the report/ directory.

References
Love, M.I., Huber, W. and Anders, S. (2014). DESeq2: Differential gene expression analysis based on the negative binomial distribution.

Garrison, E. and Marth, G. (2012). FreeBayes: Haplotype-based variant detection.

Yu, G., Wang, L.-G., Han, Y. and He, Q.-Y. (2012). clusterProfiler: Comparing Biological Themes Among Gene Clusters.
