# Tuples and Sets in Python

Python provides different data structures to store collections of data.

- **List** → `[]`
- **Dictionary** → `{key: value}`
- **Tuple** → `()`
- **Set** → `{}`

---

# Tuples in Python

A **tuple** is an ordered, immutable collection of elements.

---

# Creating a Tuple

```python
my_tuple = (1, 2, 3)
print(my_tuple)
```

Output:

```
(1, 2, 3)
```

---

## Creating Tuple from String

```python
s = tuple("siddhu")
print(s)
```

Output:

```
('s', 'i', 'd', 'd', 'h', 'u')
```

---

## Tuple with Mixed Data Types

```python
tup = (5, 7.3, "siddhu", True, [1, 2, 3], {"apple": "dog"})
print(tup)
```

---

# Accessing Tuple Elements

```python
my_tuple = (1, 2, 3)
print(my_tuple[2])
```

Output:

```
3
```

---

# Slicing Tuples

```python
tup = tuple("starboy")

print(tup[0])
print(tup[1:4])
print(tup[:3])
```

Output:

```
s
('t', 'a', 'r')
('s', 't', 'a')
```

---

# Tuple Operations

```python
tp1 = (1, 2, 3)
tp2 = ("a", "b", "c")

print(tp1 + tp2)
print(tp1 * 2)
```

---

## Repeating Elements

```python
tp3 = (1,)
print(tp3 * 10)
```

Output:

```
(1, 1, 1, 1, 1, 1, 1, 1, 1, 1)
```

---

# Deleting a Tuple

```python
weeknd = ("starboy",)
del weeknd
```

---

# Tuple Unpacking

Tuple unpacking allows assigning values to variables in a single line.

```python
tp1 = (1, 2, 3)

a, b, c = tp1
print(b)
```

Output:

```
2
```

---

## Extended Unpacking

```python
tpp = (1, 2, 3, 4, 5, 6, 7)

a, *b, c = tpp

print(a)
print(b)
print(c)
```

Output:

```
1
[2, 3, 4, 5, 6]
7
```

---

# List vs Tuple (Simple Idea)

- **List** → like a train (can add/remove compartments)
- **Tuple** → like a bus (fixed, cannot change)

- Lists use more memory
- Tuples use less memory

---

# Sets in Python

A **set** is an unordered collection of unique elements.

---

# Creating a Set

```python
lst = [1, 1, 2]

print(set(lst))
```

Output:

```
{1, 2}
```

---

# Accessing Set Elements

Sets are unordered and unindexed, so you cannot access elements using indexing.

```python
s = {"weeknd", "For", "starboy"}

for i in s:
    print(i, end=" ")
```

---

# Checking Membership

```python
print("weeknd" in s)
```

Output:

```
True
```

---

# Removing Elements

```python
s.remove("weeknd")
print(s)
```

---

## Using discard()

```python
s.discard("starboy")
print(s)
```

- `remove()` → raises error if element not found  
- `discard()` → does not raise error  

---

# Clearing a Set

```python
s = {1, 2, 3, 4, 5}

s.clear()
print(s)
```

Output:

```
set()
```

---

# Frozenset

A **frozenset** is an immutable version of a set.

```python
s = frozenset([1, 2, 3, 4, 5])
print(s)
```

---

# Typecasting to Set

```python
d = {1: "one", 2: "two", 3: "three"}

s1 = set(d)
print(s1)
```

Output:

```
{1, 2, 3}
```

---

# Set Operations

```python
s1 = {1, 2, 3}
s2 = {2, 3, 4}

print(s1.union(s2))
print(s1.intersection(s2))
print(s2.difference(s1))
```

Output:

```
{1, 2, 3, 4}
{2, 3}
{4}
```

---

# Summary

In this section we learned:

- Tuples and their properties
- Tuple creation, slicing, and unpacking
- Tuple vs List differences
- Sets and uniqueness
- Removing elements from sets
- Frozenset
- Set operations (union, intersection, difference)
