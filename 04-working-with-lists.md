# Working with Lists in Python

A **list** is a built-in Python data structure used to store multiple values in a single variable.

Lists are:

- Ordered
- Mutable (can be modified)
- Allow duplicate elements

Example:

```python
numbers = [1, 2, 3, 4, 5]
```

---

# Creating a List

A list is created using square brackets `[]`.

```python
fruits = ["apple", "banana", "mango"]
print(fruits)
```

Output:

```
['apple', 'banana', 'mango']
```

---

# Accessing Elements

List elements can be accessed using **index positions**.

Indexing starts from **0**.

```python
fruits = ["apple", "banana", "mango"]

print(fruits[0])
print(fruits[1])
```

Output:

```
apple
banana
```

---

# Negative Indexing

Python also supports **negative indexing**, which accesses elements from the end of the list.

```python
fruits = ["apple", "banana", "mango"]

print(fruits[-1])
```

Output:

```
mango
```

---

# Modifying List Elements

Lists are mutable, meaning their values can be changed.

```python
fruits = ["apple", "banana", "mango"]

fruits[1] = "orange"
print(fruits)
```

Output:

```
['apple', 'orange', 'mango']
```

---

# Adding Elements to a List

## append()

Adds an element to the end of the list.

```python
numbers = [1, 2, 3]

numbers.append(4)
print(numbers)
```

Output:

```
[1, 2, 3, 4]
```

---

## insert()

Adds an element at a specific index.

```python
numbers = [1, 2, 3]

numbers.insert(1, 10)
print(numbers)
```

Output:

```
[1, 10, 2, 3]
```

---

# Removing Elements

## remove()

Removes a specific value from the list.

```python
numbers = [1, 2, 3, 4]

numbers.remove(3)
print(numbers)
```

Output:

```
[1, 2, 4]
```

---

## pop()

Removes an element using its index.

```python
numbers = [1, 2, 3, 4]

numbers.pop(1)
print(numbers)
```

Output:

```
[1, 3, 4]
```

---

# List Length

The `len()` function returns the number of elements in a list.

```python
numbers = [1, 2, 3, 4, 5]

print(len(numbers))
```

Output:

```
5
```

---

# Looping Through a List

Lists can be iterated using a `for` loop.

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)
```

Output:

```
apple
banana
mango
```

---

# Summary

In this section we learned:

- What lists are
- How to create lists
- Accessing elements using indexing
- Modifying list values
- Adding elements (`append`, `insert`)
- Removing elements (`remove`, `pop`)
- Finding list length
- Iterating through a list
