
# ⚡ Python Shortcuts & One-Liners Cheatsheet

Boost your productivity with these **Python shortcuts, tricks, and one-liners** for cleaner, faster coding.

---

## 🧩 1. Variable Swapping

Swap two variables without a temporary one.

```python
a, b = b, a
```

---

## 🧮 2. Multiple Variable Assignment

Assign multiple values at once.

```python
x, y, z = 1, 2, 3
```

Unpack lists or tuples easily:

```python
a, b, *rest = [10, 20, 30, 40, 50]
```

---

## 🧠 3. Inline Conditional (Ternary Operator)

```python
age = 20
status = "Adult" if age >= 18 else "Minor"
```

---

## 📜 4. List Comprehensions

Compact way to create lists.

```python
squares = [x**2 for x in range(10)]
evens = [x for x in range(20) if x % 2 == 0]
```

Nested version:

```python
matrix = [[i * j for j in range(3)] for i in range(3)]
```

---

## 🧰 5. Dictionary & Set Comprehensions

```python
squares = {x: x**2 for x in range(5)}
unique_letters = {char for char in "hello"}
```

---

## 🧾 6. Enumerate

Get index and value together when looping.

```python
for index, value in enumerate(["a", "b", "c"]):
    print(index, value)
```

---

## 🪄 7. Zip

Combine iterables.

```python
names = ["Alice", "Bob", "Charlie"]
scores = [85, 90, 95]

for name, score in zip(names, scores):
    print(name, score)
```

Unzip with `*`:
```python
zipped = list(zip(names, scores))
names, scores = zip(*zipped)
```

---

## ⚙️ 8. Inline Functions (Lambdas)

Short anonymous functions.

```python
square = lambda x: x ** 2
add = lambda a, b: a + b
```

Use with `map()` or `filter()`:

```python
nums = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, nums))
even = list(filter(lambda x: x % 2 == 0, nums))
```

---

## 🧮 9. Join & Split Strings

```python
words = ["Python", "is", "awesome"]
sentence = " ".join(words)

chars = "A-B-C".split("-")
```

---

## 🧱 10. Reversing Collections

```python
nums = [1, 2, 3, 4]
print(nums[::-1])
print(list(reversed(nums)))
```

Reverse a string:

```python
text = "Python"
print(text[::-1])  # nohtyP
```

---

## 🧠 11. Get Unique Items (Remove Duplicates)

```python
unique = list(set([1, 2, 2, 3, 3, 4]))
```

Preserve order (Python 3.7+):

```python
unique_ordered = list(dict.fromkeys([1, 2, 2, 3, 3, 4]))
```

---

## 🧾 12. Counting Elements Quickly

```python
from collections import Counter

nums = [1, 2, 2, 3, 3, 3]
count = Counter(nums)
print(count.most_common(1))  # [(3, 3)]
```

---

## 🔄 13. Flatten a List of Lists

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [num for row in matrix for num in row]
```

---

## 🧰 14. Sort with Custom Keys

```python
words = ["apple", "banana", "pear"]
sorted_words = sorted(words, key=len)
```

Reverse sort:

```python
nums = [3, 1, 4, 2]
sorted_desc = sorted(nums, reverse=True)
```

---

## 🧩 15. Inline File Reading

```python
lines = [line.strip() for line in open("file.txt")]
```

---

## ⚙️ 16. Using `any()` and `all()`

```python
nums = [1, 2, 3, 0]
print(any(nums))  # True if any item is truthy
print(all(nums))  # True if all items are truthy
```

---

## 🧮 17. Chained Comparisons

```python
x = 5
if 1 < x < 10:
    print("In range!")
```

---

## 🔢 18. FizzBuzz One-Liner

```python
[("Fizz"*(i%3==0) + "Buzz"*(i%5==0) or i) for i in range(1, 21)]
```

---

## 🧩 19. Merging Dictionaries

```python
a = {"x": 1, "y": 2}
b = {"y": 3, "z": 4}
merged = {**a, **b}
```

---

## 🪄 20. Debugging Shortcut

Quickly inspect variables.

```python
x = 42
print(f"{x=}")  # Prints: x=42
```

---

## 🧮 21. List Repetition

```python
zeros = [0] * 5  # [0, 0, 0, 0, 0]
```

---

## 🧰 22. Compact Conditional Loops

```python
nums = [x for x in range(10) if x % 2 == 0]
```

---

## 🧠 23. Dictionary to List Conversion

```python
data = {"a": 1, "b": 2, "c": 3}
items = list(data.items())
keys = list(data.keys())
values = list(data.values())
```

---

## 🪄 24. Find Index Safely

```python
try:
    index = my_list.index("target")
except ValueError:
    index = -1
```

---

## ⚡ 25. Simple Timer

```python
import time
start = time.time()

# your code here

print(f"Execution time: {time.time() - start:.2f}s")
```

---

**✅ Bonus Tip:** Use `python -i script.py` to open an interactive shell *after* running your script — perfect for debugging!

---

**🔗 Related Topics:**
- [Functions](functions.md)
- [Data Structures](data_structures.md)

---

**© Python Cheatsheet — Shortcuts Section**
