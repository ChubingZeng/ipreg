<!-- README.md is generated from README.Rmd. Please edit that file -->
classo: R package for LASSO with custom penalization based on external information
==================================================================================

Introduction
------------

The aim of *classo* is to extend standard LASSO to allow the regression coefficients to be differentially penalized based on external information which may be informative for the effects of predictors on the outcome of interest.

This package has two main functions for now.

-   Empirical Bayes (EB) tuning
    EB tuning is a novel way to find the tuning parameter for LASSO, as an alternative to cross-validation.

$$ min\_{\\beta}\\frac{1}{2} \\sum\_{i=1}^{i=p}(Y\_i - \\beta\_0 - \\sum\_{j=1}^{j=p}X\_{ij}\\beta\_j)^2 + \\lambda \\sum\_{j=1}^{j=p}|\\beta\_j| $$

-   Customized LASSO
    Customized LASSO extends standard LASSO to allow differential penalization on coefficients. You can choose to plug in external data which contains information about the predictors. For example, Gene Ontology annotations or previous study restults. Please note that the number of rows in the external data should match the number of columns in your design matrix.

$$ min\_{\\beta}\\frac{1}{2} \\sum\_{i=1}^{i=p}(Y\_i - \\beta\_0 - \\sum\_{j=1}^{j=p}X\_{ij}\\beta\_j)^2 + \\sum\_{j=1}^{j=p} \\lambda(Z\_j)|\\beta\_j| $$

Currently, we allow both continuous and binary outcomes. The binary outcome case is based on the extension of linear outcome case using linear discriminat analysis.

Installation
------------

You can install *classo* from github with:

``` r
# install.packages("devtools")

library(devtools)
devtools::install_github("ChubingZeng/classo")

library(classo)
```

Usage
-----

### Empirical Bayes Tuning

### LASSO with custom penalization

Example
-------

This is a basic example which shows you how to solve a common problem:

``` r
## basic example code
```
