
# ⚙️ Python Functions Cheatsheet

A comprehensive guide to defining, calling, and mastering functions in Python.

---

## 🧩 1. Defining a Function

Use `def` followed by the function name and parentheses.

```python
def greet():
    print("Hello, world!")

greet()
```

---

## 🧠 2. Function Parameters

### Positional Parameters
```python
def add(a, b):
    return a + b

print(add(3, 5))  # Output: 8
```

### Default Parameters
```python
def power(base, exp=2):
    return base ** exp

print(power(4))    # 16
print(power(4, 3)) # 64
```

### Keyword Arguments
```python
def describe_pet(animal, name):
    print(f"{name} is a {animal}.")

describe_pet(name="Buddy", animal="dog")
```

### Arbitrary Arguments
```python
def add_all(*args):
    return sum(args)

print(add_all(1, 2, 3, 4))  # 10
```

### Arbitrary Keyword Arguments
```python
def display_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=30)
```

---

## 🪄 3. Return Values

```python
def square(x):
    return x * x

result = square(5)
print(result)
```

Return multiple values:
```python
def stats(a, b):
    return a + b, a * b

sum_, product = stats(3, 4)
print(sum_, product)
```

---

## 🧰 4. Docstrings

Document your function using triple quotes.

```python
def greet(name):
    '''Return a greeting for the given name.'''
    return f"Hello, {name}!"
```

View docstring:
```python
help(greet)
print(greet.__doc__)
```

---

## ⚙️ 5. Lambda (Anonymous) Functions

Small one-liners for simple operations.

```python
square = lambda x: x ** 2
print(square(4))  # 16
```

Example with `map()` and `filter()`:
```python
nums = [1, 2, 3, 4, 5]
squared = list(map(lambda n: n ** 2, nums))
even = list(filter(lambda n: n % 2 == 0, nums))
```

---

## 🧮 6. Recursion

A function calling itself.

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

> ⚠️ Always include a base case to prevent infinite recursion.

---

## 🧱 7. Nested Functions

Functions inside other functions.

```python
def outer():
    msg = "Hello"

    def inner():
        print(msg)

    inner()

outer()
```

---

## 🔒 8. Closures

Inner functions that remember the variables from their enclosing scope.

```python
def make_multiplier(x):
    def multiply(y):
        return x * y
    return multiply

double = make_multiplier(2)
print(double(5))  # 10
```

---

## 🧬 9. Decorators

Functions that modify the behavior of other functions.

```python
def logger(func):
    def wrapper(*args, **kwargs):
        print(f"Running {func.__name__}...")
        return func(*args, **kwargs)
    return wrapper

@logger
def greet():
    print("Hello!")

greet()
```

---

## 🧾 10. Type Hints

Add clarity and support static type checking.

```python
def add(a: int, b: int) -> int:
    return a + b
```

Use `mypy` to check types:
```bash
mypy your_script.py
```

---

## 🧩 11. Higher-Order Functions

Functions that take or return other functions.

```python
def apply(func, value):
    return func(value)

print(apply(lambda x: x * 2, 10))
```

---

## ⚙️ 12. Built-in Functions Overview

| Category | Examples |
|-----------|-----------|
| Math | `abs()`, `round()`, `sum()`, `min()`, `max()` |
| Iterables | `len()`, `sorted()`, `zip()`, `enumerate()` |
| Type Conversion | `int()`, `float()`, `str()`, `list()` |
| Logic | `any()`, `all()`, `bool()` |

---

## 🧠 13. Best Practices

Use descriptive names for clarity  
Keep functions small and focused  
Add docstrings and type hints  
Avoid side effects (modifying globals)  
Return values instead of printing when possible  


---

**© Python Cheatsheet — Functions Section**
