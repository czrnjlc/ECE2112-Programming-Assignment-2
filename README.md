# Programming Assignment 2: Data Normalization and Filtering
## Overview
This repository contains Python scripts for two data processing tasks:

### 1. Normalization Problem: 
This script creates a 5x5 NumPy array of random numbers, normalizes it, and saves the result to a file.
### 2. Divisible by 3 Problem: 
This script creates a 10x10 NumPy array of squares of the first 100 positive integers, filters out elements divisible by 3, and saves these elements to a file.

## Scripts
### 1. Normalization
#### Objective: Generate a 5x5 array of random numbers, normalize it, and save the result.
#### Process:
1. Create a 5x5 array with random numbers.
2. Normalize the array using the formula: 𝑍 = 𝑋 − mean/std
3. Save the normalized array to X_normalized.npy.

Code:
```python
import numpy as np

# Generate a 5x5 array of random numbers
X = np.random.random((5, 5))

# Function to normalize the array
def normalization(z):
    m = z.mean()
    s = z.std()
    Z = (z - m) / s
    return Z

# Normalize the array
X_normalized = normalization(X)

# Save the normalized array to a file
np.save('X_normalized.npy', X_normalized)
```

### 2. Divisible by 3
#### Objective: Create a 10x10 array of squares from 1 to 100, filter elements divisible by 3, and save the result.
#### Process:
1. Generate a 10x10 array with squares of the first 100 integers.
2. Filter elements that are divisible by 3.
3. Save these elements to div_by_3.npy.

Code:

```python
Copy code
import numpy as np

Create a 10x10 array of squares from 1 to 100
x = (np.arange(1, 101) ** 2).reshape(10, 10)

Filter elements divisible by 3
squares_div_by_3 = x[x % 3 == 0]

Save the filtered elements to a file
np.save('div_by_3.npy', squares_div_by_3)
```
### Metadata
#### Name: Cueco, Czarina Julia C.
#### Section: 2ECE-B
#### Date Submitted: September 2, 2024
