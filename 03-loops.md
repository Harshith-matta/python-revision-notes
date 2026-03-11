# Loops in Python

Loops allow a program to execute a block of code repeatedly.  
They are useful when you want to perform the same action multiple times without writing the same code again.

Python mainly provides two types of loops:

- `for` loop
- `while` loop

---

# For Loop

The `for` loop is used to iterate over a sequence such as a list, string, or range of numbers.

## Example

```python
for i in range(5):
    print(i)
```

### Output

```
0
1
2
3
4
```

### Explanation

- `range(5)` generates numbers from `0` to `4`
- The loop runs once for each value
- `i` takes the value from the sequence during each iteration

---

# Loop Through a String

A `for` loop can also iterate through characters in a string.

```python
word = "python"

for letter in word:
    print(letter)
```

### Output

```
p
y
t
h
o
n
```

---

# While Loop

The `while` loop executes a block of code as long as a condition remains `True`.

## Example

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

### Explanation

- The loop starts with `count = 0`
- Each iteration increases `count` by `1`
- The loop stops when the condition becomes `False`

---

# Break Statement

The `break` statement stops the loop immediately.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### Output

```
0
1
2
3
4
```

The loop stops when `i` becomes `5`.

---

# Continue Statement

The `continue` statement skips the current iteration and moves to the next one.

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

### Output

```
0
1
3
4
```

The value `2` is skipped.

---

## Example: Sum of numbers using a loop

```python
total = 0

for i in range(1, 6):
    total += i

print(total)
```


## Summary

Loops are used to repeat actions in a program.

In this section we learned:

- What loops are
- How `for` loops work
- How `while` loops work
- Using `break` to exit loops
- Using `continue` to skip iterations
