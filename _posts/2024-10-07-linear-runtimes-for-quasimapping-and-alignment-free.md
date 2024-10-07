---
author: Matt Ralston
header-image: "/images/dna2.gif"
hero-title: Linear vs polynomial runtimes in count vectors and count matrix transformations and functions.
hero-subtitle: Data, mapping, linear, graphical, quasi...
category: Opinion
tags: kmerdb prose meta
---


I want to discuss linear runtimes and what that means in alignment-free methods for bioinformatics and sequence alignments and quasi alignments. First, it is the splitting of the sequences, as they are read, into, let's say, 'a' De Bruijn graph. This graph consists of the k-mers, their neighborhoods, and of course the walks or paths through the graph that constitute optimal criteria and local maxima of course for traversal and contig/walk/path maximization. Typically, a search through the De Bruijn structure may be Breadth-First to find optimal depths for traversal of the path through the De Bruijn structure, optimizing for creating some sequence. This leads to read collapse along the sequence unidirectionally (bidirectionally in a unidimensional space) along the sequence space. 

The linear runtime is observed thanks to the profile being generated a priori, and then passed to aggregation and calculating functions, which only require the count vector, until the concept of the matrix in linear runtime and polynomial runtimes of matrix operations. Linear runtime being perfect maps or transformations on the data of interest. The matrices transformed with linear mappings, such as through creating distance functions, tend to have linear or better bounds, possibly constant. Polynomial runtimes include regression, least squares, and other matrix-multiplication requiring algorithms.

The linear runtime is observed by virtue of a single dimension being created at once from the inputs. The linear runtime is by virtue of the single De Bruijn graph mapping itself to some feature dimension during calculations or functions mapping the puzzle pieces to their associated locations in a transcriptomic or genomic fasta feature space.


