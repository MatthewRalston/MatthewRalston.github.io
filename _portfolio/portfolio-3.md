---
title: "kmerdb PCA"
excerpt: "Run PCA on int64 matrices from the command line."
collection: portfolio
---


Standardizing on int64 for counts, kmerdb runs principal components analysis on matrices to create the metavariables, the principal components, focusing on those with the highest proportion of variance.

This subcommand of the Python Package Authority (PyPA) package `kmerdb` writes/reads Pandas DataFrames from STDIN/STDOUT, and produces matplotlib graphics alongside the dim. reduced output.



```bash
kmerdb matrix PCA input1.tsv
```
