# Implementation-of-Linear-Regression-Using-Gradient-Descent
# NAME: DEEPAKKUMAR S
# REG NO: 212225230042
## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Initialize the input data (city population) and output data (profit).

2.Initialize the slope, intercept, learning rate, and number of iterations.

3.Calculate the predicted profit and update the slope and intercept using Gradient Descent .

4.Use the trained model to predict the profit for a new city population.


## Program:

```

import numpy as np

# Input data: City population (in 10,000s)
X = np.array([6.1, 5.0, 8.2, 7.5, 4.5, 9.0, 3.5, 6.8])

# Output data: Profit (in $10,000s)
y = np.array([17.0, 14.0, 25.0, 22.0, 13.0, 28.0, 10.0, 20.0])

# Initialize parameters
m = 0
c = 0

# Learning rate and number of iterations
learning_rate = 0.01
iterations = 1000

n = len(X)

# Gradient Descent
for i in range(iterations):

    # Prediction
    y_pred = m * X + c

    # Calculate gradients
    dm = (-2 / n) * np.sum(X * (y - y_pred))
    dc = (-2 / n) * np.sum(y - y_pred)

    # Update parameters
    m = m - learning_rate * dm
    c = c - learning_rate * dc

# Display model parameters
print("Slope (m):", m)
print("Intercept (c):", c)

# Predict profit for a new city
population = float(input("Enter city population (in 10,000s): "))

profit = m * population + c

print("Predicted Profit:", profit, "($10,000s)")

```


## Output:
<img width="939" height="707" alt="image" src="https://github.com/user-attachments/assets/336f8d11-7ec0-48e5-ad51-c85eeb285586" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
