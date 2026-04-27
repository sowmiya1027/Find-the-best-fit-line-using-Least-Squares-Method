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
Developed by: Sowmiya R 
RegisterNumber: 212225040420    
*/

import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])     
y = np.array([2, 4, 5, 4, 5])     

x_mean = np.mean(x)
y_mean = np.mean(y)

n = len(x)

m = np.sum((x - x_mean) * (y - y_mean)) / np.sum((x - x_mean) ** 2)
c = y_mean - m * x_mean

print(f"Slope (m): {m}")
print(f"Intercept (c): {c}")

y_pred = m * x + c

plt.scatter(x, y, color='blue', label='Actual data')
plt.plot(x, y_pred, color='red', label='Fitted line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression using Least Squares')
plt.legend()
plt.show()
```


## Output:
<img width="806" height="612" alt="Screenshot 2026-04-27 190146" src="https://github.com/user-attachments/assets/d115e521-2616-463d-9c2a-e347b23b328b" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
