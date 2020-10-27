import numpy as np

def spline_linear(xi, yi, x):
    spline = np.array([(yi[1:] - yi[:-1]) / (xi[1:] - xi[:-1]), yi[:-1]])
    dif = xi - np.array([x]).T
    dif[dif > 0] = np.max(dif)
    pos = np.minimum(np.argmin(np.abs(dif), axis=1), len(xi) - 2)
    return spline[0][pos] * (x - xi[pos]) + spline[1][pos]
