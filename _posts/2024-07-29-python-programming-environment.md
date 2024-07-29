---
permalink: Python
title: "Python programming environment"
subtitle: "A Data Science for Python and R, statistics, modeling, calculation, algorithms, and other effects"
author_profile: true
hero_image: "dna2.png"
---

# [Python](https://en.wikipedia.org/wiki/Python_(programming_language))

The Python programming language is a dynamically typed and simple language for the x86_64 system and beyond. It has a good ecosystem for data scientists, so long as their dependencies are properly audited.

Data scientists use Python for routine programming tasks, prototyping, and even production code. It is simple to understand from most C, smalltalk, and Perl procedural/imperative styles. It has a class system and Python style often suggests Object-Oriented Programming design principles be used where sensible.

What makes Python shine, even in 2024, is the reasonable run time for most well-engineered questions, often targeting the < 5 minute to 30 minute timeframe, with rapid iteration and prototyping, testing, feedback, documentation, version control, and more.

I recommend personally to follow PyPA and PyPI conventions, PEP RFC, and Python style conventions whereever you can. Docstrings should be Sphinx compatible. Tests, `pyproject.toml|setup.py`, `config.py`, and `pytest` and `UnitTest` test compatibility.

The current flavor of configuring a virtual environment to run your Django app, build your cyclotron's network firewall, or otherwise create a tool or application for download over PyPI is to use the PyPA tool `pipenv`.

## `pipenv` - Python version and dependency management

The Python interpreter, and pip3, or other python system-level dependencies can be left to the user to install. Another 3rd party solution is [`pyenv`](https://github.com/pyenv/pyenv.git), which `pipenv` then recognizes upon reading `pyproject.toml` (`pipenv` supports PEP-621 RFC compatibility), will offer to download a local version of Python into `$HOME/.pyenv` for the user to use with a virtualenv, typically in `$HOME/.local/share/virtualenvs`.

## `pipenv --python 3.12.4`

This will create a virtual environment (`virtualenv`) for your project's dependencies in your home directory, bind the environment to the user-supplied interpreter's version, and it essentially support successful shell sessions for your Python's environment.

## `pipenv shell`

Now you're all set! Go ahead and enjoy developing with a managed Python virtual environment, courtesy of the PyPA tool `pipenv` and yours truly.

## `requirements.txt` | `setup.py` | `pyproject.toml` - PyPI package dependencies

When I started programming in Python, all pip package dependencies were stored in a `requirements.txt` and distributed with the source for install on the user system via build/dist facilties like `setuptools`, `distutils`, `wheel`, and `pip` distributed with the Python core library, and managed by the user.

Now, `setup.py` based install has been releived in favor of `pyproject.toml` and PEP-621 standard packaging and compatibility toolchains.

Let's look at some of the packages available to install with `pip install`. If you don't need it, minimize your dependencies.






## Package list

#### NumPy

```
numpy>=1.21.2

```

NumPy remains an essential tool for manipulating numbers with good (up to 64-bit) precision. 


#### PyYAML
```
PyYAML>=6.0.1
```

yep. Yet another yaml requirement


#### jsonschema

```
jsonschema>=4.17.3
```
jsonschema not because I plan on blasting this on the web, or making any APIs. Mostly, because it's a web-centric data-structure specification middleware with JSON structure and typing facilities as made possible via language-specific deserializations.


#### setuptools

```
setuptools>=69.2.0
```
I like a certain version of setuptools noted to make sure my code is compatible with other system configurations for their Python environment.

#### Cython
```
Cython>=3.0.8
```
Yes i occasionally cythonize. I don't often need the performance needed to really leverage Cythonization. I support other statically typed languages such as Haskell, Rust, and TypeScript for strong implementations with performance priorities considered.



#### BioPython
```
biopython>=1.81
```
BioPython provides some features for sequence import that are often wrapped by data-scientist and bioinformatician codebases for flexibility and interop with standard Life Science, Bio Science, Bioinformatics, and computational biology data and file formats.


#### SciPy

```
scipy>=1.7.3

```
SciPy is often used by data-scientists for some matrix facilities, distances, vector operations, SVD/PCA facilities, and more.


#### SciKit-Learn

```
scikit-learn==1.0.2
```

SciKit-Learn is used for unsupervised and supervised learning features, operations for modeling data using their implementations.

It's essential for modeling, unless more specialized tools are needed.


#### matplotlib

```
matplotlib>=3.5.3
```

Is still a relevant graphics engine. If you're interested in data-driven graphics in Python, I suggest you start here. 

#### Pandas

```
pandas>=2.2.2
```

Pandas because we don't need the performance of Polars. Pandas is a DataFrame library with ~~good~~ fair query performance, subsetting, and index-centered manipulations on a DataFrame representation of a more general matrix (such as `numpy.ndarray`).



