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













