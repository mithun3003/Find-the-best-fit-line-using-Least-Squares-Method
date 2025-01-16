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
Developed by:MITHUN S
RegisterNumber:24901037
*/
```
```
import numpy as np
import matplotlib.pyplot as plt
#preprocessing Input data
x= np.array(eval(input()))
y= np.array(eval(input()))
#Mean
x_mean =np.mean(x)
y_mean =np.mean(y)
num=0
denom=0
for i in range(len(x)):
 num+=(x[i]-x_mean)*(y[i]-y_mean)
 denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean - m*x_mean
print(m,b)
y_predicted=m*x+b
print(y_predicted)
plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```

## Output:
![best fit line](sam.png)
8,2,11,6,5,4,12,9,6,1 
3,10,3,6,8,12,1,4,9,14
-1.1064189189189189 14.08108108108108
[ 5.22972973 11.86824324 1.91047297 7.44256757 8.54898649 9.65540541
0.80405405 4.12331081 7.44256757 12.97466216]
![Screenshot 2024-10-11 212422](https://github.com/user-attachments/assets/e7ec921f-c524-467b-b391-412ac342f0a5)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
