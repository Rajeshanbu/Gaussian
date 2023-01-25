# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### 1.import numpy as np
### 2.get the input matrix 
### 3.find the guassian elimination 
### 4.print tyhe result 

## Program:
```python
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by:Rajesh A
RegisterNumber: 22008551
'''
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
        sys.exit('divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for  k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
```

## Output:
![guassian Rajesh A,22008551](https://user-images.githubusercontent.com/118924713/214554493-a0b78267-9995-4457-bab6-7621441c0b21.png)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

