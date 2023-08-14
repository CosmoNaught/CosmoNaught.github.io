---
title: 'Linear Regression'
date: 2023-08-14
permalink: /posts/2023/08/linear-regression/
tags:
  - Linear Regression
  - Regression Algorithms
  - Boston Housing dataset
---

Linear regression is one of the foundational pillars of machine learning and statistics. It's a technique that establishes a relationship between two continuous variables. Simply put, it tries to fit the best straight line that predicts the output value within a range.

Imagine wanting to predict the price of a house based on its size. Intuitively, as the size of the house increases, the price is also likely to increase. This is where linear regression comes into play.

Interestingly, when I first began my machine learning journey, I was astounded by the buzz around 'machine learning algorithms'. I anticipated cryptic and intricate algorithms that did magical predictions. But coming across linear regression, something so conceptually simple, and seeing it under the 'machine learning' umbrella was an enlightening moment. It reminded me that sometimes, simplicity can be as powerful and effective as complexity, especially when you're just getting started or need quick insights.

## Mathematical Formulation:

Linear regression aims to model the relationship between a dependent variable $$y$$ and one or more independent variables $$x$$. When there's just one independent variable, it's called simple linear regression.

The equation of the line is given by:

$$ y = \beta_0 + \beta_1x + \epsilon $$

Where:
- $$ y $$ is the dependent variable we're trying to predict.
- $$ x $$ is the independent variable we use for prediction.
- $$ \beta_0 $$ ​ is the y-intercept of the line.
- $$ \beta_1 $$ represents the slope, indicating the change in $$y$$ for a one-unit change in $$x$$.
- $$ \epsilon $$ is the error term, capturing the difference between our prediction and the actual value.

## Dataset Description

For this demonstration, we'll utilize the **Boston Housing dataset**, a well-known dataset in the machine learning community. This dataset contains information about different houses in Boston, gathered in the 1970s. It consists of 506 entries with 14 attributes each. However, for simplicity, we'll be focusing on one attribute as our independent variable - the average number of rooms per dwelling. Our target variable will be the median value of owner-occupied homes in $1000s.

## What does our Python code aim to accomplish?

How can we predict the median value of houses in Boston based on the number of rooms using Linear Regression? The subsequent Python code provides an insight into this by:

1. Loading the Boston Housing dataset.
2. Splitting the data into training and testing sets.
3. Training a Linear Regression model using the training data.
4. Visualizing the fitted regression line against the test data.
5. Evaluating the model's performance using Mean Squared Error.

## Python Implementation:

To demonstrate the use of linear regression, we'll use the `Boston Housing dataset` available in the `sklearn.datasets package`.

```python
# Required Libraries
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.datasets import load_boston
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Load dataset
boston = load_boston()
X = boston.data[:, 5:6]  # Average number of rooms per dwelling
y = boston.target  # Median value of owner-occupied homes in $1000s

# Splitting data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Model training
model = LinearRegression()
model.fit(X_train, y_train)

# Predictions
y_pred = model.predict(X_test)

# Plotting
plt.scatter(X_test, y_test, color='blue')
plt.plot(X_test, y_pred, color='red')
plt.xlabel('Average number of rooms per dwelling')
plt.ylabel('Median value of homes in $1000s')
plt.title('Linear Regression on Boston Housing Dataset')
plt.show()

# Error metric
print(f"Mean Squared Error: {mean_squared_error(y_test, y_pred)}")

```
# Conclusion 

Linear regression, with its directness and interpretability, is an excellent starting point in the machine learning journey. Its strengths lie in its ability to provide initial insights, quick predictions, and a foundational understanding of relationships between variables. However, it's also essential to recognize its limitations. For instance, it assumes a linear relationship between variables and might not capture more complex interactions. As one delves deeper into the realm of machine learning, comparing the performance and insights of linear regression to more advanced models becomes a valuable exercise. It underscores the balance of complexity versus interpretability, and the importance of choosing the right tool for the job.