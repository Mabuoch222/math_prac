import numpy as np

def is_diagonalizable(matrix):
    # Get the eigenvalues and eigenvectors of the matrix
    eigenvalues, eigenvectors = np.linalg.eig(matrix)

    # Check if the matrix is diagonalizable by checking if the dimension
    # of the eigenspace for each eigenvalue is equal to 1
    for eigenvalue in eigenvalues:
        if np.linalg.matrix_rank(matrix - eigenvalue * np.eye(matrix.shape[0])) > 1:
            print("The matrix is not diagonalizable.")
            return False

    print("The matrix is diagonalizable.")
    return True

def find_eigenvalues(matrix):
    eigenvalues, _ = np.linalg.eig(matrix)
    return eigenvalues
