# Error Handling in Python

Errors are problems that occur in a program and stop its normal execution.

Python provides mechanisms to detect and handle errors so that programs can continue running without crashing.

Errors in Python generally fall into two categories:

- **Syntax Errors** (detected before execution)
- **Exceptions / Runtime Errors** (occur during program execution)

---

# Syntax Error

A **syntax error** occurs when Python cannot understand the code because it is written incorrectly.

Example:

```python
print("hello world"
```

Output:

```
SyntaxError: incomplete input
```

Explanation:

- Python indicates the error location with an arrow (`^`).
- This usually happens when something is missing, such as a closing parenthesis or quotation mark.

---

# TypeError

A **TypeError** occurs when an operation is performed on incompatible data types.

Example:

```python
2 + "hello"
```

Output:

```
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

Explanation:

- Python cannot add an integer and a string together.

---

# NameError

A **NameError** occurs when trying to use a variable that has not been defined.

Example:

```python
x
```

Output:

```
NameError: name 'x' is not defined
```

Explanation:

- The variable `x` has not been assigned any value.

---

# IndexError

An **IndexError** occurs when trying to access an index that does not exist in a list.

Example:

```python
my_list = [1, 2, 3]

my_list[3]
```

Output:

```
IndexError: list index out of range
```

Explanation:

- List indices start from `0`.
- The valid indices here are `0`, `1`, and `2`.

---

# KeyError

A **KeyError** occurs when trying to access a dictionary key that does not exist.

Example:

```python
d1 = {"k1": "v1"}

d1["k2"]
```

Output:

```
KeyError: 'k2'
```

Explanation:

- The key `"k2"` does not exist in the dictionary.

---

# ValueError

A **ValueError** occurs when a function receives the correct type of argument but an invalid value.

Example:

```python
int("hello")
```

Output:

```
ValueError: invalid literal for int() with base 10: 'hello'
```

Explanation:

- Python cannot convert the string `"hello"` into an integer.

---

# Handling Errors with try and except

Python allows handling errors using the `try` and `except` blocks.

## Example 1

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("You are trying to divide by zero")
```

---

## Example 2

```python
try:
    x = int("hello")
except ValueError:
    print("You are trying to convert a string into an integer")
```

---

# How Error Handling Works

- **try** → Contains code that might cause an error  
- **except** → Executes when an exception occurs in the try block  

It is recommended to catch **specific exceptions** rather than using a general `except:` block.

Catching specific exceptions helps avoid hiding unexpected bugs.

---

# Summary

In this section we learned:

- Syntax errors
- TypeError
- NameError
- IndexError
- KeyError
- ValueError
- Using `try` and `except` for error handling
