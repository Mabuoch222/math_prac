import numpy as np

def divergence(f, x, h=1e-4):
    divergence = 0
    for i in range(x.shape[0]):
        x_plus = np.copy(x)
        x_minus = np.copy(x)
        x_plus[i] += h
        x_minus[i] -= h
        divergence += (f(x_plus)[i] - f(x_minus)[i]) / (2 * h)
    return divergence

# Example usage
def f(x):
    return np.array([x[0] + x[1], x[0] - x[1]])

x = np.array([1, 2])
div = divergence(f, x)
print("Divergence: ", div)
