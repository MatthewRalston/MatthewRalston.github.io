---
title: "kmerdb - k-mer profile distances, clustering, and more"
excerpt: "kmerdb is a PyPI project for assessing inter-sequence k-mer profile distances, de Bruijn grpahs, and more. <br/><img src='/images/kmerdb.gif'>"
collection: "portfolio"

---




[![KmerDB tutorial](/images/kmerdb.gif)](https://github.com/MatthewRalston/kmerdb)

`kmerdb` is a PyPI Python package designed to quickly generate k-mer count profiles from sequencing data. Input can be `.fa` or `.fq`, and gzipped inputs are supported.

Distance metrics are provided by SciPy, with the exception of the 'pearson' distance, which uses the canonical formulation of the correlation coefficient and is written in Cython. Inputs to most downstream commands may be plain .tsv, and Unix piping from standard input is also supported.

When designing this command-line interface (CLI), additional metadata concerns were in mind. How many unique k-mer counts vs total k-mer counts were processed (i.e. was the 5-mer 'ACAAT' seen at least once? If seen 0 times, then we define it to be a nullomer.) A YAML-format metadata header is provided alongside the k-mer count vectors to provide summarizations at-a-glance to researchers, conveniently at the top of the compressed file.

The file is `gzip` or `zlib` compatible and is otherwise a plain tab-delimited text file under the block-GNU zip file compression, just below the YAML header. `view` and `header` functions are provided to quickly access file contents of both `.kdb` count profile and `.kdbg` weighted edge list formats.


## Links

* [Main page](https://matthewralston.github.io/kmerdb)

* [PyPI project](https://pypi.org/project/kmerdb)

* [GitHub page](https://github.com/MatthewRalston/kmerdb)
