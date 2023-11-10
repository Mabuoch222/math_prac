import numpy as np

def curl(f, x, h=1e-4):
    curl = np.zeros(2)
    for i in range(x.shape[0]):
        x_plus = np.copy(x)
        x_minus = np.copy(x)
        x_plus[i] += h
        x_minus[i] -= h
        curl[i] = (f(x_plus)[(i + 1) % 2] - f(x_minus)[(i + 1) % 2]) / (2 * h)
    curl[1], curl[0] = -curl[0], curl[1]
    return curl

# Example usage
def f(x):
    return np.array([x[0] + x[1], x[0] - x[1]])

x = np.array([1, 2])
c = curl(f, x)
print("Curl: ", c)
