<!-- README.md is generated from README.Rmd. Please edit that file -->
OpenCaseStudies
===============

<!-- badges: start -->
[![Travis build
status](https://travis-ci.org/opencasestudies/Bloomberg-ocs-rural-and-urban-obesity.svg?branch=master)](https://travis-ci.org/opencasestudies/Bloomberg-ocs-rural-and-urban-obesity)
<!-- badges: end -->

### Disclaimer

The purpose of the [Open Case
Studies](https://opencasestudies.github.io) project is **to demonstrate
the use of various data science methods, tools, and software in the
context of messy, real-world data**. A given case study does not cover
all aspects of the research process, is not claiming to be the most
approrpriate way to analyze a given dataset, and should not be used in
the context of making policy decisions without external consultation
from scientific experts.

### License

This case study is part of the
[OpenCaseStudies](https://opencasestudies.github.io) project. This work
is licensed under the Creative Commons Attribution-NonCommercial 3.0
([CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/us/))
United States License.

### Citation

To cite this case study:

### Title

Exploring Global Patterns of Obesity from 1985 to 2017

Body Mass Index (BMI) is often used a proxy for adiposity with
classifications based on BMI to define “underweight”, “normal”,
“overweight” and “obese”, where higher BMI has been associated with
increased mortality, rates of type 2 diabetes, cancer, heart disease,
and stroke. A recent
[paper](https://www.nature.com/articles/s41586-019-1171-x.pdf) showed
that contrary to a widely reported view (that urbanization is one of the
most important drivers in the global rise of obesity), in fact BMI is
increasing at the same rate or faster in rural areas (compared to
cities), in particular in low- and middle-income regions. Also, there a
gender-discrepancy (women have a higher BMI in rural communities). Here,
we explore this data to understand global patters in obesity. This
analysis is important because it demonstrates the need to provide better
access (financial and physical access) to healthy foods in rural
communities, especially in low-income countries to address the obesity
crisis.

### Motivating questions

1.  Is there a difference between rural and urban BMI estimates around
    the world? In particular, how does this look for females?
2.  How have BMI estimates changed from 1985 to 2017? Again, In
    particular, how does this look for females?
3.  How do different countries compare for BMI estimates? In particular,
    how does the United States compare to the rest of the world?

### Data

The data used in this analysis comes from a [supplementary
table](https://static-content.springer.com/esm/art%3A10.1038%2Fs41586-019-1171-x/MediaObjects/41586_2019_1171_MOESM1_ESM.pdf)
for the following article:

[NCD Risk Factor Collaboration (NCD-RisC). Rising rural body-mass index
is the main driver of the global obesity epidemic in adults. *Nature*
**569**, 260–264
(2019).](https://www.nature.com/articles/s41586-019-1171-x)

This article can be found freely available online.

### Analysis

In this case study, we will largly focus on methods for comparing two
groups using hypothesis testing and parametric and nonparametric tests.
We also cover multiple testing correction and fairly advanced data
visualization methods using ggplot2.

#### Data Import

Data is imported from a PDF using `pdftools` to obtain data from the
following table:

![](img/first_page.png)

#### Data wrangling

This case study covers many wrangling techniques and largely involves
using the package `stringr`.

1.  Dividing data into separate lines
2.  Removing excess white-space
3.  Removing redundant header information
4.  Correcting spacing issues
5.  Dealing with NA values that are labeled in an unusal manner
6.  Splitting the data into columns using a delimiter
7.  Changing variable names
8.  Sorting the data
9.  Converting to long format
10. Separating a column into multiple columns

#### Data exploration (exploratory analysis)

To explore the data we use the `summarize()` function and plot the data
to look at the distribution of the data. Quantile-Quantile plots are
used to evaluate the distribution and compare it to theoretical normal
distribution.

#### Summary

This case study covers fundamental concepts in statistics such as type 1
error, alpha threshold, p-values, hypothesis testing, parametric two
sample mean tests, and nonparametric two sample tests, as well as the
assumptions of the various included statistical tests and what to do
when data is paired.

### Other notes and resources

**For users**: There is a `Makefile` in this folder that allows you to
type `make` to knit the case study contained in the `index.Rmd` to
`index.html` and it will also knit the `README.Rmd` to a markdown file
(`README.md`).

**For instructors**: This case study includes suggested homework.
