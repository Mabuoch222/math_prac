import numpy as np

def Gauss_elimination(A, B):
    n = len(B)
    for i in range(0, n):
        for j in range(i+1, n):
            factor = A[j][i] / A[i][i]
            for k in range(i, n):
                A[j][k] = A[j][k] - factor * A[i][k]
            B[j] = B[j] - factor * B[i]
    X = np.zeros((n,1))
    X[n-1] = B[n-1] / A[n-1][n-1]
    for i in range(n-2, -1, -1):
        sum_ = B[i]
        for j in range(i+1, n):
            sum_ = sum_ - A[i][j] * X[j]
        X[i] = sum_ / A[i][i]
    return X

A = np.array([[2, 1, -1], [-3, -1, 2], [-2, 1, 2]])
B = np.array([[8], [-11], [-3]])

result = Gauss_elimination(A, B)
print(result)
