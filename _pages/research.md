---
permalink: /research
title: "Genomics and transcriptomics research"
author_profile: true
hero_image: "images/dna1.gif"
---

{% include page_header.md %}

My research experiences can be divided into two categories: industry research experience and academic/personal research questions. For the former, my industry experience revolves around the use of databases, web applications, UI/UX, and high-performance computing (HPC) resources to develop best-practices for modern data-science projects and software deployment stacks. 


For an example of current (2015-2022) experiences in genomic and transcriptomics technologies, let me discuss RNA-seq briefly. I have done RNA-seq in industry from Illumina sequencer automation and read quality assessment to alignment qualities and quantification (read count estimation, normalization, and variance reduction) techniques. I have done linear regression modeling using a variety of techniques, and my graduate level maths understanding covers topics from Bayesian statistics, probability, frequentist statistics, ANOVA, regression model testing, machine learning, and more. An additional industry topic among others I've done along the way in cheminformatic and bioinformatic engineering and discovery settings includes functional genomics and metagenomics research at Bayer Crop Sciences. While there, I developed a cloud computing pipeline for the assembly of microbial genomes from metagenomic samples and the assessment of genome completeness, metabolic functionality, and novel metabolite/cofactor synthesis presence/absence for use in crop treatment studies.

In academic settings, I've researched three topics. Cancer physiology and pathology (UD, Helen Graham Cancer Center's Center for Translational Cancer Research (CTCR)), microbiological physiology and stress tolerance mechanisms for biofuel development, and finally sequence alignment algorithms and their utility in addressing the genomics of inheritance and evolutionary relationships of genes via paralogy and orthology.


## Transcriptomics | RNA-seq data pipelines

RNA sequencing (RNA-seq) pipelines are essential for transcriptomic research, enabling the quantification and analysis of gene expression across different biological conditions. Published and often standaradized approaches, such as those used in The Cancer Genome Atlas (TCGA), incorporate tools like Bowtie2 for read alignment and Limma for differential gene expression analysis. Bowtie2 is a fast and memory-efficient aligner that maps short reads to a reference genome quickly with good standards for 'mapq' mapping quality reporting to ensure accurate representation of transcript abundance. Alternate short read aligners such as HISAT2, STAR, and others continue to be made, each with pros and cons to memory usage, accuracy, and compatibility. Limma, originally designed for microarray data, has been adapted for RNA-seq to model gene expression changes using empirical Bayes methods for regularization, improving statistical power in differential expression analysis. These tools, integrated into comprehensive workflows, help researchers uncover insights into disease mechanisms and gene regulation.

The RNA-seq analysis pipeline typically follows several key steps: raw-read quality control, alignment, alignment quality control, quantification, normalization, sometimes regularization, and finally hypothesis testing via differential gene expression analysis. Initially, raw reads undergo quality assessment using tools like FastQC, followed by adapter trimming and filtering with Trimmomatic. High-quality reads are then aligned to a reference genome using Bowtie2 or STAR, generating alignment files that are processed for gene-level quantification using featureCounts or HTSeq. Normalization methods, such as TMM (trimmed mean of M-values) in Limma or median of ratios in DESeq2 adjust for library size differences before differential expression analysis. Finally, statistical models in Limma, DESeq2, or edgeR identify significantly differentially expressed genes, often visualized through heatmaps, volcano plots, and pathway enrichment analyses. These steps ensure rigorous and reproducible RNA-seq data analysis, facilitating discoveries in transcriptomics and precision medicine.

I have built pipelines for professors and corporate partners internally and externally to my role in the Integrative Genomics group in Bristol-Myers Squibb's Discovery Biology department. Utilizing the best methods in clinical transcriptomic research, I have added value to differential gene expression (DGE) projects by building and validating data pipelines using bash, Nextflow, CWL, Galaxy, and more. I have automated sequencer-to-data-pipeline processes by monitoring Illumina buckets for new files, and launching the pipeline automatically following a sequencer runs completion. Utilizing the best in R and Bioconductor statistical analysis packages, I have created amazing QC reports including heatmaps and diagnostic outputs from sample covariates and other design matrix variables.


## Functional genomics


Functional genomics is a field of research focused on understanding the roles and interactions of genes within biological systems, often using high-throughput techniques such as RNA sequencing (RNA-seq), CRISPR screens, and proteomics. Unlike structural genomics, which emphasizes gene mapping and sequencing, functional genomics aims to determine how genes contribute to cellular processes, phenotypes, and disease states. Key approaches include transcriptomics to study gene expression, epigenomics to examine regulatory modifications, and metabolomics to assess biochemical changes. By integrating these data, researchers can uncover gene regulatory networks and identify biomarkers for diseases such as cancer and neurodegenerative disorders. I have worked with both Bayer Crop Sciences and Bristol-Myers Squibb in the areas of functional genomics. Please see my [resume](/cv) for specific details and work experiences.

High-throughput experimental techniques, combined with computational biology, drive functional genomics research forward. RNA-seq allows researchers to quantify gene expression changes across conditions, while chromatin immunoprecipitation sequencing (ChIP-seq) identifies regulatory elements like enhancers and transcription factor binding sites. CRISPR-Cas9 and RNA interference (RNAi) screens systematically perturb gene function to reveal essential pathways in development and disease. These methods, coupled with machine learning and network analysis, enable scientists to predict gene functions and interactions at a systems level. Functional annotation databases such as Gene Ontology (GO) and KEGG pathways further assist in contextualizing large-scale data.

Functional genomics has transformative applications in medicine, biotechnology, and synthetic biology. In precision medicine, genomic profiling helps identify patient-specific therapeutic targets, leading to tailored treatments in oncology and rare genetic disorders. In agriculture, functional genomics aids in engineering crops with enhanced resistance to pests, diseases, and environmental stresses. Synthetic biology leverages functional genomic insights to design artificial genetic circuits for applications such as biofuel production and industrial enzyme synthesis. As technologies advance, integrating multi-omics data with AI-driven analytics will further enhance our ability to decode complex biological systems and develop innovative solutions for health and industry.

I have worked in genomics, transcriptomics, cancer research, and biofuels research for 5 years of industry and 5 years of academic research to combine functional genomics approaches with computational biology to affect biofuel titers, cancer research leads, and determining targets for validation in genomics and transcriptomics investigations.

## Statistics, data science, ML, AI

[Data science](/data_science) and machine learning are fields involving linear algebra, probability, calculus, geometry, computer science, and statistics in the pursuit of predictive and explanatory models. Classical hypothesis testing remains in use in much of natural sciences research, including FDA regulated pharamaceutical research. 

Datasets are becoming more and more integrated, voluminous, and cumbersome for analysis and interpretation in modeling efforts. For the purposes of modeling, many techniques are available for different datasets and distributions of the underlying variables. Without going into detail, I will say that my experience in the field largely revolves around 3 areas: programming, data-science, and statistics; literate programming, visualization, and modeling; and full-stack application development, including exploratory data analysis and dashboards.

By combining prototyping with Python and the power of SQL, I can usually find a data model that is consistent and useful for the purposes of producing reports, graphics, and `git` repositories of code, analyses, and notebooks, or, for creating a full-stack web application for deployment on cloud or company intranet. When required, I can do extensions in Cython, Rust, or other languages for the purposes of efficient compute and stack-heap allocations.

With the advent of the CUDA language for GPU compute, neural networks, and machine learning, the possibilities are kind of endless. The typical constraint is time and ideas for the development workflow.


## k-mers, minimizers, and sequence alignment

Sequencing technologies are revolutionizing pharma, biotechnology, and disease pathology research. By sequencing mRNA molecules and interpreting their abundances, we have a *proxy* measurement for gene expression. I say proxy because true gene expression is determined primarily by the levels of proteins available in the cell to perform their enzymatic, signaling, or other functions. However, proteomic technologies including mass-spectrometry and quantitative 2D PAGE are still in their infancy, and determining these levels is considered difficult given the stochastic nature of both transcription rates and translation rates.

However, when we reverse transcribe mRNAs into cDNAs and sequence the abundances of the cDNAs using RNA-seq techniques we gain insight into the *dynamics* of gene regulation, not just temporaly, but also with respect to the systematic nature of gene regulatory dynamics. With sequence alignment, the sequenced mRNA framents, born from electrochemical or other fragmentation methods, can be mapped to their most likely locations in the genome with short-read aligners, modern day versions of the historically used alignment algorithms:  Needleman-Wunsch (approximate global alignment) and Smith-Waterman (near-optimal local alignments). Modern aligners and short-read 'mappers' make heavy use of k-mer and so-called 'minimizer' (k-mer count array subset) indexing methods to calculate likely 'seed' locales between two sequences. 

Research into k-mer count array generation largely revolves around efficient methods (online methods, precomputed, approximate structures i.e. bloom filters) for generating these vectors for use in the minimizer selection process and the data structures stored on disk and in memory for rapid access to the seed regions for use in alignment/mapping. 


K-mer count vectors are also becoming useful in approximate and probabilistic quantification methods, often called 'quasi-mappers' or 'pseudo-aligners'. These trending methods again rely on k-mer count vectors and approximate data structures for determining associations between the short reads, their k-mer compositions, and candidates for alignment from the reference genome or transcriptome.

To further research the utility of k-mers in sequence alignment, quasi-mapping, and transcriptomic quantification, I have developed a k-mer counting library called [`kmerdb`](https://matthewralston.github.io/kmerdb). The `minimizers` function is completed and `alignment` functionality is on the way.

