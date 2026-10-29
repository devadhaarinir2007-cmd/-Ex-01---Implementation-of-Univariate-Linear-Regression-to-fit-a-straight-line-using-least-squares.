# -Ex-01---Implementation-of-Univariate-Linear-Regression-to-fit-a-straight-line-using-least-squares.

## Aim:
To write a  univariate Linear Regression to fit a straight line using least squares

## Objective:
This program fits a straight line (a regression line) to a set of data points (𝑥,𝑦) using the Least Squares Method — that is, it finds the best line that minimizes the total squared difference between the actual and predicted y values.

The line equation is: y=mx+b

where m → slope of the line and b → y-intercept

## Algorithm:
 1. Import necessary libraries
 2. Input data
 3. Compute the means
 4. Calculate numerator and denominator for the slope
 5. Compute slope and intercept
 6. Predict y values
 7. Display results
 8. Plot the results

## Program:
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

x_mean = np.mean(x)
y_mean = np.mean(y)

num = 0
denom = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean)**2

m = num / denom
b = y_mean - m * x_mean

y_predicted = m * x + b
print(y_predicted)

print(m, b)

plt.scatter(x, y)                # Plot the actual data points
plt.plot(x, y_predicted, color='red')  # Plot the regression line
plt.show()
```

## Output:
<img width="270" height="35" alt="image" src="https://github.com/user-attachments/assets/e8211538-e6d8-4504-b6e7-9570e60c912f" />

<img width="126" height="32" alt="image" src="https://github.com/user-attachments/assets/d9627a2d-36de-49c8-acf2-660dd8095a1b" />

<img width="717" height="558" alt="image" src="https://github.com/user-attachments/assets/d2e481b4-5a48-473e-b817-5eeb554f293f" />

## Result:
Thus, univariate linear regression was implemented successfully using the least squares method in Python to fit a straight line to the given data.
