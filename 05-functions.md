# Functions in Python

A **function** is a reusable block of code that performs a specific task.  
Functions help organize code, reduce repetition, and make programs easier to read and maintain.

---

# Why Use Functions?

Functions help us:

- Reuse code
- Organize programs into smaller parts
- Improve readability
- Reduce code duplication

Instead of writing the same logic multiple times, we can define a function once and call it whenever needed.

---

# Defining a Function

In Python, functions are created using the `def` keyword.

```python
def greet():
    print("Hello, welcome to Python")
```

To execute the function, it must be called.

```python
greet()
```

Output:

```
Hello, welcome to Python
```

---

# Function with Parameters

Functions can accept **parameters**, which allow us to pass information to the function.

```python
def greet(name):
    print("Hello", name)
```

Calling the function:

```python
greet("Harshith")
```

Output:

```
Hello Harshith
```

Here, `name` acts as a parameter that receives the value passed to the function.

---

# Function with Multiple Parameters

A function can accept multiple parameters.

```python
def add(a, b):
    print(a + b)
```

Calling the function:

```python
add(5, 3)
```

Output:

```
8
```

---

# Returning Values from a Function

Functions can return values using the `return` statement.

```python
def add(a, b):
    return a + b
```

Calling the function:

```python
result = add(5, 3)
print(result)
```

Output:

```
8
```

The `return` statement sends the result back to the place where the function was called.

---

# Example: Checking Even or Odd

```python
def check_number(num):
    if num % 2 == 0:
        return "Even"
    else:
        return "Odd"
```

Calling the function:

```python
print(check_number(10))
```

Output:

```
Even
```

---

# Summary

In this section we learned:

- What functions are
- Why functions are useful
- How to define functions
- Passing parameters to functions
- Using multiple parameters
- Returning values from functions
