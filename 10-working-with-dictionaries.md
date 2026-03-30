# Working with Dictionaries in Python

A **dictionary** is a built-in data structure that stores data in **key-value pairs**.

Dictionaries are:

- Unordered (in older Python versions) / insertion-ordered (Python 3.7+)
- Mutable (can be modified)
- Indexed by keys

---

# Creating a Dictionary

A dictionary is created using curly braces `{}`.

```python
student = {
    "name": "siddhu",
    "age": 27,
    "gender": "male",
    "qualifies": False
}

print(student)
```

Output:

```
{'name': 'siddhu', 'age': 27, 'gender': 'male', 'qualifies': False}
```

---

# Accessing and Updating Values

Values can be accessed using keys.

```python
print(student["age"])
```

Output:

```
27
```

Updating values:

```python
student["name"] = "harshith"
student["age"] = 29

print(student)
```

---

# Looping Through a Dictionary

## Accessing Keys

```python
for key in student:
    print(key)
```

---

## Accessing Values

```python
for value in student.values():
    print(value)
```

---

## Accessing Key-Value Pairs

```python
for key, value in student.items():
    print(key, value)
```

---

# Checking if a Key Exists

```python
if "name" in student:
    print("present")
```

---

# Removing Dictionary Items

```python
d = {1: 'weeknd', 2: 'starboy', 3: 'blinding', 'age': 22}
```

## Using `del`

```python
del d["age"]
print(d)
```

---

## Using `pop()`

```python
val = d.pop(1)
print(val)
```

---

## Using `popitem()`

```python
key, val = d.popitem()
print(f"Key: {key}, Value: {val}")
```

---

## Using `clear()`

```python
d.clear()
print(d)
```

Output:

```
{}
```

---

# Nested Dictionaries

A dictionary can contain another dictionary as a value.

```python
d = {
    1: 'sorry',
    2: 'For',
    3: {
        'the': 'Weeknd',
        'starboy': 'To',
        'afterhours': 'music'
    }
}

print(d)
print(d[3])
```

Output:

```
{'the': 'Weeknd', 'starboy': 'To', 'afterhours': 'music'}
```

---

# Summary

In this section we learned:

- Creating dictionaries
- Accessing and updating values
- Looping through dictionaries
- Checking keys
- Removing items (`del`, `pop`, `popitem`, `clear`)
- Nested dictionaries
