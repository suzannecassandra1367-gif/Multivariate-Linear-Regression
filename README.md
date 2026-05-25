# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>
Import required libraries and initialize the input data X and Y.
### Step2
<br>
Plot the input data using a scatter plot to visualize the relationship.
### Step3
<br>
Calculate the mean values of X and Y.
### Step4
<br>
Compute the slope (m) and intercept (c) using the linear regression formulas.
### Step5
<br>
Predict values and plot the regression line along with actual data points.
## Program:
```
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing Input data
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

plt.scatter(X, Y)
plt.show()

import numpy as np

X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Building the model
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
c = Y_mean - m * X_mean

print("Slope =", m)
print("Intercept =", c)

import numpy as np
import matplotlib.pyplot as plt

X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Values from model
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
c = Y_mean - m * X_mean

# Making predictions
Y_pred = m * X + c

print(Y_pred)

plt.scatter(X, Y)  # actual points
plt.plot([min(X), max(X)],
         [min(Y_pred), max(Y_pred)],
         color='red')

plt.show()





```
## Output:

<img width="764" height="536" alt="Screenshot 2026-05-25 114652" src="https://github.com/user-attachments/assets/d6c22c89-baf4-4070-96aa-2c56feb72c00" />

<img width="535" height="206" alt="Screenshot 2026-05-25 114718" src="https://github.com/user-attachments/assets/81fb710d-c34e-4581-868c-eca54f510723" />

<img width="932" height="618" alt="Screenshot 2026-05-25 114749" src="https://github.com/user-attachments/assets/c4503384-d740-4b80-b9ce-ea3bd98e257e" />




<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
