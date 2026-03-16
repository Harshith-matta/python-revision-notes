# Working with Strings in Python

A **string** is a sequence of characters used to represent text in Python.

Strings are immutable, meaning their values cannot be changed after creation.

---

# Creating Strings

Strings can be created using **single quotes**, **double quotes**, or **triple quotes**.

```python
single = 'hello'
double = "hello"

multiline = '''
this is line 1
this is line 2
this is line 3
'''

print(single)
print(double)
print(multiline)
```

Output:

```
hello
hello

this is line 1
this is line 2
this is line 3
```

---

# Accessing Characters

Characters in a string can be accessed using **index positions**.

```python
single = "hello"

print(single[1])
```

Output:

```
e
```

Indexing starts from **0**.

---

# String Slicing

Slicing allows extracting a portion of a string.

```python
single = "hello"

print(single[:4])
```

Output:

```
hell
```

---

# Negative Indexing

Negative indexing accesses characters from the end of the string.

```python
double = "hello"

print(double[-1])
```

Output:

```
o
```

---

# String Concatenation

Concatenation means **joining two or more strings together**.

```python
text = "hello" + " " + "world" + "!"
print(text)
```

Output:

```
hello world!
```

---

# String Repetition

Strings can be repeated using the `*` operator.

```python
print("ha" * 3 + "!")
```

Output:

```
hahaha!
```

---

# String Length

The `len()` function returns the number of characters in a string.

```python
x = "hello"
print(len(x))
```

Output:

```
5
```

---

# Checking Substrings

A substring is a smaller string inside a larger string.

The `in` keyword checks whether a substring exists.

```python
x = "hello world"

print("hello" in x)
print(" " in x)
```

Output:

```
True
True
```

---

# String Methods

Python provides several built-in string methods.

```python
name = "harshith"

print(name.upper())
print(name.replace("harshith", "siddhu"))
print(name.split())
```

---

# String Formatting (f-strings)

F-strings allow embedding variables directly into strings.

```python
name = "harshith"

print(f"hello {name}")
```

Output:

```
hello harshith
```

---

# Summary

In this section we learned:

- How to create strings
- Accessing characters using indexing
- String slicing
- Negative indexing
- Concatenation and repetition
- Checking substrings
- Useful string methods
- String formatting with f-strings
