---
layout: post
author: Matt Ralston
header-image: "/assets/images/blog/code_syntax/feature.jpg"
hero-title: Kmer Database Format (Part 2.)
hero-subtitle: Update to format specification, CLI, and library features/architecture
category: Coding
tags: python kmers format meta
---

# Summary

* Metadata spec modified to include NumPy 'dtype' metadata and interpretation in the parser.
* 80-bit floating point precision added to custom Pearson correlation coefficient floating point accumulation to a scale of 0-1 from over 16M digits with precision.
* unsupervised machine learning (clustering, dimensionality reduction) capacities 
* Format aggregation utilities (gather spectra/profiles into a table, calculate distances between columns of a profile matrix)
* distance matrix generation includes 20+ distance metrics, including custom Cython implementation of a Pearson correlation coefficient.


# Introduction

To understand the core concepts behind kmerdb, I'd refer the reader to the original blog post on the subject described [here](https://matthewralston.github.io/coding/2019/08/26/kmer-database-format-part-1/).

Since then, there has been an update to the core architecture of the library, CLI, supported format, and designed workflows. Principally, the profile is essentially a k-mer count vector, that can be compared to other related or similar profiles.


# What's changed?


### Format

The core format has changed, with some more formalisms. The original implementation (prior to perhaps 0.6.5) used a sigle count column, along with the row number. The file was not sortable, could not support either/both integer counts and normalized decimal frequencies.

The new format features a four-column standard. The first is always the row number, the second is the row number of the original. This is ascending in the standard sort order, and would thus be identical to column 1 in many scenarios.

The third and fourth columns are integer count and floating point frequencies, with NumPy numerical 'dtype' encoding strings included in the metadata.

This provides more formalism of the format to the interpreter and supports reduced memory footprint (efficient) encodings for large datasets.

The user, as always, is still bound much more (exponentially so) by k to the degree their machine will have memory for the sort index, count, and frequency columns.

That being said, the option for 32-bit unsigned integer or float encodings may help reduce the memory footprint in certain scenarios.

### `kmerdb matrix`

The matrix command has been built out considerably, with the option to "pass" the *count* matrix without any transformations. The frequency matrix is typically not used directly from frequencies in the file. Those are provided to the user for their convenience.

The count matrix itself can be normalized or not (passed) and then passed down to other dimensionality reduction steps, used for distance matrix generation, or for clustering.

This matrix sub-command in the kmerdb suite is the center for PCA and t-SNE dimensionality reductions, as well as DESeq2 normalization of the count vector.


### `kmerdb distance` Cython extension and measures of correlation

In the distance sub-command, the custom Pearson correlation coefficient (Pearson's r, with rho as the population correlation coefficient) has been reworked as a Cython extension.

Essentially, the Pearson's r statistic is computed serially by summing/accumulating very small floating point numbers in an 80-bit floating point Cython datatype.
This provides "reasonable" performance for fairly low k (8-15). Recall that stability of summations is inversely related to the number of summations (n).

For certain larger choices of k, 80-bits may not be sufficient to produce Pearson r with reliability (correlations over 1 are a good example).

That being said, this new Cython extension is available as the 'pearson' distance in the distance matrix subcommand. 

The SciPy correlation distance remains available, as well as the Spearman rank correlation coefficient.




# Rust experimentation

I have a version of kmerdb head and view prototyped in Rust, and I'd be interested in porting the project over at some point, time permitting.



# Future Work


I'd like to add an option to better support artificial metagenome composition: cofactors file with row number equal to either single fasta file sequence count OR fasta input file array size
Essentially there are two modes already in kmerdb: single fasta file or multiple. In the case of the former, the cofactors file's row number must be equal to the number of sequences in the single fasta file.
In the other case, the cofactors row number is equal to the number of input fastas.
I'd like to form a profile decomposition into a linear regression problem. In more biological terms:
I'd like to add a regression module to decompose an (artificial) metagenome's composition into percentages. Regressing a model like this, in an exponential space of data points, could require GPU support, and will .
I'd like to add UMAP into the list of supported transformations for dimensionality reduction.
I'd like to add hypothesis testing on samples specified with null hypothesis \$$ H_{0} | r = 0 $$, so that profiles with positive or negative correlation, and thus potentially confounding factors can be identified.
I'd like to add Neo4J support so that the graphical portions of the problem can be refactored into CYPHER queries (we choose Neo4J instead of Amazon Athena and RDF oriented solutions)
I'd like to make the Neo4J the official graph database for the deBrujin graph representation.


We can redefine the role of kmerdb to be a wrapper for basic arithmetic, statistics, and data science around k-mer profile vectors designed to ingest and import the data into a graph database solution like Neo4J.


