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
import numpy as np

def determinant(a, b, c, d):
    return a * d - b * c

D = determinant(1, -3, 3, 1)
Dx = determinant(0, -3, 10, 1)
Dy = determinant(1, 0, 3, 10)

if D != 0:
    x = Dx / D
    y = Dy / D
    result = np.array([x, y])
    print(result)
else:
    print("The system has no unique solution.")
```
## Output:
![EXPERIMENT MATHS FOR AI 1](https://github.com/user-attachments/assets/b01157b1-d885-4e3e-85fe-23a232ac527d)

## Result: 
Thus the solutions for the linear equations are successfully solved using python program

