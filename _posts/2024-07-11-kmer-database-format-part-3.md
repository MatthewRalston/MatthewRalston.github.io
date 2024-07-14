---
author: Matt Ralston
header-image: "/images/dna3.gif"
hero-title: kmerdb v0.8.4 (Part 3.)
hero-subtitle: Handy pre-alpha release of, yet another k-mer library for Python
category: Coding
tags: python kmers format meta
---

# Summary

A few housekeeping changes have been made to the `kmerdb` library. Most interesting is a new format (.kdbg - a De Bruijn weighted-edge list format), bugfixes, and a slightly revised usage pattern for the profile-generating command 'kmerdb profile'.

When counting k-mers, note the following NEW syntax.

```bash
# 'kmerdb profile -k' works as before


# --minK, --maxK arguments allow multiple k-mer profiles to be made simultaneously.
kmerdb profile --output-name OUTPUT_NAME --minK 8 --maxK 12 input_1.fa [input_2.fq.gz]
# Optionally, a plain-text samplesheet, with one filepath per line may be used in place of the input .fa/.fq files.

kmerdb graph -k 10 input1.fa output.kdbg
```

Additionally, bugfixes have been made throughout the matrix, distance, and other commands. (citation subcommand fixed to silence citation warnings)

Finally, the `--debug` and `--quiet` flags have been introduced throughout the various commands to simplify STDOUT and STDERR output, with a new submodule (`appmap`) added to collect useful `--debug` information prior to error.


# Introduction

The most recent additions to the library have included bugfixes and minor usage changes. The `probability` subcommand has been deprecated for now, in favor of a more comprehensive log-odds ratio test and other Markov-process related distances.

The major change has been in the information to assist the user in usage related cases. Specifically, the `help` and `usage` subcommands produce show detailed information about key parameters, usage syntax, and input/output as positional arguments.

Another change has been the addition of the `--debug` flag, throughout. Default behavior is to collect usage information prior to program exit, upon encountering an error. However, this may interfere with error handling itself, and occassionally, the error produces no visible output. The `--debug` flag overrides this default behavior, to simply throw the error itself without collecting the diagnostic information.

Having introduced these features, usage and error reporting capabilities of the suite has been improved.


# What's new

## error handling, debug, and verbosity `-v,-vv` levels

A new error handling process was added. Some may call feature. The `--debug` flag disables the feature, and does not in-fact permit debug level logging. Only debug level error handling, with no signal interception. The default error process is more feature rich, and should, on average, help the user understand the inputs and parameters involved in the error. Combine this with `-v,-vv` verbosity handling, and most errors the user might encounter should have self-referential solutions.


## verbose usage, parameter, and input/output handling. 

New subcommand `usage|help` with added program header functionality throughout. 

The wrapper wraps up schema related to the parameters, flags, and positional arguments supplied to the program.

## the `--debug` flag

The `--debug` flag disables signal interception and (*improved*) verbose error logging.

## profile subcommand changes

Changes made to the profile subcommand, including a modified usage pattern.

## the samplesheet

A single-column plain-text list of filepaths may be supplied to the profile command, instead of one-by-one at the command-line.

## --minK kmin --maxK kmax

Multiple k-mer profiles may be generated in one invocation. May be useful for some assembly processes, k-mer statistics, etc.

## -o, --output-name

A sample naming pattern for output files.

## --quiet

Faster run-time for non-production workloads.

## Most obnoxious options deprecated or excluded from usage|help

Some command-line options are not set in stone. Most have legacy or other related use cases. Included are the `-nl`, and `-l` flags, and the `-p|--parallel` flag.

## NEW format: [.kdbg], a weighted edge list

It's a columnar format, bgzf compressed again, metadata header as before. This is the prototype for a graph format, or edge, or edge-list format. Working on it.

## 4 new distance metrics

Distance metrics have been targetted for inclusion and performant compute? Not sure where I want to leave this at. We're not doing k-mer counting on the GPU. Neither memory footprint nor compute requirements necessitate that horsepower for this problem, aside from perhaps the demonstrative utility of a CUDA kernel.

Otherwise, we have Cython and Numba JIT compilation in our toolkit for handling these distances with performance in mind.

* D2
* D2S
* D2*
* D2z
* D2shepp


# What's happening?

Currently searching for work, health improvements. Revitalizing resume and kmerdb project. Bugfixes, features, some new ideas.

I'd eventually like a robust Python project skeleton and configurator.

The AppMap project is taking off nicely.

I haven't touched minikube since I moved home late last year, so that's been phenomenal.

No Arch Linux either, so that's perfect.

# What's next?


academic sabbatical. I need time to draft some new papers in promoter and terminator motif literature.

hypothesis: does enriching the promoter and motif literature add to science?

1. Paper 1: Motif structure and bias in prokaryotic pre-transcript sequences or promoters.
hypothesis: does assessing motif frequency using a combined approach of ranked and clustered motifs yield novel motifs

2. Paper 2: Terminator structural assessment and k-mer bias assessment for prokaryotic transcriptional termination regions.
hypothesis: does creating a map of terminator structure, bubble k-mer bias, hairpin k-mer bias, and terminator diversity in genus level compendiums add richness to the emicrobial ecology field

3: Paper 3: Review of k-mer motifs, distance metrics, and early-mid alignment-free listerature (no pseudoalignment yet).
hypothesis: using alignment-free approaches towards genome annotation allows analyses to be re-run as new genomic data is added, with linear time complexity, adding to the utilities of micorbial pathology and disease research physiology, microbial genomics, and whichever datasets are used in the application reports.

4. Paper 4: Application note: kmerdb
hypothesis: alignment-free methods often begin with the step of k-mer counting, when building various indices and for alignment-free methods, as well as sequence assembly.
does standardizing the k-mer library drive the knowledge of pre-computed statistics of value, by virtue of programmatic access to data, associated format interconversion utilities, and familiar programmatic access?

application note 1:
access to a variety of k-mer count data and inter-profile distances requires accessory tools to manage large alignment-free datasets, prior to sequence assembly.
By virtue of this, closer access to data such as sequence motif, or more simply 'profiles' of, genomic count indices permits the re-assessment of and improvement upon existing assemblies. K-mer counts are direct and proveably derived from the genomic datasets, presumably FastA or FastQ formatted data.
Next to this, graphs may be assembled and delivered to assembly routines, which utilize different algorithmic and heuristic approaches to making "assembled" sequences from shorter sequence reads.
Assembly algorithms might perform differently under certain genomic, ecological, or sequence repetition conditions, and assessment of available assemblies has been difficult. 

Functional genomics took the scene in 2016, as research oriented away from second-generation sequencing technologies (Illumina HiSeq and MiSeq platforms) for the sheer amount of data, and back to the characteristics of high-value sequences and their functional signatures. 

