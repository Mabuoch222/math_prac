import numpy as np

def echelon_form(A):
    n, m = np.shape(A)
    for i in range(n):
        pivot = A[i][i]
        for j in range(i+1, n):
            factor = A[j][i] / pivot
            for k in range(i, m):
                A[j][k] = A[j][k] - factor * A[i][k]
    return A

def rank(A):
    echelon_matrix = echelon_form(A)
    n, m = np.shape(echelon_matrix)
    rank = n
    for i in range(n):
        zero_row = True
        for j in range(m):
            if echelon_matrix[i][j] != 0:
                zero_row = False
                break
        if zero_row:
            rank = rank - 1
    return rank

A = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print("Echelon Form:")
print(echelon_form(A))
print("Rank:", rank(A))
