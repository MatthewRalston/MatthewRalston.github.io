---
author: Matt Ralston
header-image: "/images/dna1.gif"
hero-title: Benchmarking short-read aligners - bwa-mem(2), bowtie(2), bbmap, and SHRiMP
category: Opinion
tags: bioinformatics prose opinion meta
---


Short-read aligners make up the core of modern bioinformatics program technologies. The aligners are responsible for mapping (rather than aligning) short reads (typically produced by Illumina sequencers) to their most likely originating loci with gapped and ungapped, genomic and transcriptomic methods. For lists of both aligners and short-read mappers and their pros/cons, see the [Wikipedia article](https://en.wikipedia.org/wiki/List_of_sequence_alignment_software). 

# Why bother benchmarking decade old software?

The short answer is: because these programs are still heavily used in bioinformatics groups even in 2024! Short read aligners are immensely popular software with userbases in the 10s of thousands of users, and are notably fast at approximate alignment (often referred to as read mapping) to a reference genome or transcriptome.


# How this analysis works

For proper comparison, I'll be comparing 5 or 6 short read aligners, all of which can be installed using the 'Anaconda' Python environment. Install your choice of aligner as follows.

```bash
conda install -c bioconda bowtie2
```




Next check out the [Github repository](https://github.com/MatthewRalston/aligner_benchmarking). Included is a miniconda 3.12 `environment.yml` file which should recapitulate my Anaconda/miniconda environment. Also included is a shell script (-?|--help) for running the analysis. PicardTools features a command called 'CollectAlignmentSummaryMetrics' and is the simplest method to check percentage aligned in tabular format for consistent definitions of alignment across the aligners.




