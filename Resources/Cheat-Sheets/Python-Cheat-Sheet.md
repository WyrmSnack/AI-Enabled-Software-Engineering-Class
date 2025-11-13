# Python Cheat Sheet

Quick reference for Python programming.

## Variables
```python
name = "John"
age = 25
price = 19.99
is_active = True
```

## Lists
```python
fruits = ["apple", "banana", "orange"]
fruits.append("grape")
fruits[0]  # "apple"
len(fruits)  # 4
```

## Dictionaries
```python
person = {"name": "John", "age": 25}
person["name"]  # "John"
person.get("email", "N/A")  # "N/A"
```

## Functions
```python
def greet(name):
    return f"Hello, {name}!"

def calculate_total(items, tax=0.10):
    return sum(items) * (1 + tax)
```

## Control Flow
```python
if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")

for item in items:
    print(item)

while condition:
    do_something()
```

## List Comprehensions
```python
squares = [x**2 for x in range(10)]
evens = [x for x in range(10) if x % 2 == 0]
```

## Error Handling
```python
try:
    result = risky_operation()
except ValueError as e:
    print(f"Error: {e}")
finally:
    cleanup()
```

## Classes
```python
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email
    
    def greet(self):
        return f"Hello, {self.name}!"
```

## Type Hints
```python
def add(a: int, b: int) -> int:
    return a + b
```

