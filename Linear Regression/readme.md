# Linear Regression

Linear regression predicts a real-valued output based on an input value.

## Simple Linear Regression model

Implementation of linear regression with one variable to predict profits for a food truck given data for profits and populations from different cities.

The objective of linear regression is to minimize the cost function

![jfunction](https://user-images.githubusercontent.com/29837880/31140946-05206f5e-a844-11e7-877b-6827cfabd34a.PNG)

where the hypothesis h(x) is given by the simple linear regression model

![simpleregressionfunction](https://user-images.githubusercontent.com/29837880/31140945-0518e7fc-a844-11e7-999a-d06db5be907f.PNG)

Thetas are the parameters of our model which are used to minimize the cost function J. This is done using the batch gradient descent algorithm where each iteration performs the update

![thetaupdate](https://user-images.githubusercontent.com/29837880/31140947-052678ea-a844-11e7-9226-3cf89442750e.PNG)


With each step of gradient descent, the parameters Thetas come closer to the optimal values that will achieve the lowest cost J.

Plot of the data and fitted linear regression line for one independent variable. 
![linearreg1](https://user-images.githubusercontent.com/29837880/31135771-0312f098-a834-11e7-9755-71598eaffe5b.png)

Surface plot of the cost function varying with changes in estimated regression parameters and eventually reaching a global minimum to provide the optimal parameters.

![costfunctionsurface](https://user-images.githubusercontent.com/29837880/31135852-5002ff1a-a834-11e7-8088-9dead7a08eab.png)

Contour plot of the cost function varying with changes in estimated regression parameters and eventually reaching a global minimum to provide the optimal parameters. Each step of the gradient descent goes moves towards the minimum.

![costfunctioncontour](https://user-images.githubusercontent.com/29837880/31135853-50074728-a834-11e7-9fad-4c77dbee15ba.png)


## Multivariate Linear Regression model

Implementation of linear regression with multiple variables to predict house prices in Portland, OR given two features: the size of the house and the number of bedrooms.

In the multivariate case, the cost function can  be written in the following vectorized form:

![jfunctionmultivariate](https://user-images.githubusercontent.com/29837880/31140944-0518876c-a844-11e7-9579-f6c9349b023b.PNG)

Plot of the cost function J versus number of iterations during a gradient descent. The cost function converges to a minimum after an appropriate learning rate was chosen.

![jfunction](https://user-images.githubusercontent.com/29837880/31135854-5007c0ea-a834-11e7-9256-0c8d32839f96.png)
