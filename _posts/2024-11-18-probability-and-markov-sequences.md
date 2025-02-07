---
author: Matt Ralston
header-image: "/images/dna2.gif"
hero-title: What are Markov sequences and why do they matter for biologists?
hero-subtitle: Markov chains are fundamental abstractions/analogies for biologists. This posts explains why
category: bioinformatics
tags: prose bioinformatics meta
---


## The interesting macromolecules inside a cell are sequences


Most biologists have some experience thinking of various sequence representations of macromolecules inside plant, animal, and human cells. The analogy is quite intrinsic to DNA, RNA, and protein sequences, which make the machines, barriers, converters, enzymes, and other microscopic machines that can be labeled and observed inside of cells with modern microscopes, such as the fluorescent microscope.

What is a sequence and why does it matter?

A sequence is a series of molecular 'monomers' or single, atomic (inseparable) components, that, when connected, perform important functions of DNA or their counterpart protein machines.  The first sequence of a protein molecule, is typically methionine, and is encoded by the 'start' codon ATG in DNA sequences. By encoding 'start' buttons, signals, or what analogy makes sense to you, the cell encodes the coordinates of the beginning of a useful gene's protein coding sequence into the DNA segment comprising the gene. When a certain machine (RNA polymerase) or complex of machines 'feels' certain signals in the DNA, it locks into the DNA grooves, unwinding the DNA from double stranded DNA into separate and complementary sequences, one of which has the correct direction for the RNA polymerase (a RNA producing enzyme, involved in a complex) to start reading and producing a single strand of RNA that also carries the code for the desired protein. Eventually, this RNA is read by another machine known as the ribosome. The ribosome is a molecular complex of rRNA, tRNA, and proteins that can convert this intermediary coding 'messenger' mRNA into a chain, or sequence, of amino acids.

Eventually, the thermodynamic properties of the amino acid sequence's exposed R groups (the unique parts of each monomer) result in a 'folding' effect, that turns a 1-dimensional sequence of amino acids, into a 3D structure, with shapes, grooves, and a really unique structure that interacts with other proteins, DNA or RNA, or sugars, vitamins, and other molecules to produce 1000s to 100's of thousands of unique molecular machines inside the cell.


Interesting side note: my thesis project concerned a specific type of molecular machine called the heat shock proteins. When the temperature rises beyond a certain point, the energy level of all molecules inside the cell, results in thermal exchanges that disrupt the normal assembly or 'fold' of many proteins in the cell, disrupting proper function which may result in cell death. Chemical disruption (like alcohol) can cause similar effects, by changing the way the amino acids within a protein interact with each other in the normal fold. 

Cells adapt to this 'stress' by creating heat shock proteins and associated responses. These proteins desperately try to correct the fold under more mild stress conditions, and help extend the life of a cell under mild stress conditions, to what would otherwise be extremely disruptive: the heat or chemical stressors.

## What are sequences in more general terms?

Sequences are often thought of as discrete events, connected to the preceding event, one after the other, from some distribution of events that is goverened by the system of study. So, say you are rolling dice. The first roll produces 1, the second 4, and so on. The chain of rolls is a sequence, and in this case, assuming a fair die, the rolls or events are independent and identically distributed (iid), where no prediction can necessarily be made by just the preceding roll. The events are said to be independent. 

Okay, so far so good. But how do we make use of sequences if the events or atoms of the sequence are always random?

They aren't always random, but they aren't always completely dependent (on the preceding event) either.

In sequence biology, I study DNA sequences and I am trying to create a test of the likelihood of a sequence compared to a dataset of sequences. Phrased a different way, "how likely is this sequence to belong to this organism?" Or "how does this sequence's composition tell us something about where it came from". In a laboratory, you would sequence a sample, such as a SARS Coronavirus after isolating the Coronavirus RNA. After sequencing, you 'align' the sequence against a database of known sequences, typically from the NIH. This alignment produces a neighbor to the p-value, known as the E value. The e-value attempts to address the likelihood of a match of two sequences. I've been taught to parrot the following. The E value is a probability (a value from 0 to 1) that shows whether or not the test statistic (associated with the E-value, the query, and the database) may be as extreme or more extremely rare than what is expected by the null model. The null model, for those who are curious, is an essential part of every statistical test. 

A short and trivial example follows:

Say you have a database of sequences of ACTG repeated. Now you have another database of AATT, repeated as well. Is the sequence ACTGACTG likely in the second database? Not so much. If it consists entirely of A's and T's, the E-value will be very large, near 1. The first database exclusively contains ACTG, so the e-value will be very low, near 0. 


The exact value of the E-value depends on the alignment algorithm, and how it produces its score for exact or near matches. Influencing parameters include the match score, the mismatch score, and gap penalties. Substition matrices also influence the score.


## What does this mean for the average biologist?

For one, it means that you should understand the substitution scoring mechanism involved, whether the sequence is protein or DNA, and what the effect of the gap means on an alignment score. A low e-value *could* mean a strong match, and an organism that is likely to have produced the obsereved query sequence. It could also mean the parameters of the alignment were too lenient, or other bias. 


Let's say a sequence ACTGACTG is divided into segments of 3 bases, ACT, CTG, TGA, etc. Now, all of these 3-mers have associated frequencies in the database. Under the null model, perhaps all the sequences are *uniformly* distributed, they have equally likely frequencies. The associated markov probability would be the product of the 8-3+1 = 6 3-mer's equal probabilities. That's not a very realistic null model, and real world databases would have frequencies representing the observed data. You would compare the markov probability of the sequence vs the null model as a ratio: the likelihood ratio or odds ratio, comparing the query over the known data. A ratio greater than 1 suggests that the query is likely, given the data. Is it likely enough? A ratio less than 1 suggests that the query is very implausible, given the data.

This is the topic I have been developing alongside of my software.

