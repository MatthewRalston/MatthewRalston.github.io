---
title: "kmerdb kmeans"
excerpt: "Run k-means clustering on Pandas dataframes from the command-line"
collection: portfolio
---


Standardizing on int64 for counts, kmerdb provides access to two k-means methods in the Python ecosystem: scikit-learn, and biopython.

Using k-means on k-mer count matrices, say on the first and second principal component of the artificial metagenome may reveal groupings of interest and other spatial characteristics of use for adjacent and concurrent analysis on hierarchical structures of the species diagram. Of course, more value is gained on large (30-200+ species) metagenomes.

This subcommand of the Python Package Authority (PyPA) package `kmerdb` writes/reads Pandas DataFrames from STDIN/STDOUT, and produces matplotlib graphics alongside the k-means elbow diagram choices (if k is not provided), and choice of k and principal components to provide for k-means clustering and visualization.



```bash
kmerdb kmeans -k 4 kmer_count_matrix_after_PCA.12.tsv
```



