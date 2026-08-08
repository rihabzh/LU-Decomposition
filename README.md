# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
(i) To find the L and U matrix
Step 1:
Start.

Step 2:
Input the matrix 𝐴,A from the user.

Step 3:
Store the matrix as a NumPy array.

Step 4:
Call the LU decomposition function from scipy.linalg.lu(A) which decomposes the matrix into three matrices: P: Permutation matrix L: Lower triangular matrix U: Upper triangular matrix

Step 5:
Extract P, L, and U from the function output.

Step 6:
Display the L (lower triangular matrix). Display the U (upper triangular matrix).

Step 7:
End.

(ii) To find the LU Decomposition of a matrix
Step 1:
Start

Step 2:
Input the coefficient matrix A.

Step 3:
Input the constant matrix (right-hand side vector) B.

Step 4:
Perform LU factorization of matrix A using lu_factor(A), which returns: A combined matrix containing the factors of L and U. A pivoting array P representing row interchanges.

Step 5:
Solve the system of equations AX=B using the LU factors and the pivoting array with lu_solve((L, P), B).

Step 6:
Store the result in variable X.

Step 7:
Print the solution vector X.

Step 8:
End
## Program:
(i) To find the L and U matrix
```
'''
Program to find L and U matrix using LU decomposition.
Developed by: RIHAB ZAKKAIR HUSSAIN
RegisterNumber: 212225230226
'''

import os
os.environ["OPENBLAS_NUM_THREADS"] ='1'

import numpy as np
from scipy.linalg import lu
m=np.array(eval(input()))
p,l,u=lu(m)
print(l)
print(u)
```
(ii) To find the LU Decomposition of a matrix
```
'''Program to solve a matrix using LU decomposition.
Developed by: RIHAB ZAKKAIR HUSSAIN
RegisterNumber: 212225230226
'''
import os
os.environ["OPENBLAS_NUM_THREADS"] ='1'
 
# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
m=np.array(eval(input()))
c=np.array(eval(input()))
piv,lu= lu_factor(m)
re=lu_solve((piv,lu),c)
print(re)
```

## Output:
1. <img width="887" height="721" alt="Screenshot 2026-08-08 143608" src="https://github.com/user-attachments/assets/ed420236-c400-4a8b-82d6-e4a5c938dd73" />

2. <img width="673" height="541" alt="Screenshot 2026-08-08 143615" src="https://github.com/user-attachments/assets/f0411338-fe9e-450c-9b3f-9ede16ddbaae" />


## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

