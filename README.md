# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy as np and import sys
2. Get the inputs of the matrix to be calculated
3. Develop a sub program to proceed with Gaussian elimination method
4. Develop a sub program to calculate the unknowns using back substitution method
5. Print the result obtained

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Dharini PV
RegisterNumber: 212222240024
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exist('Divide by Zero found')
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
    print("X%d = %0.2f"%(i,x[i]),end=' ')
```

## Output:
![image](https://github.com/DHARINIPV/Gaussian/assets/119400845/db98c233-bb60-4b12-8965-1e78f3cacbba)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

