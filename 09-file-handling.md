# File Handling in Python

File handling allows us to create, read, write, and delete files in Python.

Python provides built-in functions to work with files efficiently.

---

# Creating a File

A file can be created using the `open()` function with write mode (`'w'`).

```python
with open('new_file.txt', 'w') as f:
    f.write('Hello, this is a new text file created using open() function.')

print("File created successfully.")
```

Output:

```
File created successfully.
```

Explanation:

- `'w'` mode creates a new file (or overwrites an existing file)
- `with` ensures the file is automatically closed after use

---

# Opening Files

General syntax:

```python
open(filename, mode)
```

### Parameters:

- **filename** → name of the file (`.txt`, `.json`, etc.)
- **mode** → operation to perform

### Common Modes:

- `'r'` → Read
- `'w'` → Write (overwrite)
- `'a'` → Append

---

# Appending Data to a File

Append mode (`'a'`) adds new content without removing existing data.

```python
with open("new_file.txt", "a") as f:
    f.write('\nhelloooooooooo')
```

---

# Reading a File

```python
with open("new_file.txt", "r") as f:
    print(f.read())
```

Output:

```
helloooooooooo
```

---

# Removing a Specific Line

```python
line_to_remove = "helloooooooooo"

with open("new_file.txt", 'r') as f:
    lines = f.readlines()

with open("new_file.txt", 'w') as f:
    for line in lines:
        if line.strip('\n') != line_to_remove:
            f.write(line)
```

---

# Adding New Content Again

```python
with open("new_file.txt", "a") as f:
    f.write('\nSo finally added a new line to the file')
```

---

# Clearing File Content

To delete all content inside a file:

```python
with open('new_file.txt', 'r+') as f:
    f.seek(0)
    f.truncate()
```

Explanation:

- `seek(0)` moves the cursor to the beginning
- `truncate()` removes all content

---

# Deleting a File

Python provides the `os` module to delete files.

```python
import os

file_path = 'new_file.txt'

if os.path.exists(file_path):
    os.remove(file_path)
    print(f"{file_path} has been deleted.")
else:
    print(f"{file_path} not found.")
```

---

# Summary

In this section we learned:

- Creating files using `open()`
- File modes (`r`, `w`, `a`)
- Reading and writing files
- Appending data
- Removing specific lines
- Clearing file content
- Deleting files using `os`
