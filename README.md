# PyThinking

This repository is my attempt at doing statistical rethinking in python. It will only make sense to read this if you (1) have the following book and (2) want to do it all in Python.

Book:   Statistical Rethinking
Author: Richard McElreath
Edt.:   2nd

The sub folder `code_boxes` contains Jupyter notebooks for each chapter of the book with the same numbering, but translations to python. 

If differences, packages, etc. are required, a *Note* is attached at the end in italic explaining the code changes. This repository also explains some ideas on how to implement stuff in python.

I try to stick as close to the original variable names, etc., as possible. A compilation of the original `R code` boxes can be found here: [https://github.com/rmcelreath/rethinking/blob/master/book_code_boxes.txt](https://github.com/rmcelreath/rethinking/blob/master/book_code_boxes.txt)

There is going to be a folder with excercises, were the exercises are solved in the pythonic way. References to where I compared solutions with are given on top of each exercise sheet.

Just for fun: Here I use `Py code #` instead of `R code #`, where `#` represents the number of the code box.

*Note*: Without the book, you won't learn anything, so no reason to keep on reading. I won't repeat the questions in the exercises, I won't give details on the PyCode boxes when things should be obvious. 

## General notes

This code translation assumes that you have some basic python knowledge. Otherwise, why go through the pain, use R.

R and Python have different bases, e.g., while command `log(2)` is a default command in R, python requires a math package to load this. There are several other of these packages that we need.

## Pre-requisites
Several standard python packages are used here. In order to install all the packages in your python environment, you can run the following command:

    pip install numpy, sklearn, matplotlib, scipy, pandas, seaborn

Imports will take place at the top of every Jupyter notebook and won't be repeated for clarity, however, I will try and use the default imports.

### matplotlib
Matplotlib will be used for plotting purposes. we will generally import matplotlib as

    from matplotlib.pyplot import plt

So you will be easily able to find the plotting commands by looking for `plt.` in a given code example

### numpy
Numpy will be used as a math package. In the translated code, we will always import numpy into the namespace np and will not further comment on this section. You will thus, when numpy is needed, read the first line as following:

    import numpy as np
    
In general, for all arrays for mathematical operations, `np.arrays` will be used rather than python's built in lists. 

### pandas
Pandas by now is the default package in python for handling and analyzing data. While often not required per se, it makes data and its analysis a lot easier. Pandas especially bring R-like data frames and other classes to python that are not natively available. For using pandas we will always import it in its default way:

    import pandas as pd

### seaborn
Directly from their [website](https://seaborn.pydata.org/): "Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics."

### scipy
Scientific python package, will be used for it's feature rich stats package where appropriate. Required since Python does not have by default all stats functions loaded as R does.

### scikit-learn
While R comes preloaded with many data analysis packages, python does not. We thus need to install a package to handle things like linear models, which are by default available in R. Let's try out the [scikit-learn](https://scikit-learn.org) package and see where it leads us. Importing this package will be explicity stated in the code.

## A personal note
McElreath's book pretty much describes me perfectly in the "Audience" section: just read the first paragraph. I got this book out of this curiosity, after it was recommended to me by a friend. Turns out: the second edition just came out.  Furthermore, the author mentioned code translations in the preface and that he hopes there will be some for the second edition as well. Since I have been programming in python for around 15 years now and have always feared away from R (there just never was a reason to look into it), I decided to go through the book, understand and follow the R code, but also translate this code into python, where I'm more comfortable. I decided to also document this process here. Maybe this can help somebody else at some point too. If not, at least it will be a reminder for myself on how to set up my python environment on a new system later on again if I want to do problems from the book.
