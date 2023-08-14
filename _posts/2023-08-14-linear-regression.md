---
title: 'Linear Regression'
date: 2023-08-14
permalink: /posts/2023/08/linear-regression/
tags:
  - Linear Regression
  - Regression Algorithms
---

Linear regression is a foundational algorithm in the machine learning world. It's used to predict a continuous target variable based on one or more input features. The algorithm tries to find the best fit straight line that accurately predict the output values within a range.

## Mathematical Formulation:

Linear regression seeks to model the relationship between a dependent variable and one or more independent variables by fitting a linear equation to observed data. For a simple linear regression (one independent variable), the formula is:

Linear regression seeks to model the relationship between a dependent variable and one or more independent variables by fitting a linear equation to observed data. For a simple linear regression (one independent variable), the formula is:

$$ y = \beta_0 + \beta_1x $$

Where:
- $$ y $$ is the dependent variable.
- $$ x $$ is the independent variable.
- $$ \beta_0 $$ is the y-intercept.
- $$ \beta_1 $$ is the slope of the line.

## Python Implementation:

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.datasets import make_regression

# Generate sample data
X, y = make_regression(n_samples=100, n_features=1, noise=0.4, bias=50)

# Create a linear regression model
model = LinearRegression()

# Train the model
model.fit(X, y)

# Predict using the model
y_pred = model.predict(X)

# Plotting
plt.scatter(X, y, color='blue', label='True data')
plt.plot(X, y_pred, color='red', label='Linear fit')
plt.title('Linear Regression')
plt.xlabel('X')
plt.ylabel('y')
plt.legend()
plt.show()

```
# Conclusion 

Linear regression is a straightforward yet powerful algorithm for predicting continuous values. While it assumes a linear relationship between inputs and outputs, it can serve as a benchmark for more complex algorithms or be used directly when the relationship is indeed linear.