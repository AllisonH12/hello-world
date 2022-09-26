import numpy as np

def getsumofneighbors(matrix, i, j):
    region = matrix[max(0, i-1) : i+2,
                    max(0, j-1) : j+2]
    return np.sum(region) - matrix[i, j] # Sum the region and subtract center
    
array = [[1, 2, 3],
         [1, 2, 4]
         [2, 5, 3]]

print(getsumofneighbors(array, 0, 0))