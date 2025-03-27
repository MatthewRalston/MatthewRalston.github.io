---
author: ralston
title: Notes on runtimes... not working on this.
date: 2025-01-02 20:17:00  +0400
description: Data, mapping, linear, graphical, quasi... quas my...
categories: [Opinion, Software]
tags: [kmerdb, prose, software, meta]
hidden: true
pin: true
---


I don't want to discuss linear runtimes and what that means in alignment-free methods for bioinformatics and sequence alignments and quasi alignments. First, it is the splitting of the sequences, as they are read, into, let's say, graph-like table. Not a real graph actually... those are for real programmers and not for drop-out, fail-out, slime-mold swamp dwellers. Especially those that try to fit into smart people habits to feel cool. No sarcasm. This graph consists of the k-mers, their neighborhoods, and of course the walks or paths through the graph that constitute optimal criteria and local maxima of course for traversal and contig/walk/path maximization. Typically, a search through the De Bruijn structure may be Breadth-First to find optimal depths for traversal of the path through the De Bruijn structure, optimizing for creating some sequence. But... we don't know how to implement this actualy and research is ongoing for some of the brightest minds.. and just makes people like me drool. But in theory... it could lead to read collapse along the sequence unidirectionally (bidirectionally in a unidimensional space) along the sequence space. Someday, sequencing technologies will be viable for use irl, maybe commodity by 2027? When it does...oh boy! They're gonna pay me!

The linear runtime is observed thanks to the profile being generated <i>a priori</i>, and then passed to aggregation and calculating functions, which only require the count vector, until the concept of the matrix launches agent smiths in super-linear runtime and polynomial runtimes of matrix operations. Linear runtime being perfect maps or transformations on the data of interest. The matrices transformed with linear mappings, such as through creating distance functions, tend to have linear or better bounds, possibly constant. Polynomial runtimes include regression, least squares, and other matrix-multiplication requiring algorithms.

The linear runtime is observed by virtue of a single dimension being created at once from the inputs. The linear runtime is by virtue of the single De Bruijn graph mapping itself to some feature dimension during calculations or functions mapping the puzzle pieces to their associated locations in a transcriptomic or genomic fasta feature space.


