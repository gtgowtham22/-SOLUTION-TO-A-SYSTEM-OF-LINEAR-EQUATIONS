# -SOLUTION-TO-A-SYSTEM-OF-LINEAR-EQUATIONS
## Aim:
To write a python program to find a solution to a system of linear equations.
## Equipment’s required:
1. 	Hardware – PCs
2. 	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step 1: 
Import the numpy module to use the built-in functions for calculation
### Step 2: 
Prepare the lists from each linear equations and assign in np.array()
### Step 3: 
Using the np.linalg.solve(), we can find the solutions.
### Step 4: 
End the program
## Program:
```
#Program to find the solution for the given linear equations.
#Developed by: G.T.GOWTHAM
#RegisterNumber:24901330
import numpy as np

# Given system of equations:
# 5x - 3y - 10z = -9
# 2x + 2y - 3z  = 4
# -3x - y + 5z  = -1

# Determinant function for 3x3 matrix
def determinant(a, b, c, d, e, f, g, h, i):
    return (a * (e * i - f * h) - 
            b * (d * i - f * g) + 
            c * (d * h - e * g))

# Coefficient matrix determinant (D)
D = determinant(5, -3, -10,
                2,  2, -3,
               -3, -1,  5)

# Dx matrix determinant (replace first column with constants)
Dx = determinant(-9, -3, -10,
                  4,  2, -3,
                 -1, -1,  5)

# Dy matrix determinant (replace second column with constants)
Dy = determinant(5, -9, -10,
                 2,  4, -3,
                -3, -1,  5)

# Dz matrix determinant (replace third column with constants)
Dz = determinant(5, -3, -9,
                 2,  2,  4,
                -3, -1, -1)

# Check if system has a unique solution
if D != 0:
    x = Dx / D
    y = Dy / D
    z = Dz / D
    # Print in exact NumPy format
    result = np.array([x, y, z])
    print(result)
else:
    print("The system has no unique solution.")
```
## Output:
![ex1 mathsai](https://github.com/user-attachments/assets/00324714-c282-49f8-bd24-3526093f7b22)


## Result: 
Thus the solutions for the linear equations are successfully solved using python program

