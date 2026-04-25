# EXP 1: Implementation of Univariate Linear Regression

# REG NO:212224040052

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
import numpy as np
import matplotlib.pyplot as plt

X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 5, 4, 5])

n = len(X)

sum_x = np.sum(X)
sum_y = np.sum(Y)
sum_xy = np.sum(X * Y)
sum_x2 = np.sum(X * X)

m = (n * sum_xy - sum_x * sum_y) / (n * sum_x2 - sum_x ** 2)
c = (sum_y - m * sum_x) / n

print("Slope (m) =", m)
print("Intercept (c) =", c)

Y_pred = m * X + c
print("Predicted values:", Y_pred)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()


```

## Output:
<img width="1048" height="661" alt="image" src="https://github.com/user-attachments/assets/2d7af708-63b2-4d4e-adf3-43da6ab62730" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
