---
author: ralston
title: What are the D2 metrics?
date: 2023-10-12 22:18:00 +0400
description: How do researchers compare two kmer count profiles.
categories: [Bioinformatics, data-science, math]
tags: [kmerdb,  prose, meta, opinion]
hidden: true
pin: false
---


## D2 metrics to compare sequences from kmer frequency vectors

Blaisdell, Reinert, Shepperd, and others have used D2 family metrics, among others, to compare genomic sequences from their kmer count or frequency vectors. 

It's essential for sequence comparison to adjacently/concurrently have some type of non-alignment (direct, exact solution to local alignment problems. More complex with gap-penalties) concept of sequence similarity. One method is to split the genome, or sequence of consideration, into the frequencies of words, or kmers, for the purpose of then comparing the vectors of counts as a proxy to how many words or similar substrings each sequence has. 

D2 family metrics have essential features for any pairwise metric: self-normalization (D2S), and better/optimal statistical power (D2*). Note that D2 metrics have been shown to be asymptotically normal with larger and larger sequences. The puzzle piece method of using k-mer frequency vector similarity, with long sequences, may provide advantages over alignment based similarities.

More to come...



## D2S


Xw is the word count, in this case, equivalent to a k-mer count from a k-mer count vector/profile. 

```
X~w = Xw - nhat*pw      Y~w = Yw - nhat*py
```

... [NOTE]: E(Xw) = nhat*pw

```
nhat = n - k
```

and then we have the revised D2 metrics. From Blaisdell 1986
```
D2S = \sigma X~w*Y~w / \sqrt( X~w^2 + Y~w^2 )

```

## D2*

The power optimized D2* statistic relies on some improvements to portability of the statistics to spaces where the D2S shows its own failings with regards to statistical power (1 - beta).

```
D2* = \sigma X~w*Y~w / \sqrt( mhat * nhat * pwx * pwy )
```


For those whose mathematics understanding may make reading the previous difficult, let's begin with D2. 


>I'll check back in on this. (3/19/25)




