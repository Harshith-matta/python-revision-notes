# Python Modules: math and random

In Python, modules are like libraries.  
Just like you go to a library to find books, we use modules to access useful functions.

We use the `import` keyword to use a module.

```python
import math
```

---

# Math Module

The `math` module provides mathematical functions and constants.

---

## Mathematical Constants

```python
print(math.pi)
print(math.e)
print(math.tau)
print(math.inf)
print(-math.inf)
print(math.nan)
```

### Note

- `pi` → used in circle calculations  
- `e` → used in exponential growth (AI, ML, finance)  
- `inf` → represents infinity  
- `nan` → used when result is undefined  

---

## Number Functions

```python
print(math.ceil(4.2))
print(math.floor(4.8))
print(math.fabs(-10))
print(math.factorial(5))
print(math.gcd(12, 18))
print(math.isclose(0.1 + 0.2, 0.3))
print(math.prod([1, 2, 3, 4]))
```

### Note

- `ceil()` → rounds up  
- `floor()` → rounds down  
- `fabs()` → absolute value  
- `factorial()` → used in probability  
- `gcd()` → simplifies fractions  
- `prod()` → multiplies all elements in a list  

---

## Floating Point Precision

```python
print(0.1 + 0.2)
print(math.isclose(0.1 + 0.2, 0.3))
```

Output:

```
0.30000000000000004
True
```

### Note

Floating-point calculations produce tiny errors ("math dust").  
Use `math.isclose()` to compare values safely.

---

## Power, Logs and Roots

```python
print(math.sqrt(16))
print(math.pow(2, 3))
print(math.exp(2))
print(math.log(10))
print(math.log(10, 2))
print(math.log2(8))
print(math.log10(100))
```

---

## Trigonometry

```python
print(math.sin(math.radians(90)))
print(math.cos(0))
print(math.tan(math.radians(45)))
```

---

## Inverse Trigonometry

```python
print(math.asin(1))
print(math.acos(1))
print(math.atan(1))
print(math.atan2(1, 1))
```

---

## Angle Conversion

```python
print(math.degrees(math.pi))
print(math.radians(180))
```

---

## Hyperbolic Functions

```python
print(math.sinh(1))
print(math.cosh(1))
print(math.tanh(1))
```

---

## Special Functions

```python
print(math.erf(1))
print(math.erfc(1))
print(math.gamma(5))
print(math.trunc(4.6))
```

### Note

- `gamma(n)` → works like factorial (n-1)!  
- `erf()` → probability (bell curve)  

---

## Distance and Geometry

```python
print(math.hypot(3, 4))
print(math.dist([1, 2], [4, 6]))
```

### Note

- `hypot()` → Pythagoras theorem  
- `dist()` → distance between two points  

---

# Random Module

The `random` module is used to generate random values.

```python
import random
```

---

## Random Numbers

```python
print(random.random())
print(random.randint(1000, 9999))
```

### Note

- `randint(1000, 9999)` → used for OTP generation  

---

## Random Choice

```python
lst = ["black", "white", "red", "green", "pink", "blue"]
print(random.choice(lst))
```

---

## Shuffling Data

```python
random.shuffle(lst)
print(lst)
```

### Note

Used in games, card shuffling, random ordering.

---

## Multiple Random Values

```python
for i in range(5):
    print(random.random())
```

---

## Random Sampling

```python
print(random.sample(range(1000, 9999), 10))
```

### Note

Returns unique random values (no repetition).

---

# Summary

- `math` module → mathematical operations  
- `random` module → randomness and simulations  
- Useful in real-world tasks like:
  - OTP generation  
  - simulations  
  - games  
  - probability  
