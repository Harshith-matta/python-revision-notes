# Introduction to NumPy

NumPy is a Python library used for numerical computations.

It is widely used in:

- Data Science
- Machine Learning
- Scientific Computing

```python
import numpy as np
```

---

# Creating Arrays

```python
arr1 = np.array([1, 2, 3])                 # 1D array
arr2 = np.array([[1, 2], [3, 4]])          # 2D array
arr3 = np.array([[[1, 2], [3, 4]],
                 [[5, 6], [7, 8]]])        # 3D array

print(arr1)
print(arr2)
print(arr3)
```

---

# Array Properties

```python
arr = np.array([1, 2, 3])

print(arr.ndim)   # number of dimensions
print(arr.shape)  # shape of array
```

---

# Creating Special Arrays

```python
a0 = np.zeros((3, 3))
a1 = np.ones((2, 2))
ar = np.arange(0, 10, 2)

print(a0)
print(a1)
print(ar)
```

---

# Indexing and Slicing

```python
arr = np.array([1,2,3,4,5,6,7,8,9])

print(arr[1])        # single element
print(arr[-1])       # last element
print(arr[0:2])      # slicing
print(arr[::2])      # step slicing
```

---

## 2D Indexing

```python
a2 = np.array([[1,2,3],
               [4,5,6],
               [7,8,9]])

print(a2[1, 0])     # row 1, column 0
print(a2[:, 1])     # all rows, column 1
```

---

# Reshaping Arrays

```python
arr = np.array([1,2,3,4,5,6,7,8,9])

reshaped = arr.reshape(3, 3)
print(reshaped)
```

---

# Arithmetic Operations

```python
x = np.array([1,2,3])
y = np.array([4,5,6])

print(x + y)
print(x - y)
print(x * y)
print(x / y)
```

---

# Universal Functions

```python
a = np.array([-3, -1, 0, 1, 3])

print(np.absolute(a))
print(np.sqrt(a))
print(np.exp(a))
print(np.sin(a))
```

---

# Aggregation Functions

```python
array = np.array([[1,2,3],
                  [4,5,6]])

print(np.sum(array))
print(np.mean(array))
print(np.std(array))
print(np.var(array))
print(np.min(array))
print(np.max(array))
print(np.argmax(array))

print(np.sum(array, axis=0))
print(np.sum(array, axis=1))
```

---

# Broadcasting

```python
arr = np.array([1,2,3])

print(arr + 1)
print(arr * 2)
```

---

# Filtering (Boolean Indexing)

```python
ages = np.array([[21,17,19,20,16,30,18,65],
                 [39,22,15,99,18,19,20,21]])

teenagers = ages[ages < 18]
adults = ages[(ages >= 18) & (ages < 65)]
seniors = ages[ages >= 65]

print(teenagers)
print(adults)
print(seniors)
```

---

# Using np.where()

```python
print(np.where(ages >= 18, ages, 0))
```

---

# Random Numbers

```python
rng = np.random.default_rng()

print(rng.integers(1, 7, size=3))
print(np.random.uniform(-1, 1, size=(3, 2)))
```

---

# Random Choice and Shuffle

```python
fruits = np.array(["apple", "orange", "banana", "coconut"])

rng.shuffle(fruits)
print(fruits)

print(rng.choice(fruits, size=3))
```

---

# Structured Arrays

```python
dtype = [('name', 'S10'), ('year', int), ('cgpa', float)]

vals = [('Hrithik', 2009, 8.5),
        ('Ajay',    2008, 8.7),
        ('Pankaj',  2008, 7.9)]

a = np.array(vals, dtype=dtype)

print(np.sort(a, order='name'))
```

---

# Image Processing Example

```python
from skimage import io
import matplotlib.pyplot as plt

img = io.imread("image.jpg")

print(img.shape)

plt.imshow(img)
plt.imshow(img[:, ::-1])       # flip image
plt.imshow(img[50:150, 150:280])  # crop
plt.imshow(img[::30, ::30])   # downsample
```

---

# Summary

- NumPy is used for fast numerical computation  
- Arrays are more efficient than lists  
- Supports vectorized operations  
- Used heavily in data science and machine learning  
