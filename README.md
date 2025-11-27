# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Input matrix dimensions and initialize augmented matrix and solution vector.

2.Populate the augmented matrix with user inputs.

3.Perform Gaussian elimination to reduce the matrix to upper triangular form, ensuring no division by zero.

4.Back substitute to compute solution values for the variables.

5.Print the solution vector formatted to two decimal places.

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by:DIVYA PRIYA.S 
RegisterNumber: 25018016

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end =" ")
        
```

## Output:
![gaussian elimination]()
<img width="1907" height="896" alt="Screenshot 2025-11-27 202145" src="https://github.com/user-attachments/assets/6804f6c8-eba1-4b67-bcd9-dcf11cf14fd5" />
<img width="1901" height="757" alt="Screenshot 2025-11-27 202314" src="https://github.com/user-attachments/assets/908b8855-b62f-4f19-a2d6-842bd21c6dda" />
<img width="1503" height="655" alt="Screenshot 2025-11-27 202329" src="https://github.com/user-attachments/assets/a3d60f63-d38a-488e-be6d-54f13d8da9aa" />

## Result:

Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

