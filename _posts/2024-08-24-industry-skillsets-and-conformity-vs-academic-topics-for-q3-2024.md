---
author: Matt Ralston
header-image: "/images/dna2.gif"
hero-title: Industry skillsets vs academic topics for Q4 2024
hero-subtitle: What topics are the focus for the near future?
category: Opinion
tags: linear_algebra metagenomics meta
---


# What topics are currently under focus?

I am building fundamentals in linear modeling, from multiple perspectives. Linear algebra, regression, decompositions, matrix multiplication, the statistics of regression, different forms of relevant adjacent and normal equations for regression. The thoughtprocess of the linear modeling problem. Covariate elimination using analysis of variances (ANOVA) and lasso. Ridge regression is a briefly studied and more edge-case for regression. I'd like to learn about canonical correlation analysis and other methods.

The objective of the regression focus is to perform compositional analysis on populations of bacteria represented in NGS datasets.

The approach used will be some hybrid of Cython, NumPy, CuPy, cublass-gemm, and Strassen multiplication. Under 200, I want to do Strassen on CPU. Over 200, I want to use cublass-gemm completely.


# Why the sudden shift of focus?

Mostly a documentation and capture issue, but an old focus of the library was metagenomic applications and not just genomics and pure EDA. A shift of focus could address this tastefully and briefly without reorganizing too much time into initial implementation.


# What is the scope and how about time estimate?

The scope is the Strassen multiplication, the regression and delegations, numpy cpu inversion, and then Strassen, numpy, or cublas-gemm mult. Cublas doesn't look extraordiarily viable, although only an hours woth of tinkering with chatgpt suggests that it is extraordinarily version dependent. I'd like to stick with numpy-blas delegated cpu matrix products for now. Othr options yet unimplemented include different NumPy mediated BLAS/LAPACK, IBM mlk, or other system linear algebra toolkit multiplications and then finally, the Strassen multiplication. I might decide to delegate (4x4 ...) 3x3 or 2x2 matrix multiplications to NumPy beneath the Strassen implementation for speed. I might also produce additional wrappers with different styles of delegation and/or choices for implementation, but GPU multiplications don't seem to be necessary at speed for any reason, nor do the multiplications seem necessarily amenable to on-GPU calculations.

# What obstacles are there so far?

I'm having some issues with implicit or not-yet-obvious type conversions between C objects, Cython, and Python. Also, one or more libraries are cimported incorrectly. There are some general syntax issues. But the biggest obstacle is the Python-Cython transition without familiarity with sources of relevant documentation.


