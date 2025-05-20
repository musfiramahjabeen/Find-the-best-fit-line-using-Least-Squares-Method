# EXP1 - Implementation of Univariate Linear Regression
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
```python
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: MUSFIRA MAHJABEEN M
RegisterNumber:  212223230130
*/
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y) 
num=0
de=0
for i in range(len(x)):
           num+=(x[i]-x_mean)*(y[i]-y_mean)
           de+=(x[i]-x_mean)**2 
m=round(num/de,2)
c=round(y_mean-m*x_mean,2)
y_predict=m*x+c
print("Numerator : ",num)
print("Denominator : ",de)
print("Slope / m : ",m)
print("Y-Intercept : ",c)
print("Y-Precict : ",y_predict)
plt.scatter(x,y,color='purple')
plt.plot(x,y_predict,color='brown') 
plt.show() 

```

## Output:
![Screenshot 2024-02-20 090926](https://github.com/MOHAMEDAHSAN/Find-the-best-fit-line-using-Least-Squares-Method/assets/139331378/c973cb04-5382-4d64-a1b6-54810c0d993f)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
