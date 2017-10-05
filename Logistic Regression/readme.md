# Logistic regression

Logistic regression is a method for classifying data into discrete outcomes.

## Unregularized Logistic Regression

Implementation of logistic regression to predict whether a student gets admitted into a university using two parameters, score at test 1 and score at test 2.

The cost function in logistic regression is

![jcostfunctlogisticreg](https://user-images.githubusercontent.com/29837880/31242090-f3423e48-a9d3-11e7-8eb8-7e4b88a0cf6b.PNG)

where the logistic regression hypothesis h(x) is given by

![logisticreg](https://user-images.githubusercontent.com/29837880/31242086-f33b0862-a9d3-11e7-9ca3-5bf2f4303c4e.PNG)

with g(z) the sigmoid function below

![sigmoid](https://user-images.githubusercontent.com/29837880/31242088-f33bf8ee-a9d3-11e7-8f2d-9004d727a95e.PNG)

Unlike for the Linear Regression, instead of using the gradient descent algorythm we are going to use a Matlab built-in optimization solver named "fminunc" to find the best parameters thetas.

After learning the best parameters thetas, we plot the data logistic regression line.

![linearlogisticreg](https://user-images.githubusercontent.com/29837880/31242093-f344657e-a9d3-11e7-8462-ef567d836f6b.png)

The accuracy of the model is 89%.


## Regularized Logistic Regression

Implementation of regularized logistic regression to predict if microchips from a manufactory pass quality tests. 

A first plot of the data alone (not included here for conciseness) showed that a linear logistic line would only do so poorly at separating defective chips from those properly functionning. Therefore we need to create new features (more than 2) in order to better fit the data.

To do so we map the two features into all polynomials of degree six and thus obtain a total of 28 features.

![mapfeature](https://user-images.githubusercontent.com/29837880/31242085-f33a4bde-a9d3-11e7-838e-0c65048ee73e.PNG)

The cost function of the regularized logistic regression is given by

![jcostfunctlogisticregressregul](https://user-images.githubusercontent.com/29837880/31242094-f362b538-a9d3-11e7-9d44-696b79c73903.PNG)

We then plot the data and decision boundary:

![nonlinearlogisticreg](https://user-images.githubusercontent.com/29837880/31242087-f33b53d0-a9d3-11e7-9d85-c5b9d41e6468.png)

The regularization parameters used was lambda = 0.01 and it proved to correctly balace bias and variance in the model.

### Variance vs Bias

Out of curiosity let's now set lambda = 100 in order for the decision line to underfit the data. 

![nonlinearlogisticregunder](https://user-images.githubusercontent.com/29837880/31242091-f3426a94-a9d3-11e7-85cd-1dd5a077a588.png)

By setting such a large lambda, we are giving less weight to the unregularized cost function to be minimized. Thus our model is more biased and less accurate.

Now let's set lambda = 0 in order for the decision line to overfit the data.

![nonlinearlogisticregover](https://user-images.githubusercontent.com/29837880/31242089-f33e73e4-a9d3-11e7-993d-e49961490e2b.png)

By setting such a small -null- lambda, we are giving all the weight to the unregularized cost function to be minimized. Thus our model fits the training data too well and has such a large variance that it will make poor predictions on new data.
