# Supervised Learning

* Teaching the model with labelled data.

## Types of supervised learning

1. Classification:

![](../.gitbook/assets/image%20%2818%29.png)

    2. Regression:

![](../.gitbook/assets/image%20%2810%29.png)

## Regression

A regression model relates y, or the dependent variable, to a function of x, i.e., the independent variables.

Two types of variables:

* Dependent variables\(y\)
  * The dependent variable can be seen as the "state", "target" or "final goal" we study and try to predict.
  * Should be a continuous value and cannot be a discrete value.
* Independent variables\(x\)

  * independent variables, also known as explanatory variables, can be seen as the "causes" of those "states".
  * Can be measured on a categorical or continuous data

#### Two types of regression models:

![](../.gitbook/assets/image%20%2817%29.png)

![](../.gitbook/assets/image%20%2813%29.png)

### Linear regression

#### Simple Linear Regression:

![](../.gitbook/assets/image%20%2816%29.png)



![](../.gitbook/assets/image%20%2819%29.png)

The objective of linear regression is to minimize this MSE equation, and to minimize it, we should find the best parameters, θ0 and θ1.

![](../.gitbook/assets/image%20%2811%29.png)

#### Multiple linear regression:

* Extension of simple linear regression
* Dependent variable y is a linear combination of independent variables x

![](../.gitbook/assets/image%20%2820%29.png)

* $$\theta^Tx$$in a one dimensional space, is the equation of a line. It is what we use in simple linear regression. 
* In higher dimensions, when we have more than one input \(or x\), the line is called a plane or a hyper-plane and this is what we use for multiple linear regression.

### Non linear regression

* Multiple linear regression:
  * Relationship between the independent variable x and the dependent variable y is modelled as an nth degree polynomial in x.
* Non linear regression:
  *  $$\hat{y}$$ must be a non-linear function of the parameters $$\theta $$ not necessarily the features x
  * model is nonlinear by parameters

## Classification

### K-Nearest Neighbors

* The k-nearest-neighbors algorithm is a classification algorithm that takes a bunch of labelled points and uses them to learn how to label other points.
* This algorithm classifies cases based on their similarity to other cases.
* K-nearest neighbors is based on this paradigm: “Similar cases with the same class labels are near each other.”

#### K-Nearest Neighbors Algorithm

1.  Pick a value for K.
2. Calculate the distance of unknown case from all cases.
3. Select the K observations in the training data that are ‘nearest’ to the unknown data point.
4. Predict the response of the unknown data point using the most popular response value from the K nearest neighbors.

### Evaluation Metrics

* Explains the performance of a model.

#### Jaccard index

![](../.gitbook/assets/image%20%2822%29.png)

#### F1 Score

* Precision is a measure of the accuracy, provided that a class label has been predicted.
* Recall is the true positive rate.

![](../.gitbook/assets/image%20%2823%29.png)

#### Log Loss

* Logarithmic loss \(also known as Log loss\) measures the performance of a classifier where the predicted output is a probability value between 0 and 1.

![](../.gitbook/assets/image%20%2821%29.png)

### Decision Trees







