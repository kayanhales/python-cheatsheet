
# 🐍 Python Basics Cheatsheet

A concise reference for Python fundamentals — variables, data types, operators, and control flow.

---

## ⚙️ 1. Python Syntax Overview

```python
# This is a comment
print("Hello, World!")  # Output: Hello, World!
```

### Indentation
Python uses **indentation** to define blocks (no `{}` needed).
```python
if True:
    print("Indented block")
```

---

## 💡 2. Variables

No need to declare types — Python is dynamically typed.

```python
x = 10
name = "Alice"
pi = 3.14
is_active = True
```

Reassigning changes type dynamically:
```python
x = "Now I'm a string!"
```

---

## 🧮 3. Data Types

| Type | Example | Description |
|------|----------|--------------|
| `int` | `42` | Whole numbers |
| `float` | `3.1415` | Decimal numbers |
| `str` | `"Hello"` | Text |
| `bool` | `True`, `False` | Logical values |
| `list` | `[1, 2, 3]` | Ordered, mutable collection |
| `tuple` | `(1, 2, 3)` | Ordered, immutable collection |
| `set` | `{1, 2, 3}` | Unordered, unique values |
| `dict` | `{"a": 1, "b": 2}` | Key-value pairs |

---

## ✍️ 4. Strings

```python
name = "Python"
print(name.lower())
print(name.upper())
print(name[0:3])  # Slicing
print(len(name))
```

### String Formatting
```python
age = 25
print(f"My age is {age}")  # f-string
print("My age is {}".format(age))
```

---

## ➕ 5. Operators

| Type | Operators | Example | Result |
|------|------------|----------|--------|
| Arithmetic | `+`, `-`, `*`, `/`, `//`, `%`, `**` | `5 ** 2` | `25` |
| Comparison | `==`, `!=`, `>`, `<`, `>=`, `<=` | `5 > 3` | `True` |
| Logical | `and`, `or`, `not` | `x > 0 and y < 10` | — |
| Assignment | `=`, `+=`, `-=`, `*=` | `x += 5` | — |
| Membership | `in`, `not in` | `'a' in 'cat'` | `True` |
| Identity | `is`, `is not` | `x is y` | — |

---

## 🔁 6. Conditionals

```python
age = 18

if age >= 18:
    print("Adult")
elif age > 13:
    print("Teenager")
else:
    print("Child")
```

Ternary Expression:
```python
status = "Adult" if age >= 18 else "Minor"
```

---

## 🔄 7. Loops

### For Loop
```python
for i in range(5):
    print(i)
```

### While Loop
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Loop Control Statements
```python
for n in range(10):
    if n == 3:
        continue  # Skip 3
    if n == 8:
        break     # Stop at 8
    print(n)
```

---

## 🧱 8. Data Structures

### Lists
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits[0])  # Access first item
```

### Tuples
```python
point = (3, 4)
print(point[0])
```

### Sets
```python
nums = {1, 2, 3, 3}
print(nums)  # {1, 2, 3}
```

### Dictionaries
```python
person = {"name": "Alice", "age": 25}
print(person["name"])
person["age"] = 26
```

---

## 🧮 9. List Comprehensions

A concise way to create lists.

```python
squares = [x**2 for x in range(5)]
evens = [n for n in range(10) if n % 2 == 0]
```

---

## ⚠️ 10. Exception Handling

```python
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("That's not a number!")
else:
    print("You entered:", num)
finally:
    print("Done!")
```

---

## 🧰 11. Type Conversion

```python
x = 10
print(str(x))  # "10"
print(float(x))  # 10.0
print(int("20"))  # 20
```

---

## 🕒 12. Useful Built-ins

```python
abs(-5)      # 5
round(3.7)   # 4
len("hello") # 5
sum([1,2,3]) # 6
sorted([3,1,2]) # [1,2,3]
```

---

## 🧠 13. Input & Output

```python
name = input("Enter your name: ")
print("Hello,", name)
```

---

## ✅ 14. Best Practices

✅ Use clear, descriptive variable names  
✅ Follow PEP 8 style guide  
✅ Keep indentation consistent (4 spaces)  
✅ Use `with` for file handling  
✅ Comment wisely and write readable code  

---

**🔗 Related Topics:**
- [Functions](functions.md)
- [File Handling](file_handling.md)
- [Data Structures](data_structures.md)

---

**© Python Cheatsheet — Basics Section**
