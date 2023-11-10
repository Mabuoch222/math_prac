import numpy as np

def check_linear_dependence(vectors):
    # Convert the list of vectors to a matrix
    matrix = np.column_stack(vectors)
    rank = np.linalg.matrix_rank(matrix)

    if rank < len(vectors):
        print("The vectors are linearly dependent.")
        return True
    else:
        print("The vectors are linearly independent.")
        return False

def generate_linear_combination(coefficients, vectors):
    # Multiply each vector by its coefficient and sum them up
    return np.sum([c * v for c, v in zip(coefficients, vectors)], axis=0)
