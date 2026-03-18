# Advanced Function Concepts in Python

Python functions support several advanced features that make programs more flexible and powerful.

These include:

- `pass` keyword
- Recursion
- `*args` and `**kwargs`
- Assigning functions to variables
- Passing functions as arguments
- Storing functions in data structures
- Lambda functions
- Using `map()` and `filter()`

---

# The `pass` Keyword

The `pass` keyword is used as a placeholder when a statement is syntactically required but no action needs to be performed.

It is useful when writing incomplete code.

```python
x = 10

if x > 5:
    pass
else:
    print("taki taki")
```

Here, the `pass` statement does nothing but allows the program to run without errors.

---

# Recursion

Recursion is a technique where a function calls itself.

It is useful for solving problems that can be broken into smaller identical problems.

Common use cases include:

- Mathematical computations
- Tree traversal
- Divide and conquer algorithms

## Example: Factorial Using Recursion

```python
def factorial(n):
    if n == 0:       # Base case
        return 1
    else:            # Recursive case
        return n * factorial(n - 1)

print(factorial(5))
```

Output:

```
120
```

---

# Types of Recursion

### Tail Recursion

The recursive call is the **last operation** performed by the function.

Some programming languages can optimize tail recursion to reduce memory usage.

### Non-Tail Recursion

The function performs additional operations **after the recursive call returns**, so it cannot be optimized like a loop.

---

# *args and **kwargs

Python allows functions to accept a variable number of arguments.

## *args

`*args` allows passing multiple positional arguments.

```python
def fun(*args):
    return sum(args)

print(fun(5, 10, 15))
```

Output:

```
30
```

---

## **kwargs

`**kwargs` allows passing multiple keyword arguments.

```python
def fun(**kwargs):
    for key, value in kwargs.items():
        print(key, value)

fun(a=1, b=2, c=3)
```

Output:

```
a 1
b 2
c 3
```

---

# Assigning Functions to Variables

In Python, functions are **first-class objects**, which means they can be assigned to variables.

```python
def msg(name):
    return f"Hello, {name}!"

f = msg

print(f("Emma"))
```

Output:

```
Hello, Emma!
```

---

# Passing Functions as Arguments

Functions can also be passed as arguments to other functions.

```python
def msg(name):
    return f"Hello, {name}!"

def fun1(fun2, name):
    return fun2(name)

print(fun1(msg, "Alex"))
```

Output:

```
Hello, Alex!
```

---

# Storing Functions in Data Structures

Functions can be stored inside data structures like lists or dictionaries.

```python
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

d = {
    "add": add,
    "subtract": subtract
}

print(d["add"](5, 3))
print(d["subtract"](5, 3))
```

Output:

```
8
2
```

---

# Lambda Functions

Lambda functions are **small anonymous functions**.

Characteristics:

- They do not have a name
- They contain only one expression
- The result is returned automatically

Example:

```python

def square(n):
  return n ** 2

def cube(c):
  return c ** 3

def tlist (nlist,trlist):
  tr0 = trlist(nlist[0])
  tr1 = trlist(nlist[1])
  return tr0,tr1

test = [1,2]
tlist([1,3],square)

#instead of all these the lambda can simply
square = lambda x: x ** 2

print(square(5))
```

Output:

```
25
```

---

# Using `map()` with Lambda

The `map()` function applies a function to each element in an iterable.

```python
agapi = [1,2,3,4,5,6,7,8,9]

list(map(lambda x: x**2, agapi))
```

Output:

```
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```

---

# Using `filter()` with Lambda

The `filter()` function selects elements from an iterable based on a condition.

```python
agapi = [1,2,3,4,5,6,7,8,9]

list(filter(lambda x: x % 2 != 0, agapi))
```

Output:

```
[1, 3, 5, 7, 9]
```

---

# Summary

In this section we learned:

- Using the `pass` keyword
- Recursion and factorial example
- Tail vs non-tail recursion
- Using `*args` and `**kwargs`
- Assigning functions to variables
- Passing functions as arguments
- Storing functions in data structures
- Lambda functions
- Using `map()` and `filter()`
