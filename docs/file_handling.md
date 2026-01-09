
# 🗂️ Python File Handling Cheatsheet

Master the essentials of working with files in Python — reading, writing, managing, and handling exceptions.

---

## 📖 1. Opening Files

Use the built-in `open()` function.

```python
file = open("example.txt", "r")  # Modes: r, w, a, x, b, t
content = file.read()
file.close()
```

### Common Modes

| Mode | Description |
|------|--------------|
| `r`  | Read (default) |
| `w`  | Write (overwrites file) |
| `a`  | Append |
| `x`  | Create (fails if file exists) |
| `b`  | Binary mode |
| `t`  | Text mode (default) |
| `r+` | Read and write |

---

## 🧠 2. Using `with` (Context Manager)

Automatically handles closing files — the **best practice**.

```python
with open("data.txt", "r") as file:
    data = file.read()
print("File closed:", file.closed)
```

---

## ✍️ 3. Writing to Files

```python
with open("notes.txt", "w") as f:
    f.write("First line\n")
    f.write("Second line\n")
```

> 💡 Using `w` overwrites the file; use `a` to append.

---

## 📜 4. Reading Files

```python
with open("notes.txt", "r") as f:
    print(f.read())        # Entire file
    f.seek(0)
    print(f.readline())    # One line
    f.seek(0)
    print(f.readlines())   # List of lines
```

---

## 🧩 5. Working with Binary Files

```python
with open("image.png", "rb") as f:
    bytes_data = f.read()
```

To write binary data:

```python
with open("copy.png", "wb") as f:
    f.write(bytes_data)
```

---

## 🔄 6. Checking File Existence

```python
import os

if os.path.exists("notes.txt"):
    print("File exists")
else:
    print("File not found")
```

Or use `pathlib` (modern and preferred):

```python
from pathlib import Path

path = Path("notes.txt")
if path.exists():
    print("File exists")
```

---

## 🗑️ 7. Deleting and Renaming Files

```python
import os

os.rename("old_name.txt", "new_name.txt")
os.remove("unnecessary.txt")
```

Or with `pathlib`:

```python
path = Path("old.txt")
path.rename("new.txt")
path.unlink()  # Deletes the file
```

---

## 📂 8. Directory Handling

```python
os.mkdir("my_folder")
os.rmdir("my_folder")
os.listdir(".")  # List files in current directory
```

`pathlib` version:

```python
p = Path("my_folder")
p.mkdir(exist_ok=True)
for file in p.iterdir():
    print(file)
```

---

## ⚠️ 9. Handling File Exceptions

```python
try:
    with open("data.txt") as f:
        print(f.read())
except FileNotFoundError:
    print("File does not exist!")
except PermissionError:
    print("Permission denied!")
```

---

## 🧰 10. Reading/Writing CSV and JSON

### CSV
```python
import csv

# Writing
with open("data.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Alice", 30])

# Reading
with open("data.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

### JSON
```python
import json

data = {"name": "Bob", "age": 25}

with open("data.json", "w") as f:
    json.dump(data, f)

with open("data.json", "r") as f:
    loaded = json.load(f)
    print(loaded)
```

---

## 🧼 11. Tips & Best Practices

Always use `with open()` for safety  
Use `pathlib` over `os` when possible  
Validate file paths before reading/writing  
Close files explicitly if not using `with`  
ßHandle exceptions for robust code  


---

**© Python Cheatsheet — File Handling Section**
