---
permalink: /research
title: "Genomics and transcriptomics research"
author_profile: true
hero_image: "images/dna1.gif"
---

# Transriptomics | RNA-seq data pipelines

RNA sequencing (RNA-seq) pipelines are essential for transcriptomic research, enabling the quantification and analysis of gene expression across different biological conditions. Standardized approaches, such as those used in The Cancer Genome Atlas (TCGA), incorporate tools like Bowtie2 for read alignment and Limma for differential gene expression analysis. Bowtie2 is a fast and memory-efficient aligner that maps short reads to a reference genome, ensuring accurate representation of transcript abundance. Limma, originally designed for microarray data, has been adapted for RNA-seq to model gene expression changes using empirical Bayes methods, improving statistical power in differential expression analysis. These tools, integrated into comprehensive workflows, help researchers uncover insights into disease mechanisms and gene regulation.

The RNA-seq analysis pipeline typically follows several key steps: quality control, alignment, quantification, normalization, and differential gene expression analysis. Initially, raw reads undergo quality assessment using tools like FastQC, followed by adapter trimming and filtering with Trimmomatic. High-quality reads are then aligned to a reference genome using Bowtie2 or STAR, generating alignment files that are processed for gene-level quantification using featureCounts or HTSeq. Normalization methods, such as TMM (trimmed mean of M-values) in Limma, adjust for library size differences before differential expression analysis. Finally, statistical models in Limma, DESeq2, or edgeR identify significantly differentially expressed genes, often visualized through heatmaps, volcano plots, and pathway enrichment analyses. These steps ensure rigorous and reproducible RNA-seq data analysis, facilitating discoveries in transcriptomics and precision medicine.

I have built pipelines for professors and corporate partners internally and externally to my role in the Integrative Genomics group in Bristol-Myers Squibb's Discovery Biology department. Utilizing the best methods in clinical transcriptomic research, I have added value to differential gene expression (DGE) projects by building and validating data pipelines using bash, Nextflow, CWL, Galaxy, and more. I have automated sequencer-to-data-pipeline processes by monitoring Illumina buckets for new files, and launching the pipeline automatically following a sequencer runs completion. Utilizing the best in R and Bioconductor statistical analysis packages, I have created amazing QC reports including heatmaps and diagnostic outputs from sample covariates and other design matrix variables.


# Functional genomics


# k-mers, minimizers, and sequence alignment



