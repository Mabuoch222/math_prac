import numpy as np
from scipy.linalg import null_space, orth

def basis_of_matrix_space(matrix):
    # Compute the basis of column space
    col_basis = orth(matrix.T)

    # Compute the basis of null space
    null_basis = null_space(matrix)

    # Compute the basis of row space
    row_basis = orth(matrix)

    # Compute the basis of left null space
    left_null_basis = null_space(matrix.T)

    return col_basis, null_basis, row_basis, left_null_basis
