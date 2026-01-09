
# 🧱 Python Data Structures Cheatsheet

Master Python’s core data structures — lists, tuples, sets, and dictionaries — with practical examples.

---

## 📋 1. Lists

Mutable, ordered collections of items.

```python
fruits = ["apple", "banana", "cherry"]
```

### Common Operations
```python
fruits.append("orange")     # Add
fruits.remove("banana")     # Remove
fruits.insert(1, "kiwi")    # Insert at index
fruits.pop()                # Remove last item
fruits.sort()               # Sort list
fruits.reverse()            # Reverse order
print(len(fruits))          # Length
```

### List Slicing
```python
numbers = [0, 1, 2, 3, 4, 5]
print(numbers[1:4])   # [1, 2, 3]
print(numbers[::-1])  # Reverse
```

### List Comprehension
```python
squares = [x**2 for x in range(5)]
even = [n for n in range(10) if n % 2 == 0]
```

---

## 🪄 2. Tuples

Immutable and ordered collections — great for fixed data.

```python
point = (3, 4)
print(point[0])  # 3
```

### Tuple Unpacking
```python
x, y = point
print(x, y)
```

### One-Element Tuple
```python
single = (5,)
print(type(single))  # <class 'tuple'>
```

> ⚠️ Without the comma → `(5)` is just an `int`.

---

## 🧩 3. Sets

Unordered, mutable collections of **unique** items.

```python
nums = {1, 2, 3, 3, 2}
print(nums)  # {1, 2, 3}
```

### Set Operations
```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)  # Union → {1, 2, 3, 4, 5}
print(a & b)  # Intersection → {3}
print(a - b)  # Difference → {1, 2}
print(a ^ b)  # Symmetric difference → {1, 2, 4, 5}
```

### Useful Methods
```python
s = {10, 20, 30}
s.add(40)
s.remove(20)
s.discard(50)  # Safe remove (no error)
```

---

## 🧰 4. Dictionaries

Key-value pairs, mutable and unordered (since Python 3.7, they maintain insertion order).

```python
person = {"name": "Alice", "age": 25}
```

### Access and Modify
```python
print(person["name"])
person["age"] = 26
person["city"] = "New York"
```

### Dictionary Methods
```python
print(person.keys())      # dict_keys(['name', 'age', 'city'])
print(person.values())    # dict_values(['Alice', 26, 'New York'])
print(person.items())     # dict_items([('name', 'Alice'), ('age', 26), ('city', 'New York')])
```

### Looping
```python
for key, value in person.items():
    print(f"{key}: {value}")
```

### Dictionary Comprehension
```python
squares = {x: x**2 for x in range(5)}
```

---

## 🧮 5. Nested Data Structures

You can combine structures:

```python
users = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
]
print(users[0]["name"])  # Alice
```

---

## 🪣 6. Stacks and Queues (Using Lists or `collections.deque`)

### Stack (LIFO)
```python
stack = [1, 2, 3]
stack.append(4)
stack.pop()  # Removes 4
```

### Queue (FIFO)
```python
from collections import deque

queue = deque(["a", "b", "c"])
queue.append("d")
queue.popleft()  # Removes 'a'
```

---

## 🧮 7. Useful Built-ins

| Function | Description | Example |
|-----------|--------------|----------|
| `len()` | Count items | `len([1,2,3]) → 3` |
| `sum()` | Add numbers | `sum([1,2,3]) → 6` |
| `sorted()` | Return a sorted copy | `sorted({3,1,2}) → [1,2,3]` |
| `min()` / `max()` | Smallest / largest value | `min([3,5,1]) → 1` |
| `all()` | True if all items true | `all([1, True, 3]) → True` |
| `any()` | True if any item true | `any([0, 0, 1]) → True` |

---

## ⚙️ 8. Copying Collections

```python
import copy

a = [1, 2, [3, 4]]
b = a.copy()       # Shallow copy
c = copy.deepcopy(a)  # Deep copy
```

---

## 🧠 9. Type Conversion

```python
tuple([1, 2, 3])        # → (1, 2, 3)
list((1, 2, 3))         # → [1, 2, 3]
set([1, 2, 2, 3])       # → {1, 2, 3}
dict(a=1, b=2)          # → {'a': 1, 'b': 2}
```

---

## ✅ 10. Best Practices

Use lists for ordered data  
Use tuples for fixed data  
Use sets to remove duplicates  
Use dictionaries for key-value mapping  
Use comprehensions for concise creation  

---

**🔗 Related Topics:**
- [Basics](basics.md)
- [Functions](functions.md)
- [File Handling](file_handling.md)

---

**© Python Cheatsheet — Data Structures Section**
