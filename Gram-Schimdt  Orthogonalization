import numpy as np

def gram_schmidt_orthogonalization(vectors):
    # Initialize the orthogonal and orthonormal bases
    orthogonal_basis = []
    orthonormal_basis = []

    for v in vectors:
        # Subtract the projections of v onto previous orthogonal vectors
        w = v - np.sum([np.dot(v, u) / np.dot(u, u) * u for u in orthogonal_basis], axis=0)
        orthogonal_basis.append(w)

        # Normalize the orthogonal vector to get the orthonormal vector
        norm = np.linalg.norm(w)
        if norm == 0:
            orthonormal_basis.append(np.zeros_like(w))
        else:
            orthonormal_basis.append(w / norm)

    return orthonormal_basis
