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
import pandas as pd
import numpy as np

# Read CSV file
data = pd.read_csv("50_Startups.csv")

# Select input and output
X = data[['R&D Spend']].values
y = data['Profit'].values

# Normalize input
X_mean = np.mean(X)
X_std = np.std(X)
X = (X - X_mean) / X_std

# Initialize parameters
m = 0
b = 0
learning_rate = 0.01
iterations = 1000
n = len(X)

# Gradient Descent
for i in range(iterations):
    y_pred = m * X.flatten() + b

    dm = (-2 / n) * np.sum(X.flatten() * (y - y_pred))
    db = (-2 / n) * np.sum(y - y_pred)

    m = m - learning_rate * dm
    b = b - learning_rate * db

# Display model parameters
print("Slope:", m)
print("Intercept:", b)

# Predict profit for a new city
rd_spend = float(input("Enter R&D Spend: "))

rd_scaled = (rd_spend - X_mean) / X_std
profit = m * rd_scaled + b

print("Predicted Profit:", profit)

```


## Output:
<img width="996" height="627" alt="image" src="https://github.com/user-attachments/assets/86bb69a9-5d75-4395-add1-fcedc01e40f7" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
