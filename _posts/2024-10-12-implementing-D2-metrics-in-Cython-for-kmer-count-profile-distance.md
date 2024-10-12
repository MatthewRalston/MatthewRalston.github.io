---
author: Matt Ralston
header-image: "/images/dna3.gif"
hero-title: What are the D2 metrics?
hero-subtitle: How do researchers compare two kmer count profiles.
category: Data-science
tags: kmerdb prose meta
---


## D2 metrics to compare sequences from kmer frequency vectors

Blaisdell, Reinert, Shepperd, and others have used D2 family metrics, among others, to compare genomic sequences from their kmer count or frequency vectors. 

It's essential for sequence comparison to adjacently/concurrently have some type of non-alignment (direct, exact solution to local alignment problems. More complex with gap-penalties) concept of sequence similarity. One method is to split the genome, or sequence of consideration, into the frequencies of words, or kmers, for the purpose of then comparing the vectors of counts as a proxy to how many words or similar substrings each sequence has. 

D2 metrics have essential features for any pairwise metric: self-normalization (D2S), and better/optimal statistical power (D2*). Note that D2 metrics have been shown to be asymptotically normal with larger and larger sequences. The puzzle piece method of using k-mer frequency vector similarity, with long sequences, may provide advantages over alignment based similarities.

More to come...

