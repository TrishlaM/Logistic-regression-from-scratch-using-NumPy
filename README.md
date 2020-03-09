# Logistic-regression-from-scratch-using-NumPy
In this repository, the PIMA Indians diabetes dataset has been used to illustrate how to create a logistic regression model from scratch using vectorization of the predictor variables and gradient descent algorithm for cost minimization with the intuition of neural network.
The steps used to create the model are listed below -

#### 1. Defining the activation function
The model algorithm consists of linear transformation of predictor variables to predict the output, which will give a numeric value. Thus, to restrict those values in the range of 0 and 1, an activation function is used here.
We have used the sigmoid activation function here which is given by-

####  sigmoid(Z)=1/(1+e^(-Z))

#### 2. Random initialization of parameters (bias term and coefficients)
The parameters 'w' and 'b' have been initialized as 0 to start with. With each iteration of the logistic regression algorithm, the    values are updated using the optimization function.The 'w' vector has the shape (no. of features in predictor, 1).

#### 3. Forward propagation
In this step, we do the activation conversion and compute the cost of the model which is given by

