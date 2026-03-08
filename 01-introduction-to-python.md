# Introduction to Python

Python is a high-level programming language known for its simple and readable syntax.  
It is widely used for web development, data science, automation, machine learning, and many other applications.

---

# Hello World Program

The first program most beginners write is the **Hello World** program.

```python
print("Hello World")
```

### Explanation

- `print()` is a built-in Python function used to display output.
- `"Hello World"` is a **string**, which is a sequence of characters.

---

# Data Types in Python

Python supports different types of data.

Common basic data types include:

### Integer

Whole numbers.

```python
x = 10
```

Examples:

```
-2, -1, 0, 1, 2
```

---

### Float

Numbers with decimal points.

```python
price = 10.5
```

Examples:

```
0.1, 3.14, -2.5
```

---

### String

Text data enclosed in quotes.

```python
name = "Python"
```

Examples:

```
"a"
"hello"
"123"
```

---

# Variables

Variables are symbolic names used to store data values.

Example:

```python
virat = 60
rohit = 30
rahul = 10
```

You can access a variable by writing its name:

```python
virat
```

You can also perform operations:

```python
virat + rohit + rahul
```

---

# Variable Naming Rules

Variable names cannot start with a number.

❌ Invalid:

```python
1x = 2
```

✔ Valid:

```python
x1 = 2
age = 21
```

---

# Multiple Variables

Python allows assigning multiple variables in one line.

```python
x, y, z = 1, 2, 3
```

Example usage:

```python
a = x + y + z
print(a)
```

---

# Taking Input in Python

The `input()` function allows users to enter data.

```python
name = input("Enter your name: ")
print(name)
```

Note:  
`input()` returns the value as a **string**.

---

# Input with Data Type Conversion

To convert input into numbers:

### Integer Input

```python
age = int(input("Enter your age: "))
print(age)
```

### Float Input

```python
price = float(input("Enter the price: "))
print(price)
```

---

# Multiple Inputs

You can take multiple inputs in one line.

```python
first_name, last_name = input("Enter your first and last name: ").split()

print(f"First name = {first_name}")
print(f"Last name = {last_name}")
```

---

# Summary

In this section we covered:

- Python introduction
- Hello World program
- Data types
- Variables
- Variable rules
- Input handling
