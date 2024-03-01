# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Amrutha varshni
RegisterNumber: 212222040007
*/
import numpy as np
import matplotlib.pyplot as plt

# proceeding input data

x=np.array(eval(input()))
y=np.array(eval(input()))

# mean

x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0

# to find sum of(xi-x')&(yi-y')&(xi-x')^2

for i in range(len(x)):
    num+=(x[i]-x_mean*(y[i]-y_mean))
    denom+=(x[i]-x_mean)**2
    m=num/denom

# calculate intercept

b=y_mean-m*x_mean
print(m,b)

# line equation

y_predicted=m*x+b
print(y_predicted)

# to plot graph

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```

## Output:
![image](https://github.com/Priya-Loganathan/Find-the-best-fit-line-using-Least-Squares-Method/assets/121166075/099155ff-119d-45b6-b979-8816ed7ec877)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
