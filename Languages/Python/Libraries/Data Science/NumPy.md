# NumPy

NumPy is a powerful library for numerical computing in Python. It provides support for arrays, matrices, and many mathematical functions to operate on these data structures.

## Installation

You can install NumPy using pip:

```bash
pip install numpy
```

## Importing NumPy

To use NumPy, you need to import it:

```python
import numpy as np
```

## Creating Arrays

### From a List

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
print(a)
```

### From a Tuple

```python
import numpy as np

b = np.array((1, 2, 3, 4, 5))
print(b)
```

### From a List of Lists

```python
import numpy as np

c = np.array([[1, 2, 3], [4, 5, 6]])
print(c)
```

## Array Attributes

### Shape

```python
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6]])
print(a.shape)
```

### Data Type

```python
import numpy as np

a = np.array([1, 2, 3])
print(a.dtype)
```

## Array Operations

### Element-wise Addition

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = a + b
print(c)
```

### Element-wise Multiplication

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = a * b
print(c)
```

### Dot Product

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
dot_product = np.dot(a, b)
print(dot_product)
```

## Array Slicing

### Basic Slicing

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
print(a[1:4])
```

### Slicing 2D Arrays

```python
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(a[0:2, 1:3])
```

## Array Reshaping

### Reshape 1D to 2D

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5, 6])
b = a.reshape((2, 3))
print(b)
```

### Reshape 2D to 3D

```python
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6]])
b = a.reshape((2, 1, 3))
print(b)
```

## Array Concatenation

### Concatenate 1D Arrays

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = np.concatenate((a, b))
print(c)
```

### Concatenate 2D Arrays

```python
import numpy as np

a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
c = np.concatenate((a, b), axis=0)
print(c)
```

## Array Splitting

### Split 1D Array

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5, 6])
b = np.split(a, 3)
print(b)
```

### Split 2D Array

```python
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
b = np.split(a, 3)
print(b)
```

## Mathematical Functions

### Square Root

```python
import numpy as np

a = np.array([1, 4, 9, 16])
b = np.sqrt(a)
print(b)
```

### Exponential

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.exp(a)
print(b)
```

### Logarithm

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.log(a)
print(b)
```

## Random Numbers

### Random Array

```python
import numpy as np

a = np.random.rand(3, 3)
print(a)
```

### Random Integer

```python
import numpy as np

a = np.random.randint(1, 10, size=(3, 3))
print(a)
```

## Linear Algebra

### Matrix Multiplication

```python
import numpy as np

a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
c = np.matmul(a, b)
print(c)
```

### Determinant

```python
import numpy as np

a = np.array([[1, 2], [3, 4]])
det = np.linalg.det(a)
print(det)
```

### Inverse

```python
import numpy as np

a = np.array([[1, 2], [3, 4]])
inv = np.linalg.inv(a)
print(inv)
```

## Statistics

### Mean

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
mean = np.mean(a)
print(mean)
```

### Median

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
median = np.median(a)
print(median)
```

### Standard Deviation

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
std_dev = np.std(a)
print(std_dev)
```

## Saving and Loading

### Save to File

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
np.save('array.npy', a)
```

### Load from File

```python
import numpy as np

a = np.load('array.npy')
print(a)
```
