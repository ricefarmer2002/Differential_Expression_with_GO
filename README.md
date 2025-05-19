Genetics Exam - Transcriptomic Analysis Pipeline
Overview
This repository contains the code and analysis for transcriptomic analysis, specifically differential expression analysis, performed on RNA-seq data from mutant and control samples. The focus of this study is a single-nucleotide polymorphism (SNP) in the transcription factor, forkhead protein (FKHR) mRNA, suspected to cause a genetic disease by altering gene expression.

Key Findings
The most significant SNP (C1103G) leads to a Proline-to-Arginine amino acid change in FKHR.

Differential expression analysis identified thousands of differentially expressed genes (DEGs).

Gene Ontology (GO) enrichment analysis highlighted:

Upregulation of mitotic processes, chromosome segregation, and mRNA processing.

Downregulation of ion homeostasis and autophagy pathways.

Repository Structure
bash
Copy
Edit
├── data/                 # Input data (counts and sample metadata)
├── results/              # Analysis outputs (plots, DEG lists, enriched GO terms)
├── scripts/              # R scripts for the analysis
├── figures/              # Generated figures (PCA, MA plot, Volcano plot)
└── README.md             # This file
Prerequisites
R (version 4.0 or above)

R packages:

DESeq2

Tidyverse

pheatmap

EnhancedVolcano

clusterProfiler

org.Hs.eg.db

Biostrings

Installation
Ensure that all required R packages are installed:

r
Copy
Edit
install.packages("tidyverse")
install.packages("pheatmap")
BiocManager::install("DESeq2")
BiocManager::install("EnhancedVolcano")
BiocManager::install("clusterProfiler")
BiocManager::install("org.Hs.eg.db")
BiocManager::install("Biostrings")
Usage
1. Load Data
Place the counts_data.csv and sample_info.csv files in the data/ directory.

Adjust file paths in the R script if using a different directory.

2. Run the Analysis
Use the R script in the scripts/ directory to perform the full analysis:

r
Copy
Edit
source("scripts/transcriptomic_analysis.R")
3. Generate Plots
MA plot, Volcano plot, PCA, Heatmap, and GO enrichment dot plots are automatically generated in the figures/ directory.

4. View Results
Differential expression results are saved as results/diffexpr-results.txt.

Significant DEGs are saved in results/significant_DEGs.csv.

GO enrichment analysis results are saved in results/enrichment_results.txt.

Key Analysis Steps
Loading Data: RNA-seq count matrix and sample metadata are loaded and validated.

DESeq2 Differential Expression: Normalization, statistical testing, and identification of DEGs.

Visualizations:

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

Notes
The GAI (Generative AI) Declaration: ChatGPT 3.5 was used for interpreting error messages and improving code annotations.

The full report on the analysis and findings can be found in the report/ directory.

References
Love, M.I., Huber, W. and Anders, S. (2014). DESeq2: Differential gene expression analysis based on the negative binomial distribution.

Garrison, E. and Marth, G. (2012). FreeBayes: Haplotype-based variant detection.

Yu, G., Wang, L.-G., Han, Y. and He, Q.-Y. (2012). clusterProfiler: Comparing Biological Themes Among Gene Clusters.
