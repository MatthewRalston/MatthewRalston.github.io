---
permalink: /data_science
title: "Statistics and Data Science"
author_profile: true
hero_image: "images/dna2.gif"
---

{% include page_header.md %}

## Data science experience

I'm a data professional that focuses on the **statistical analysis of data** using regression and probability techniques, machine learning, and [other methods](/about#skills) particularly on genomic sequences and experiment datasets. I turn DNA sequences into count vectors of DNA subsequences for use in alignment, k-mer compositional analysis, overrepresented motif analysis, De Bruijn graph formation, or total count vector based differentials on sequences or assemblies.

In addition, I turn alignment abundances into digital readouts of **gene expression** for use in downstream analysis such as differential gene expression comparisons, **whole transcriptome interpretations** of gene representation and functional ontologies such as metabolic enzyme representation, transcription factor and **cell signaling and pathway representation**, ortholog (gene families) and paralog (related functionality via duplication) gene family completeness and genome completeness. 

So in addition to functional metrics such as the ontologies and their statistics, the alignment abundances, referred to as read counts, provide abundance approximations that are integral to variance estimation among replicates of a given condition and its use in a variance modeling and hypothesis testing framework like DESeq2 and limma. 

There are 3 success factors (KPIs) that must be measured for the goal of your project: the dataset's design, the modeling method, and "other" factors resulting in sample quality loss or sampling success when considering conclusions of the modeling process. 

When describing the data one takes an exploratory flavor when initially contaminating your dataset with inspection. You might try a correlation matrix plot (the default functionality of an organized dataset in base R's `plot` function) to start with to initially discover trends that may be causal or uncausal between your dependent and independent variables and then further exploring variance through formal distribution fitting and testing frameworks to determine which hypothesis tests may be appropriate for use in explanatory reporting.

## What is data science


Data science is an interdisciplinary field that combines statistical analysis, probability theory, and machine learning to extract insights from structured and unstructured data. Python is the dominant programming language in this domain, offering powerful libraries such as NumPy for numerical computations, pandas for data manipulation, and scikit-learn for machine learning. R is another widely used language, particularly valued for its statistical modeling and visualization capabilities, with packages like ggplot2, dplyr, and caret. These tools enable data scientists to preprocess data, perform exploratory data analysis (EDA), and apply statistical techniques to uncover patterns and relationships within datasets. Modeling is the name of the game in good research practices and producing clear and reproducible protocols for assessing and modeling associations between experimental variables.

Probability and statistics form the foundation of data science, underpinning key methods for data interpretation and decision-making. Probability distributions, hypothesis testing, and Bayesian inference are essential techniques implemented using NumPy in Python and base R or the stats package. For performance optimization, Cython can be used to accelerate computationally intensive statistical operations by compiling Python code to C-like speed. Machine learning builds on these principles, leveraging algorithms such as regression, decision trees, support vector machines, and neural networks to make predictive models. With NumPy for matrix operations, Cython for performance enhancements, and R for statistical rigor, data scientists can efficiently analyze large datasets, optimize models, and drive insights in fields ranging from finance and healthcare to artificial intelligence and scientific research.


## How does data science affect me?

If you work in industry as a technologist, or adjacent to technology concerning the collection and analysis of data in the knowledge economy, then you are likely effected in some way by data science. Machine learning and statistics are at the core of modern cancer treatments, weather modeling, geospatial data concerning agriculture, research and development of technologies, products, and pharmaceuticals. The list goes on. You are likely impacted by the data science at the core of the development of artificial intelligence and its impact on the American worker. 

Whether or not you work with data in some capacity, modern data science methods such as deep learning, pattern recognition, and support vector machines have large reaching impacts on our everyday life.


## What does data science look like in practice?

Data science is an interdisciplinary field leveraging programming, data structures and algorithms, statistics, and machine learning to produce insights or models concerning the response of dependent variables to independent variables. Feature engineering is the art of "manipulating" data to produce novel or effective covariates: response variables that are measurable and/or derivable from existing datasets. 

By leveraging programming and algorithms, in practice, most problems concerning instrumental read outs are addressable with statistics and data science to produce models that are informative (addressing variation) or predictive in nature. Typical introductory concepts include normalization, type I/II error, positive predictive value, false discovery rates, and regularization. 

By leveraging Linux computational infrastructure using shell scripts as glue code, Docker containers for reproducible builds, and Python/R/Rust programming for data manipulations, algorithms, and modeling, many problems in the knowledge economy are addressable with never before seen parallelization.

## How does data science relate to software engineering

Data science is a facet of software engineering releated to the processing of data and it has "stacks" like every other field of software development. The current "stacks" are an experience of access to the ecosystem, typically [anaconda.org](https://anaconda.org) or the Python Package index, algorithms written and distrubted via the rust community's "crate" ecosystem, or the Java ecosystem (Sun/Oracle) or 'big data' and beyond stacks dedicated to cloud technology stacks, and form-for-purpose systems related to the corporate internal and external server experiences.

Data science is a fundamental component of businesses, government, research and academia. By leveraging certain architecture concepts for internal or external cloud contracting, you may gain access to amortized costs, simpler backup-deploy-scale experiences for the development team, and better conclusions from your data science and learning teams. 


## Software engineering conventions in data science

Data science teams should always consider the security, completeness, and efficacy of their deployments into their data science environment. I leverage and contribute to internal docker repositories with documentation, commented code, and audit-friendly coding styles consistent with PEP standards or `rust` release standards. 

I dockerize my dependencies to make them host agnostic, and contribute source code tarballs as releases on company `git` servers. I comment my code, produce production `README.md`s, produce usage and feature documentation in Markdown, LaTeX, or Pandoc standard formats, and produce user facing websites to ensure my code has a powerful interface for users. 

I use either a kubernetes based data science stack, Nextflow/CWL/WDL, or a similar deployment and maintainance standard such as classical full-stack app (NodeJS:MEAN/MERN/MVRN or Python Django/Flask/FastAPI + HTML5/HTMX/CSS/JS application stacks Tailwind/jQuery) with REST-APIs, UI/UX, databases, migration schedules, and backup policies to test and validate methods for data-science workflows. The prototyping nature of using an interpreted language and a classical Javascript stack allows me to respond rapidly to changing requirements or parameterization of an application interface (the API). 

Other teams use Docker in their workflow tools, typically enterprise software stacks with similarity to cloud deployments. You put the application specific code from your developers in proper Linux source install experiences, Dockerize the dependencies, and launch the application in your fit-for-purpose internal or external cloud services provider's experience for running the container-based architecture.

## Statistics

My knowledge of statistics extends to the use, interpretation, and quality of ordinary and nonordinary (OLS) regression models, ANOVA, F-test, clustering, I use R packages for regression trees. I use machine learning and statistics workflows in R where possible, and otherwise use programming languages (Python/bash/R) in pipeline steps or otherwise use a compiled language after prototyping.

I implement custom probability feature variables in Python typically. It's fast enough and **until** you implement in Rust during scale-up I'm typically assembling the data processing workflow via steps written in shell with the necessary dependency environment available, and sometimes I run these steps as Docker containers in a formal workflow environment.

Otherwise, I typically use fit-for-purpose software for a modeling task in R or otherwise on Linux systems.

## Machine learning

Machine learning facilities are typically offered in one of two ways. The first is as a package provided for the user via some package management system such as PyPI, conda, npm, cargo, etc. The second is as a complete full-stack application with some components written in a core machine learning language such as CUDA, or for interface access to core machine learning libraries via C/C++ such as OpenBLAS or LAPACK. I do both. When writing a core alogrithm with needs for access to LAPACK or CUDA, I tend to prototype in a language with a good C compiler such as zig, Rust, or CPython. When doing the former, like writing a step to parse or collate or convert data, I use containers with the relevant wrapper code to launch and assess the individual machine learning, statistics, or data tool. That's how I assemble machine learning pipelines.

## Artificial intelligence

I am a AI user, and I use it for templating, methods research, reference aggregation, and some UI related tasks. 

I don't have a strong question about AI or the ethics of its use. To me it's a search engine generally speaking, with some facilities for providing better context more quickly to the research experience. I tend to use a mixture of Claude, OpenAI, Gemini and others. I use openai-4o-mini in production with `zed` to describe an algorithmic approach or some facet of a larger data science stack. I typically use this alongside Emacs for integrations.

I don't let AI write my code for me, and I am proficient in Python, familiar with Rust, Scala and to a lesser extent Haskell, and I write many languages of different programming paradigms. I am a bit of a functional programming and metaprogramming geek, and I also enjoy or understand the application of inheritance, encapsulation, abstraction, and polymorphism.

[`kmerdb`](https://github.com/MatthewRalston/kmerdb) is a 100% AI-free repository of a aligner/DeBruijn graph project I started writing in 2018-2020 prior to the advent of modern AI tools such as copilot, OpenAI, and others. 






## How do you approach a data science problem?

First I define the variables and the goals of using those variables to investigate relevant and irrelevant relationships inbetween columns of the data matrix and their relationships to the variables of the design matrix.

Next, I read relevant literature to bias my opinion of the methods and their utility in estimation, and value to modeling the problem at hand.

### Literature and knowledge mapping in documentation design

I use plain text and markup syntax to produce LaTeX documentation. I use different visualization software to assess datasets and pre-produce graphics relevant for exploratory or explanatory data analysis mostly in report form.

### Exploring relationships with your data

I use various methods in looking at models and model fit, in and out of sample statistics, normalization of data, and mostly boxplots of the interesting variables. I then look across the covariates for grouping and testing of individual groups.

### Do you contaminate your data?

/s. Always. I write software for comparing data I understand how to model. I am typically in discovery in the "green" team which does methods development, not sample testing, and I write code to mostly do exploratory analysis. Explanatory stuff like formal hypothesis testing has a place, but writing basic modeling tasks is pretty simple. You frame a question, state your assumptions, rationalize the methodology, and then assess the question to the best of the nexus of the method, the data, and your ability. 

Contaminating data in this sense I refer to, is whether or not you have looked at your data prior to your testing, if you are in the testing group. I mostly do exploratory graphics, and I have worked on some pipelines and report infrastructures that assess models made by others, or in-house and discovery related. 

### Red-team and green-team methods testing/development


In machine learning, established and specified methods, their requirements, and method goals are suggested to be used in a blind study format for assessing any given problem. By using exploratory views of the data, and thus "contaminating the data" we may introduce method or analyst bias. A data scientist may make a mistake during normalization of variables and appropriate variance descriptions of those variables. 

The tester does not have the luxury of exploring the relationships to make a concrete perspective on the "influencing" variables and instead looks at a single view of the relationships defined in the methodology at hand. The tester instead typically produces a report and some artifacts related to the methodologies assumptions and perspectives, and reports the results to the "customer" in some format. 

The methods development group in a research organization, typically the senior engineers (16+ years), validates methods and defines new valuable views of the data and its properties and typically makes recommendations to key stakeholders, including institutional review boards, requirements and policy decision-makers, management, and procurement or accounting. 

Some test groups also make such recommendations, but typically at more formal capcities about certain tests and studies vs than engineering and implementing the methods approved for usage on certain datasets vs the actual testing process itself. Not all teams follow the same organizational format depending on group goals, deliverables needed, and resourcing.

"Green team red team" formats in development or engineering groups allows for two different requirement sets of goals. In industry I've mostly been on "green"/development teams and I also produced internal infrastructure for integrational code and data views, which is typically green team, and I've made recommendations about variables and outlier patterns related to processing a specific dataset. In my experience, while both teams test, the red team is typically throughput related, where as green team's method development priorities, while also throughput related, are often related to addressing artifacts in particular datasets and how they determine a model's success, or absence of, in a given analysis. The "red" or testing/senior team makes formal recommendations to leadership about specific tests, the methods power and versatility in the test/study goal, and limitations of assumptions about interpretations on a particular dataset by virtue of the senior experience level typical of members of the "red" team.

In my own research however, I do both. I describe the method and vet it against method styles and trends. Another name for the green team would be the "development" team, and "red" or other teams perform some combination of testing and methods development.


