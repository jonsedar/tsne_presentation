# t-SNE Presentation

_Personal Project for t-SNE Demonstration_

Demo of high dimensional data visualisation with t-distributed Stochastic Neighbor Embedding (t-SNE) using the [Urban Land Cover Classification](https://archive.ics.uci.edu/ml/datasets/Urban+Land+Cover) dataset from the UCI Machine Learning Repository.

Barebones repo for hosting the Jupyter Notebook and presentation of my t-SNE presentation delivered at Python Quants and PyData London meetups Jan 2016

This is also a small example of using RISE to present a Jupyter Notebook RISE is quite new, available at https://github.com/damianavila/RISE


---


# Simplest usage: view the content in Github

1. Open the Github page for the `tsne_presentation.ipynb` file
2. Github magically renders the file to static HTML for reading


---


# Slightly more advanced usage: download and run the reveal.js presentation

## Git clone the repo to your workspace.

e.g. in Mac OSX terminal:

        $> git clone https://github.com/jonsedar/tsne_presentation.git
        $> cd tsne_presentation


## Using a basic webserver, locally host the `tsne_presentation.html` file

e.g. in Mac OSX terminal, use Python's inbuilt webserver

        $> python -m http.server      (if using Python 3)
        or
        $> python -m SimpleHTTPServer  (if using Python 2)

Then open `localhost:8000/tsne_presentation.html` in your webbrowser


---


# Execute the Notebook for yourself and use RISE to present

## Setup a virtual environment for Python libraries

**NOTE:** using Python 3.4

Using Anaconda distro, create a new virtual env, installing packages from
env YAML file:

        $> conda env create --file conda_env_tsne_presentation.yml
        $> source activate tsne_presentation



## Install RISE:

1. Clone the RISE repo https://github.com/damianavila/RISE
2. Source activate your python environment (if not already done)
3. Run `python setup.py install` from within the cloned RISE directory, this will install the nbextension


## Edit or rerun the Notebook

1. Run `$> ipython notebook` as normal, open `tsne_presentation.ipynb` and
make edits, re-run etc as you wish

## View the RISE presentation
1. Click the newly added button within the Notebook menu "Enter/Exit Live Reveal Slideshow"


## Compile a static presentation using plain old reveal.js

1. At the terminal, use nbconvert:

        $> ipython nbconvert tsne_presentation.ipynb --to slides

This creates `tsne_presentation.html` which you can serve as before using e.g.

        $> python -m http.server


---
