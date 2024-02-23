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
Developed by: 
RegisterNumber:  
*/
import numpy as np
import matplotlib.pyplot as plt 
x = np.array([0,1,2,3,4,5,6,8,9,10])
y = np.array([1,3,2,5,7,8,8,9,10,12])
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range (len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean 
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='blue')
plt.show()
```

## Output:
![screen spot 1](https://github.com/ganesanmohan/Find-the-best-fit-line-using-Least-Squares-Method/assets/161014098/b6b8671e-5443-4375-9aa5-7536fcd05630)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
