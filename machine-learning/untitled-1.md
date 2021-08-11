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

![](../.gitbook/assets/image%20%2825%29.png)

#### Log Loss

* Logarithmic loss \(also known as Log loss\) measures the performance of a classifier where the predicted output is a probability value between 0 and 1.

![](../.gitbook/assets/image%20%2821%29.png)

### Decision Trees

* Decision trees are built using recursive partitioning to classify the data.
* The algorithm chooses the most predictive feature to split the data on.
* What is important in making a decision tree, is to determine “which attribute is the best, or more predictive, to split data based on the feature.”
* A node in the tree is considered “**pure**” if, in 100% of the cases, the nodes fall into a specific category of the target field.
* ”Impurity” of nodes is calculated by “Entropy” of data in the node.

![](../.gitbook/assets/image%20%2824%29.png)

#### Entropy and Information gain

* Entropy is the amount of information disorder, or the amount of randomness in the data.
* The entropy in the node depends on how much random data is in that node and is calculated for each node.
* In decision trees, we're looking for trees that have the smallest entropy in their nodes.
* The entropy is used to calculate the homogeneity of the samples in that node.
* If the samples are completely homogeneous the entropy is zero and if the samples are equally divided, it has an entropy of one.

![P is for the proportion or ratio of a category](../.gitbook/assets/image%20%2823%29.png)

* The tree with the higher **information gain** after splitting is used for branching.
* **Information gain** is the information that can increase the level of certainty after splitting.

![](../.gitbook/assets/image%20%2826%29.png)

* It is the entropy of a tree before the split minus the weighted entropy after the split by an attribute.
* We can think of information gain and entropy as **opposites**.

### Logistic Regression

* Logistic regression is a statistical and machine learning technique for classifying records of a dataset, based on the values of the input fields.
* In logistic regression, dependent variables should be continuous; if categorical, they should be dummy or indicator-coded.
* The main objective of training in logistic regression, is to change the parameters of the model, so as to be the best estimation of the labels of the samples in the dataset.

#### Sigmoid function/logistic function:

* The sigmoid function, also called the logistic function, resembles the step function and is used by the following expression in the logistic regression.
* In logistic regression, we model the probability that an input \(X\) belongs to the default class \(Y=1\), and we can write this formally as, $$ P(Y=1|X)$$ .
*  $$P(y=0|X) = 1 - P(y=1|X)$$ 
* 
![](../.gitbook/assets/image%20%2832%29.png)

![](../.gitbook/assets/image%20%2835%29.png)

* The training process:

![](../.gitbook/assets/image%20%2830%29.png)

* Changing the value of $$\theta$$ to reduce the cost : gradient descent
*  Regularization is a technique used to solve the overfitting problem in machine learning models. **C** parameter indicates **inverse of regularization strength** which must be a positive float. Smaller values specify stronger regularization.

#### Logistic regression cost function

* $$\hat{y}$$ does not return a class as output, but it’s a value of \(0,1\), which should be assumed as a probability. 

#### Gradient Descent

* Gradient descent is an iterative approach to finding the minimum of a function.
* Gradient descent is a technique to use the derivative of a cost function to change the parameter values, to minimize the cost or error.
* The gradient is the slope of the surface at every point. And, the direction of the gradient is the direction of the greatest uphill.
* Gradient descent is like taking steps in the current direction of the slope, and the learning rate is like the length of the step you take.

![](../.gitbook/assets/image%20%2829%29.png)

* The derivative equation returns the slope of that point, and we should update the parameter in the opposite direction of the slope.
* A vector of all these slopes is the gradient vector, and we can use this vector to change or update all the parameters. 
* We take the previous values of the parameters and subtract the Error derivative. This results in the new parameters for θ that we know will decrease the cost. 
* Also, we multiply the gradient value by a constant value $$\eta$$ , which is called the learning rate. Learning rate gives us additional control on how fast we move on the surface.
* In sum, we can simply say, Gradient descent is like taking steps in the current direction of the slope, and the learning rate is like the length of the step you take.

![](../.gitbook/assets/image%20%2836%29.png)

### Support Vector Machine

* mapping data into a higher dimensional space is called **kernelling.**

![](../.gitbook/assets/image%20%2834%29.png)

