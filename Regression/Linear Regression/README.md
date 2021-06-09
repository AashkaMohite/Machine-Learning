# Linear Regression

## What is Linear Regression
Linear regression model is a linear approach to explain the relationship between a dependent variable and one or more independent variables using straight line. \
The formula for straight line is y = mx + c \
<img src="https://user-images.githubusercontent.com/83816588/120738142-f2e05680-c50c-11eb-8eab-12d6c50fe51c.jpeg" width=50% height=50%> \
Here x : independent variable \
     y : dependent variable \
     m : slope (change is y with unit change in x) \
     c : intercept (when x = 0, then y = c) 
     
## Math behind it

The first step is to find a straight line between x and y but the straight line should be a ***best fit line*** 
>### what is a best fit line? 
>Best fit line refers to a line through a scatter plot of data points that best expresses the relationship between those points. \
But there can be multiple best fit lines

### so next question is how to choose the best fit line
Hence for that we need to find the minimum sum of erros for each line \
and whichever line gives the minimum error then that should be taken as best fit line \
\
now for selecting the best fit line we need to use a function called ***Cost function/ loss Function*** which uses the **mean square error** 
> ### What is Mean Square error?
>The mean squared error (MSE) tells you how close a regression line is to a set of points. \
It does this by taking the distances from the points to the regression line (these distances are the “errors”) and squaring them. \
The squaring is necessary to remove any negative signs. It also gives more weight to larger differences. \
It’s called the mean squared error as you’re finding the average of a set of errors.

But there can be million of straight lines and finding the cost function of each of line may be difficult or it can use more processing power. \
>Insead we can use ***Gradient descent*** 

consider we have 3 points as shown below  


## sklearn library for Linear Regression
