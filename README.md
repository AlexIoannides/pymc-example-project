# Template PyMC3 Project for Bayesian Data Analysis
The repository contains an example Bayesian data analysis, using data collected from a set of multi-lot on-line auction events executed in Europen markets, over the past year. It contains a Jupyter notebook in which we build interpretable models of the average Return-on-Reserve, using variables that describe various facets of multi-lot on-line auction events (e.g. the average number of bidders per-lot), using probabilitic programming methods (from the PyMC3 package), for (Bayesian) model inference.

As we have already mentioned, the ultimate aim of this endeavour is for this repo to serve as a template project-workflow for conducting an end-to-end Bayesian data analysis using PyMC3. It includes many helper functions for automating otherwise tedious tasks (e.g. interacting with Theano to score models on test data, or handling PyMC3 back-ends to avoid having to recompute MCMC sampling), as well as examples of how data pre-processing can be integrated with Scikit-Learn. 

The overall approach to statistical (scientific) workflow has been heavily inspired by the book 'Statistical Rethinking - A Bayesian Course with Examples in R and Stan', by Richard McElreath http://xcelab.net/rm/statistical-rethinking/, which is the most significant book on statistics and modelling that I have read during a career spanning more than a decade.

## Dependencies
This project was assembled using an isolated virtual environment, created with `virtualenv`. The exact details (e.g. versions) of the packages used are contained in the requirements.txt file in the root directory. At a very high-level this is essentially:
- PyMC3
- numpy
- Pandas
- scikit-learn
- matplotlib