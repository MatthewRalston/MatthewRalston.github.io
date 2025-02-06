---
permalink: /research
title: "Genomics and transcriptomics research"
author_profile: true
hero_image: "images/dna1.gif"
---

# Transriptomics | RNA-seq data pipelines

RNA sequencing (RNA-seq) pipelines are essential for transcriptomic research, enabling the quantification and analysis of gene expression across different biological conditions. Standardized approaches, such as those used in The Cancer Genome Atlas (TCGA), incorporate tools like Bowtie2 for read alignment and Limma for differential gene expression analysis. Bowtie2 is a fast and memory-efficient aligner that maps short reads to a reference genome, ensuring accurate representation of transcript abundance. Limma, originally designed for microarray data, has been adapted for RNA-seq to model gene expression changes using empirical Bayes methods, improving statistical power in differential expression analysis. These tools, integrated into comprehensive workflows, help researchers uncover insights into disease mechanisms and gene regulation.

The RNA-seq analysis pipeline typically follows several key steps: quality control, alignment, quantification, normalization, and differential gene expression analysis. Initially, raw reads undergo quality assessment using tools like FastQC, followed by adapter trimming and filtering with Trimmomatic. High-quality reads are then aligned to a reference genome using Bowtie2 or STAR, generating alignment files that are processed for gene-level quantification using featureCounts or HTSeq. Normalization methods, such as TMM (trimmed mean of M-values) in Limma or median of ratios in DESeq2 adjust for library size differences before differential expression analysis. Finally, statistical models in Limma, DESeq2, or edgeR identify significantly differentially expressed genes, often visualized through heatmaps, volcano plots, and pathway enrichment analyses. These steps ensure rigorous and reproducible RNA-seq data analysis, facilitating discoveries in transcriptomics and precision medicine.

I have built pipelines for professors and corporate partners internally and externally to my role in the Integrative Genomics group in Bristol-Myers Squibb's Discovery Biology department. Utilizing the best methods in clinical transcriptomic research, I have added value to differential gene expression (DGE) projects by building and validating data pipelines using bash, Nextflow, CWL, Galaxy, and more. I have automated sequencer-to-data-pipeline processes by monitoring Illumina buckets for new files, and launching the pipeline automatically following a sequencer runs completion. Utilizing the best in R and Bioconductor statistical analysis packages, I have created amazing QC reports including heatmaps and diagnostic outputs from sample covariates and other design matrix variables.


# Functional genomics


Functional genomics is a field of research focused on understanding the roles and interactions of genes within biological systems, often using high-throughput techniques such as RNA sequencing (RNA-seq), CRISPR screens, and proteomics. Unlike structural genomics, which emphasizes gene mapping and sequencing, functional genomics aims to determine how genes contribute to cellular processes, phenotypes, and disease states. Key approaches include transcriptomics to study gene expression, epigenomics to examine regulatory modifications, and metabolomics to assess biochemical changes. By integrating these data, researchers can uncover gene regulatory networks and identify biomarkers for diseases such as cancer and neurodegenerative disorders. I have worked with both Bayer Crop Sciences and Bristol-Myers Squibb in the areas of functional genomics. Please see my [resume](/cv) for specific details and work experiences.

High-throughput experimental techniques, combined with computational biology, drive functional genomics research forward. RNA-seq allows researchers to quantify gene expression changes across conditions, while chromatin immunoprecipitation sequencing (ChIP-seq) identifies regulatory elements like enhancers and transcription factor binding sites. CRISPR-Cas9 and RNA interference (RNAi) screens systematically perturb gene function to reveal essential pathways in development and disease. These methods, coupled with machine learning and network analysis, enable scientists to predict gene functions and interactions at a systems level. Functional annotation databases such as Gene Ontology (GO) and KEGG pathways further assist in contextualizing large-scale data.

Functional genomics has transformative applications in medicine, biotechnology, and synthetic biology. In precision medicine, genomic profiling helps identify patient-specific therapeutic targets, leading to tailored treatments in oncology and rare genetic disorders. In agriculture, functional genomics aids in engineering crops with enhanced resistance to pests, diseases, and environmental stresses. Synthetic biology leverages functional genomic insights to design artificial genetic circuits for applications such as biofuel production and industrial enzyme synthesis. As technologies advance, integrating multi-omics data with AI-driven analytics will further enhance our ability to decode complex biological systems and develop innovative solutions for health and industry.

I have worked in genomics, transcriptomics, cancer research, and biofuels research for 5 years of industry and 4 years of academic research to combine functional genomics approaches with computational biology to affect biofuel titers, cancer research leads, and determining targets for validation in genomics and transcriptomics investigations.


# k-mers, minimizers, and sequence alignment



