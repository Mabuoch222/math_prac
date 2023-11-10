import numpy as np

def gradient(f, x, h=1e-4):
    gradient = np.zeros_like(x)
    for i in range(x.shape[0]):
        x_plus = np.copy(x)
        x_minus = np.copy(x)
        x_plus[i] += h
        x_minus[i] -= h
        gradient[i] = (f(x_plus) - f(x_minus)) / (2 * h)
    return gradient

# Example usage
def f(x):
    return x[0]**2 + x[1]**2

x = np.array([1, 2])
grad = gradient(f, x)
print("Gradient: ", grad)
