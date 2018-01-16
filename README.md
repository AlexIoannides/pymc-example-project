# Template PyMC3 Project for Bayesian Data Analysis
The repository contains an example Bayesian data analysis, using data collected from a set of multi-lot on-line auction events executed in Europen markets, over the past year. It contains a Jupyter notebook in which we build interpretable models of the average Return-on-Reserve, using variables that describe various facets of multi-lot on-line auction events (e.g. the average number of bidders per-lot), using probabilitic programming methods (from the PyMC3 package), for (Bayesian) model inference.

As we have already mentioned, the ultimate aim of this endeavour is for this repo to serve as a template project-workflow for conducting an end-to-end Bayesian data analysis using PyMC3. It includes many helper functions for automating otherwise tedious tasks (e.g. interacting with Theano to score models on test data, or handling PyMC3 back-ends to avoid having to recompute MCMC sampling), as well as examples of how data pre-processing can be integrated with Scikit-Learn.

The overall approach to statistical (scientific) workflow has been heavily inspired by the book 'Statistical Rethinking - A Bayesian Course with Examples in R and Stan', by Richard McElreath http://xcelab.net/rm/statistical-rethinking/, which is the most significant book on statistics and modelling that I have read during a career spanning more than a decade.

## Project Dependencies
This project was assembled using an isolated virtual environment, created with `virtualenv`. The exact details (e.g. versions) of the packages used are contained in the requirements.txt file found the root directory. At a very high-level this is essentially:
- PyMC3
- numpy
- Pandas
- scikit-learn
- matplotlib

The steps below walk-through the process of installing these dependencies and making them available to the Jupyter template notebook via a dedicated Python 3 kernel.

### Creating a Virtual Environment
I am assuming that the reader will be using OS X, is familiar with using the terminal and that they have Python 3 and the Jupyter package installed and made generally available (i.e. they are on the PATH). From within the root directory, run the following commands to create a virtual environment (called `venv`) and activate it,

```bash
python3 -m venv venv
source venv/bin/activate
```

To deactivate the virtual environment at a later date (e.g. after you run the steps below), just use `deactivate` from the command line.

### Install Dependencies from requirements.txt
To install the dependencies for this project, run the following commands from the terminal next,

```bash
pip install -r requirements.txt
```

### Creating a Jupyter Kernel for the Virtual Environment
Now that we have an isolated virtual environment for this project we need to be able to access it via Jupyter kernel. This is achieved with the following terminal commands,

```bash
ipython kernel install --user --name=pymc3_proj
```

The `pymc3_proj` should now be available from within Jupyter to associate with the notebook in this repo! Should you need to remove the kernel at a later date, then the location of the `kernels` directory (which will contain a dedicated directory for the `pymc3_proj` kernel), can be found by running,

```bash
jupyter kernel --data-dir
```

Then, it's simply a matter of running `rm -rf kernels/pymc3_proj` from within the directory returned from the above command.
