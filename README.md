# Deep Neural Network Regression Estimating Bicycle Rental

TensorFlow deep regression model predicting bicycle rental.

---

## Problem Overview

A [dataset] has the number of bicycles rented during a day in a community, and other data related to the amount of bicycle renting, such as the weather situation on that day. The dataset has 731 instances and 15 variables. There are 7 categorical and 5 numerical variables among the explanatory variables. The remaining 3 variables can be considered explained, or dependent, variables. We aim to create a model to estimate the number of rented bicycles in a day.

[Linear regression] can estimate values for a variable given other correlated variables. It does that by fitting a mathematical function with coefficients associated with each variable composing the function. When multiple explanatory variables are used to predict an explained variable, a multiple linear regression is performed. When multiple variables are present, more complex regression models may generate better results. However, it is important to control the complexity of a regressor model so that it remains efficient and interpretable. Fortunately, we can control the complexity of a regressor model when we are dealing with regressors built using [neural networks].



## Analysis Introduction

[Deep neural networks] are capable of learning both linear and non-linear relationships between variables. Like this, it becomes possible to understand deeper connections between the independent and dependent variables. On the other hand, it has been known that [deep neural networks with 3 hidden layers are enough to model pratically all patterns in the data]. This provides an upper bound on the complexity of a neural network regressor, as its complexity is determined by the number of layers and neurons in it.

Using a neural network regressor with 3 hidden layers, we have set up a model that predicts bicycle rental with a close linear relationship with the actual numbers:

![deep_regression_bicycle_sharing_actual_vs_predicted](https://user-images.githubusercontent.com/33037020/211704479-5336ea14-6fce-4fdb-b1eb-1573a9f370dd.PNG)

With an [R2 score] of 0.89, we argue that this neural network model is able to work pretty well with the bicycle rental dataset. A [mean absolute error] (MAE) of about 5% of the dependent variable's range confirms this notion. Additionally, the MAE only deviates from the mean by roughly 10% of the average number of bicycles rented.

[//]: #
[dataset]: <https://www.kaggle.com/competitions/bike-sharing-demand/data>
[neural networks]: <https://www.ibm.com/topics/neural-networks>
[Deep neural networks]: <https://www.ibm.com/topics/deep-learning>
[Linear regression]: <https://en.wikipedia.org/wiki/Linear_regression>
[deep neural networks with 3 hidden layers are enough to model pratically all patterns in the data]: <https://www.sciencedirect.com/science/article/abs/pii/S0893608021001465>
[R2 score]: <https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html>
[mean absolute error]: <https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html>
