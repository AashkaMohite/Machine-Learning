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
> <img src="https://user-images.githubusercontent.com/83816588/121772476-2bc69e00-cb93-11eb-925e-ec03c6578c76.jpeg" width=80% height=50%> \
> now whichever line gives the minimum error is considered as best fit line. 

But there can be million of straight lines and finding the cost function of each of line may be difficult or it can use more processing power. 
>Insead we can use ***Gradient descent*** 

consider we have 3 points as shown below  
<img src="https://user-images.githubusercontent.com/83816588/121772537-87912700-cb93-11eb-8f3f-23154857bb47.jpeg" width=80% height=50%> 

### case 1
<img src="https://user-images.githubusercontent.com/83816588/121772571-abed0380-cb93-11eb-9ac0-b019462b2d3d.jpeg" width=80% height=50%> \
<img src="https://user-images.githubusercontent.com/83816588/121772614-fff7e800-cb93-11eb-958f-f7699bee8a35.jpeg" width=80% height=50%> \
Therefore when slope is 1 the error is 0. \
\
Now plotting the error and slope of case 1 on another graph 
<img src="https://user-images.githubusercontent.com/83816588/121772627-1a31c600-cb94-11eb-8202-708b3aa75bfd.jpeg" width=80% height=50%> 

### case 2
<img src="https://user-images.githubusercontent.com/83816588/121772649-49e0ce00-cb94-11eb-823e-5ac4c358bafe.jpeg" width=80% height=50%> \
When slope = 0.5 the error is 1.16 \
Now plotting the error and slope of case 2 on graph 
<img src="https://user-images.githubusercontent.com/83816588/121772661-5d8c3480-cb94-11eb-894e-1915df43b695.jpeg" width=80% height=50%>

### case 3
<img src="https://user-images.githubusercontent.com/83816588/121772667-6977f680-cb94-11eb-9690-47b813e46d45.jpeg" width=80% height=50%> \
When slope = 1.5 the error is 1.16 \
Now plotting the error and slope of case 3 on graph 
<img src="https://user-images.githubusercontent.com/83816588/121772674-7c8ac680-cb94-11eb-8c37-775d1f3db284.jpeg" width=80% height=50%> \
\
And eventually the graph wil be like as below: \
<img src="https://user-images.githubusercontent.com/83816588/121772682-88768880-cb94-11eb-97bf-fdbcef170fe6.jpeg" width=50% height=20%> \
This graph is known as **Gradient descent** \
\
Now we have to reach to this global minima and for that we will use the convergence theorem \
<img src="https://user-images.githubusercontent.com/83816588/121772691-94624a80-cb94-11eb-8af1-a7e8917d6cd2.jpeg" height=50%> \
\
Consider you got a error based on some slope value \
<img src="https://user-images.githubusercontent.com/83816588/121772695-a04e0c80-cb94-11eb-8fcc-b15c19c8f355.jpeg" height=50%> \
\
Now we can go downward using convergence theorem \
to find out the next point then use convergence theorem \
<img src="https://user-images.githubusercontent.com/83816588/121772700-b065ec00-cb94-11eb-813f-10c9f10cbef5.jpeg" width=50% height=20%> 

here α is taken as 0.001 \
the α should not be too large as it will miss the global minima \
and α should not be too small as it will take too much time to reach global minima \
\
As soon as it reaches to global minima, the slope will be zero and at that time **m** value will represent the slope of best fit line \
When there will be more than one feature then the gradient descent will be 3D like a bowl and each and every feature will try to reach the global minima. \
<img src="https://user-images.githubusercontent.com/83816588/121772197-9080f900-cb91-11eb-8daf-a900b2809be5.png" width=50% height=30%> 
\
## sklearn library for Linear Regression
```python
from sklearn.linear_model import LinearRegression
reg = LinearRegression().fit(X, y)
```
<img src="https://user-images.githubusercontent.com/83816588/121773594-8adbe100-cb9a-11eb-875d-1631827acb80.png">
<img src="https://user-images.githubusercontent.com/83816588/121773608-a3e49200-cb9a-11eb-9c47-09ff4b6f1318.png">

#### References 
1. https://www.analyticsvidhya.com/blog/2021/04/gradient-descent-in-linear-regression/ 
2. https://youtu.be/1-OGRohmH2s 
3. https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html
