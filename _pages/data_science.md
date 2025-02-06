---
permalink: /data_science
title: "Statistics and Data Science"
author_profile: true
hero_image: "images/dna2.gif"
---

# Data science experience

I am a data professional that focuses on the analysis of genomic sequences. I turn DNA sequences into count vectors of DNA subsequences for use in alignment, k-mer compositional analysis, overrepresented motif analysis, De Bruijn graph formation, or total count vector based differentials on sequences or assemblies.

In addition, I turn alignment abundances into digital readouts of gene expression for use in downstream analysis such as differential gene expression comparisons, whole transcriptome interpretations of gene representation and functional ontologies such as metabolic enzyme representation, transcription factor and cell signaling and pathway representation, orthologous (gene families) and paralogous (related functionality) gene families and of course genome completeness. 

So in addition to functional metrics such as the ontologies and their statistics, the alignment abundances, referred to as read counts, provide abundance approximations that are integral to variance estimation among replicates of a given condition and its use in a variance modeling and hypothesis testing framework like DESeq2. 

Depending on the goal of your project, you design your variable selections either as a linear combination of other variables, or directly into your testing design and implying the method used for modeling. When describing the data one takes an exploratory flavor when initially contaminating your dataset with inspection. You might try a correlation matrix plot to start with to initially discover trends that may be causal or incausal between your dependent and independent variables and then constructing your feature selection to use 


# How do you approach a data science problem?

First I define the variables and the goals of using those variables to investigate relevant and irrelevant relationships inbetween columns of the data matrix and their relationships to the variables of the design matrix.

Next, I read relevant literature to bias my opinion of the methods and their utility in estimation, and value to modeling the problem at hand.

## Literature and knowledge mapping in documentation design

I use plain text and markup syntax to produce LaTeX documentation. I use different visualization software to assess datasets and pre-produce graphics relevant for exploratory or explanatory data analysis mostly in report form.

## Exploring relationships with your data

I use various methods in looking at models and model fit, in and out of sample statistics, normalization of data, and mostly boxplots of the interesting variables. I then look across the covariates for grouping and testing of individual groups.

## Do you contaminate your data?

Always. I write software for comparing data I understand how to model. I am typically in discovery in the "green" team which does methods development, not sample testing, and I write code to mostly do exploratory analysis. Explanatory stuff like formal hypothesis testing has a place, but writing basic modeling tasks is pretty simple. You frame a question, state your assumptions, rationalize the methodology, and then assess the question to the best of the nexus of the method, the data, and your ability. 

Contaminating data in this sense I refer to, is whether or not you have looked at your data prior to your testing, if you are in the testing group. I mostly do exploratory graphics, and I have worked on some pipelines and report infrastructures that assess models made by others, or in-house and discovery related. 

## Red team green team


In machine learning, established and specified methods, their requirements, and method goals are suggested to be used in a blind study format for assessing any given problem. By using exploratory views of the data, and thus "contaminating the data" we may introduce method or analyst bias. A data scientist may make a mistake during normalization of variables and appropriate variance descriptions of those variables. 

The tester does not have the luxury of exploring the relationships to make a concrete perspective on the "influencing" variables and instead looks at a single view of the relationships defined in the methodology at hand. The tester instead typically produces a report and some artifacts related to the methodologies assumptions and perspectives, and reports the results to the "customer" in some format. 

The methods development group in a research organization, typically the senior engineers (16+ years), validates methods and defines new valuable views of the data and its properties and typically makes recommendations to key stakeholders, including institutional review boards, requirements and policy decision-makers, management, and procurement or accounting. 

Some test groups also make such recommendations, but typically at more formal capcities about certain tests and studies vs than engineering and implementing the methods approved for usage on certain datasets vs the actual testing process itself. Not all teams follow the same organizational format depending on group goals, deliverables needed, and resourcing.

"Green team red team" formats in development or engineering groups allows for two different requirement sets of goals. In industry I've mostly been on "green"/development teams and I also produced internal infrastructure for integrational code and data views, which is typically green team, and I've made recommendations about variables and outlier patterns related to processing a specific dataset. In my experience, while both teams test, the red team is typically throughput related, where as green team's method development priorities, while also throughput related, are often related to addressing artifacts in particular datasets and how they determine a model's success, or absence of, in a given analysis. The "red" or testing/senior team makes formal recommendations to leadership about specific tests, the methods power and versatility in the test/study goal, and limitations of assumptions about interpretations on a particular dataset by virtue of the senior experience level typical of members of the "red" team.

In my own research however, I do both. I describe the method and vet it against method styles and trends. Another name for the green team would be the "development" team, and "red" or other teams perform some combination of testing and methods development.


# What is data science


Data science is an interdisciplinary field that combines statistical analysis, probability theory, and machine learning to extract insights from structured and unstructured data. Python is the dominant programming language in this domain, offering powerful libraries such as NumPy for numerical computations, pandas for data manipulation, and scikit-learn for machine learning. R is another widely used language, particularly valued for its statistical modeling and visualization capabilities, with packages like ggplot2, dplyr, and caret. These tools enable data scientists to preprocess data, perform exploratory data analysis (EDA), and apply statistical techniques to uncover patterns and relationships within datasets. Modeling is the name of the game in good research practices and producing clear and reproducible protocols for assessing and modeling associations between experimental variables.

<!--
Probability and statistics form the foundation of data science, underpinning key methods for data interpretation and decision-making. Probability distributions, hypothesis testing, and Bayesian inference are essential techniques implemented using NumPy in Python and base R or the stats package. For performance optimization, Cython can be used to accelerate computationally intensive statistical operations by compiling Python code to C-like speed. Machine learning builds on these principles, leveraging algorithms such as regression, decision trees, support vector machines, and neural networks to make predictive models. With NumPy for matrix operations, Cython for performance enhancements, and R for statistical rigor, data scientists can efficiently analyze large datasets, optimize models, and drive insights in fields ranging from finance and healthcare to artificial intelligence and scientific research.
-->

# How does data science affect me?

If you work in industry as a technologist, or adjacent to technology concerning the collection and analysis of data in the knowledge economy, then you are likely effected in some way by data science. Machine learning and statistics are at the core of modern cancer treatments, weather modeling, geospatial data concerning agriculture, research and development of technologies, products, and pharmaceuticals. The list goes on. You are likely impacted by the data science at the core of the development of artificial intelligence and its impact on the American worker. 

Whether or not you work with data in some capacity, modern data science methods such as deep learning, pattern recognition, and support vector machines have large reaching impacts on our everyday life.


# What does data science look like in practice?

Data science is an interdisciplinary field leveraging programming, data structures and algorithms, statistics, and machine learning to produce insights or models concerning the response of dependent variables to independent variables. Feature engineering is the art of "manipulating" data to produce novel or effective covariates: response variables that are measurable and/or derivable from existing datasets. 

By leveraging programming and algorithms, in practice, most problems concerning instrumental read outs are addressable with statistics and data science to produce models that are informative (addressing variation) or predictive in nature. Typical introductory concepts include normalization, type I/II error, positive predictive value, false discovery rates, and regularization. 

By leveraging Linux computational infrastructure using shell scripts as glue code, Docker containers for reproducible builds, and Python/R/Rust programming for data manipulations, algorithms, and modeling, many problems in the knowledge economy are addressable with never before seen parallelization.

# How does data science relate to software engineering




