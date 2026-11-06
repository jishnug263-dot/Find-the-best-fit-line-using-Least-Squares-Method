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
from sklearn.linear_model import LinearRegression

X = np.array([2,3,4,5,6]).reshape(-1,1)
Y = np.array([20000,30000,40000,45000,50000])

model = LinearRegression()

model.fit(X,Y)

predict = model.predict(X)

print("Coefficient:",model.coef_[0])
print("Intercept:", model.intercept_)

plt.scatter(X,Y,color='blue',label='Experiance')
plt.plot(X,predict,color='red',label='Salary')
plt.title('Linear Regression Example')
plt.xlabel('Experiance')
plt.ylabel('Salary')
plt.legend() 
plt.show()

```

## Output:
<img width="818" height="617" alt="image" src="https://github.com/user-attachments/assets/20834295-e36a-4308-a916-5f06b63c9b0d" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
