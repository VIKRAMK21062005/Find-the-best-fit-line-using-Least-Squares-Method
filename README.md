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

# Preprocessing Input data

X=np.array(eval(input()))
Y=np.array(eval(input()))

# Mean
Xmean=np.mean(X)
Ymean=np.mean(Y)
num=0 #for slope
den=0 #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
  num+=(X[i]-Xmean)*(Y[i]-Ymean)
  den+=(X[i]-Xmean)**2

#calculate slope
m=num/den

#claculate intercept
b=Ymean-m*Xmean
print(m,b)
#Line equation
Y_pred=m*X+b
print(Y_pred)

#to plot grap
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()
```
## Output:
3.6,4.8,7.2,6.9,10.7,6.1,7.9,9.5,5.4
9.3,10.2,11.5,12,18.6,13.2,10.8,22.7,12.7
1.537302371541502 2.8370580808080827
[ 8.37134662 10.21610946 13.90563516 13.44444444 19.28619346 12.21460255
 14.98174682 17.44143061 11.13849089]
![ml-01](https://github.com/VIKRAMK21062005/Find-the-best-fit-line-using-Least-Squares-Method/assets/120624033/f7562694-acb9-4228-aa6f-6f130d7aef54)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
