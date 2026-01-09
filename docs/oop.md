
# 🧱 Python Object-Oriented Programming (OOP) Cheatsheet

Everything you need to know about **classes, objects, inheritance, encapsulation, and polymorphism** in Python.

---

## 🧩 1. What is OOP?

OOP (Object-Oriented Programming) organizes code into **objects** that bundle **data** (attributes) and **behavior** (methods).

---

## 🧱 2. Defining a Class

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name}.")

p1 = Person("Alice", 25)
p1.greet()
```

---

## 🧠 3. `__init__` Method

The constructor initializes an object’s attributes when it’s created.

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

car = Car("Tesla", "Model 3")
print(car.brand)  # Tesla
```

---

## 🧍 4. Instance Variables vs Class Variables

```python
class Dog:
    species = "Canine"  # Class variable

    def __init__(self, name):
        self.name = name  # Instance variable

dog1 = Dog("Rex")
dog2 = Dog("Buddy")

print(dog1.species)  # Canine
print(dog1.name)     # Rex
```

---

## ⚙️ 5. Methods

### Instance Method
Operates on an instance (`self` refers to it).

### Class Method
Uses `@classmethod` and the class itself (`cls`).

### Static Method
Uses `@staticmethod` — doesn’t need class or instance.

```python
class Example:
    def instance_method(self):
        return "Called instance method", self

    @classmethod
    def class_method(cls):
        return "Called class method", cls

    @staticmethod
    def static_method():
        return "Called static method"
```

---

## 🧬 6. Inheritance

Derive a new class (child) from another (parent).

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("Some sound")

class Dog(Animal):
    def speak(self):
        print("Woof!")

dog = Dog("Buddy")
dog.speak()
```

### `super()` for Parent Access
```python
class Bird(Animal):
    def __init__(self, name, color):
        super().__init__(name)
        self.color = color
```

---

## 🧱 7. Encapsulation

Control access to data using **private** and **protected** attributes.

```python
class Account:
    def __init__(self, balance):
        self._balance = balance      # Protected
        self.__pin = "1234"          # Private

    def get_balance(self):
        return self._balance

    def _update_balance(self, amount):
        self._balance += amount
```

> Prefix with `_` → “protected” convention (internal use).  
> Prefix with `__` → name mangling (`_ClassName__var`).

---

## 🔄 8. Polymorphism

Different classes share the same interface but implement behavior differently.

```python
class Cat:
    def speak(self): return "Meow"

class Dog:
    def speak(self): return "Woof"

for animal in [Cat(), Dog()]:
    print(animal.speak())
```

---

## 🧰 9. Magic (Dunder) Methods

| Method | Purpose |
|---------|----------|
| `__init__` | Constructor |
| `__str__` | Human-readable string |
| `__repr__` | Debug representation |
| `__len__` | Define length |
| `__add__` | Overload `+` operator |
| `__eq__` | Define equality |
| `__call__` | Make instance callable |

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __repr__(self):
        return f"Vector({self.x}, {self.y})"
```

---

## 🧱 10. Composition (HAS-A Relationship)

Use other classes as attributes.

```python
class Engine:
    def start(self):
        print("Engine starting...")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        self.engine.start()
        print("Car ready!")
```

---

## 🧩 11. Abstract Classes (Interfaces)

Force child classes to implement specific methods.

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2
```

---

## 🧾 12. Property Decorator

Use getters and setters cleanly.

```python
class Employee:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name

    @name.setter
    def name(self, value):
        if not value:
            raise ValueError("Name cannot be empty")
        self._name = value
```

---

## 🧠 13. Multiple Inheritance

```python
class A:
    def greet(self): print("Hello from A")

class B:
    def greet(self): print("Hello from B")

class C(A, B):
    pass

c = C()
c.greet()  # Method Resolution Order (MRO): A → B
```

View MRO:
```python
print(C.mro())
```

---

## ⚙️ 14. Data Classes (Python 3.7+)

Automatically generate boilerplate methods.

```python
from dataclasses import dataclass

@dataclass
class Point:
    x: int
    y: int

p = Point(3, 4)
print(p)  # Point(x=3, y=4)
```

---

## ✅ 15. Best Practices

✅ Use clear naming conventions  
✅ Favor composition over inheritance when possible  
✅ Keep classes small and focused  
✅ Use properties to encapsulate data  
✅ Add `__repr__` for better debugging  

---

**🔗 Related Topics:**
- [Functions](functions.md)

---

**© Python Cheatsheet — OOP Section**
