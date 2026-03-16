# Functions in Python

A **function** is a reusable block of code designed to perform a specific task.

Functions help make programs:

- More organized
- Easier to read
- Reusable
- Easier to maintain

Instead of writing the same code multiple times, we can define a function and call it whenever needed.

---

# Defining a Function

In Python, a function is defined using the `def` keyword.

```python
def greet():
    print("Hello, welcome to Python")
```

This creates a function named `greet`.

To execute the function, we call it:

```python
greet()
```

Output:

```
Hello, welcome to Python
```

---

# Function with Parameters

Functions can accept **parameters**, which allow data to be passed into the function.

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

Here, `name` is a parameter that receives the value provided when the function is called.

---

# Function with Multiple Parameters

A function can accept more than one parameter.

```python
def add(a, b):
    result = a + b
    print(result)
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

The `return` statement sends the result back to where the function was called.

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

# Why Functions Are Important

Functions make programs easier to manage by:

- Reducing code repetition
- Improving readability
- Organizing logic into smaller parts
- Making programs easier to debug

---

# Summary

In this section we learned:

- What functions are
- How to define a function
- Using parameters
- Passing multiple arguments
- Returning values from functions
- Writing simple function examples
