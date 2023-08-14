---
title: 'Logistic Regression'
date: 2023-08-15
permalink: /posts/2023/08/logistic-regression/
tags:
  - Logistic Regression
  - Regression Algorithms
  - Breast Cancer dataset
---

Logistic regression, despite having "regression" in its name, is primarily used for binary classification tasks - where the outcome is one of two categories. Think of it as answering "yes" or "no" to a question. For instance, given a set of features from a breast mass, is it benign or malignant?

One of the first applications I witnessed of logistic regression was on a medical dataset similar to the Breast Cancer dataset. The goal was to predict the likelihood of a tumor being malignant based on its characteristics. The simplicity and effectiveness of logistic regression made it an ideal choice for such a vital prediction.

## Mathematical Formulation:

Logistic regression aims to model the probability that a given input belongs to one of the two categories. It uses the logistic function (or sigmoid function) to squeeze the output between 0 and 1:

$$ p(X) = \frac{\epsilon^{\beta_{0}+\beta_{1}X}}{1+\epsilon^{\beta_{0}+\beta_{1}X}} $$

Where:

- $$ p(X) $$ is the probability that the dependent event occurs, given the value of the independent variable $$ X $$.
- $$ \beta_{0} $$ and $$ \beta_{1}$$  are coefficients
- $$ \epsilon $$ is the base of the natural logarithm (approximately equal to 2.71828).

## Dataset Description

We'll use the **Breast Cancer dataset**. This dataset comprises features computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. It contains 569 samples and 30 feature variables, with the target being either malignant (1) or benign (0).

What does our Python code aim to accomplish?

Given the features of a breast mass, such as its texture, radius, smoothness, and compactness, can we predict if the tumor is benign or malignant using Logistic Regression? Our Python demonstration will:

1. Load the Breast Cancer dataset.
2. Split the data into training and testing sets.
3. Train a Logistic Regression model.
4. Evaluate the model's performance using accuracy.

# Python Implementation:

To demonstrate the use of logistic regression, we'll use the `Breast Cancer dataset` available in the `sklearn.datasets` module.

```python
# Required Libraries
from sklearn.datasets import load_breast_cancer
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# Load dataset
data = load_breast_cancer()
X = data.data
y = data.target

# Splitting data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Model training
model = LogisticRegression(max_iter=5000)
model.fit(X_train, y_train)

# Predictions
y_pred = model.predict(X_test)

# Accuracy
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy*100:.2f}%")
```

## Results & Discussion

After loading the Breast Cancer dataset and splitting it into training and test sets, we trained a logistic regression model using the training data. When we used this model to predict whether the tumors in the test set were benign or malignant, we achieved an accuracy of approximately $$ accuracy \times 100 \% $$. This suggests that logistic regression provides a reliable means to classify tumors based on their features. However, it's essential to look at other metrics like precision, recall, and F1-score for a more comprehensive evaluation, especially for medical datasets where false negatives or false positives could have significant implications.

## Conclusion

Logistic regression offers a direct and interpretable method for tackling binary classification problems. With its probabilistic outcome, it doesn't just give a black-and-white answer but provides a measure of certainty. This can be especially useful in applications where understanding the likelihood of an event, and not just the event's prediction, is vital. However, its linear decision boundary means it might not always capture the intricate patterns in more complex datasets. In these cases, combining it with other techniques or moving to a different algorithm might yield better results. As a starting point, especially for simpler datasets or for a quick initial analysis, it's a solid go-to choice.

# Further Reading
TBD
