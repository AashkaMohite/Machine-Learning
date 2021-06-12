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
now for selecting the best fit line we need to use a function called ***Cost function/ loss Function*** which uses the **mean squared error** 
> ### What is Mean Square error?
>The mean squared error (MSE) tells you how close a regression line is to a set of points. \
It does this by taking the distances from the points to the regression line (these distances are the “errors”) and squaring them. \
The squaring is necessary to remove any negative signs. It also gives more weight to larger differences. \
It’s called the mean squared error as you’re finding the average of a set of errors. \
> <img src=1> \
> now whichever line gives the minimum error is considered as best fit line. \

But there can be million of straight lines and finding the cost function of each of line may be difficult or it can use more processing power. 
>Insead we can use ***Gradient descent*** 

consider we have 3 points as shown below  \ 
<img 2> \
<img 3> \
<img 4> \
Therefore when slope is 1 the error is 0. \
\
Now plotting the error and slope of case 1 on another graph \
<img 5> \
\
<img 6> \
When slope = 0.5 the error is 1.16 \
Now plotting the error and slope of case 2 on graph \
<img 7>\
\
<img 8>
When slope = 1.5 the error is 1.16 \
Now plotting the error and slope of case 3 on graph \
<img 9> \

And eventually the graph wil be like as below:
<img 10>
This graph is known as **Gradient descent** \
\
Now we have to reach to this global minima and for that we will use the convergence theorem \
<img 11> \
\
Consider you got a error based on some slope value \
<img 12\
\
Now we can go downward using convergence theorem \
to find out the next point then use convergence theorem \
<img 13> \

here α is taken as 0.001 \
the α should not be too large as it will miss the global minima \
and α should not be too small as it will take too much time to reach global minima \
\
As soon as it reaches to global minima, the slope will be zero and at that time **m** value will represent the slope of best fit line \
When there will be more than one feature then the gradient descent will be 3D like a bowl and each and every feature will try to reach the global minima. \
<img 14>
## sklearn library for Linear Regression

#### References 
1. https://www.analyticsvidhya.com/blog/2021/04/gradient-descent-in-linear-regression/
2. 
