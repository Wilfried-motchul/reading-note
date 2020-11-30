# Linear Regressions

We know that linear regression is a popular technique and you might as well seen the mathematical equation of linear regression. But do you know how to implement a linear regression in Python?? If so don’t read this post because this post is all about implementing linear regression in Python. There are several ways in which you can do that, you can do linear regression using numpy, scipy, stats model and sckit learn. But in this post I am going to use scikit learn to perform linear regression.

## Exploring Boston Housing Data Set

The first step is to import the required Python libraries into Ipython Notebook.

```
% matplotlib inline
import numpy as np
import pandas as pd
import scipy.stats as stats
import matplolib.pyplot as plt
import sklearn
```

This data set is available in sklearn Python module, so I will access it using scikitlearn. I am going to import Boston data set into Ipython notebook and store it in a variable called boston.

```
from sklearn.dataset import loard_boston
boston = loard_boston()
```

## Scikit Learn

In this section I am going to fit a linear regression model and predict the Boston housing prices. I will use the least squares method as the way to estimate the coefficients.

Y = boston housing price(also called “target” data in Python)

and

X = all the other features (or independent variables)

First, I am going to import linear regression from sci-kit learn module. Then I am going to drop the price column as I want only the parameters as my X values. I am going to store linear regression object in a variable called lm.

```
from sklearn.linear_model import LinearRegression
X = bos.drop('PRICE', axis = 1)

# this creates a LinearRegression object
lm = LinearRegression()
lm
```
## Fitting a Linear Model

we are going to use all 13 parameters to fit a linear regression model. Two other parameters that you can pass to linear regression object are fit_intercept and normalize.

In [20]: lm.fit(X, bos.PRICE)

Out[20]: LinearRegression(copy_X=True, fit_intercept=True, normalize=False)

I am going to print the intercept and number of coefficients.