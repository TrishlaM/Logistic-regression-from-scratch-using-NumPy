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
              ![image](https://user-images.githubusercontent.com/54930611/76259706-3540b800-6224-11ea-8dc0-5a4fedf9f195.png)

#### 4. Optimization
Using this function definition, we optimize the cost function mentioned above and update the parameters to minimize the cost. The gradients descent algorithm is used and using the algorithm, the gradients of the 'w' and 'b' parameters are computed and the parameters are updated by using the following formula-
 #####      w := w - learning_rate * dw, and
 #####      b := b - learning_rate * db
 
 By running this function using loop for n no. of iterations, we reach a convergence point where the cost function doesn't decrease any further. 
 Another important thing to note is the choice of learning rate. Learning rate shouldn't be too small to increase the computational expense, or too large to overshoot the global minima. Thus, we try the model algorithm with various learning rates to find out the rate which gives optimizes the cost function the best.
 
 The final step is to create a 'predict' function and calculate the accuracy of predicted alues from test set.
