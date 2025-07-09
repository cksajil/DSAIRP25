# Coding Best Practices
# Python Coding Best Practices:

## Overview

- **Objective:** Learn and apply best practices to write clean, maintainable, and professional Python code.


[![Python Coding Best Practices](https://img.youtube.com/vi/TDbo1mLpjOM/0.jpg)](https://youtu.be/TDbo1mLpjOM)




## 🧱 1. Code Structure and Formatting

### ✅ Follow PEP8

- Use 4 spaces for indentation  
- Keep lines ≤ 79 characters  
- Use blank lines to separate functions/classes  
- Use spaces around operators  

### Example

```python
# Bad
def add(a,b):return a+b

# Good
def add(a: int, b: int) -> int:
    return a + b
```

### File Paths using OS Library

```python
# Bad
file_path = "C:\\Downloads\\data.txt"

# Good
from os.path import join
file_path = join("C", "Downloads", "data.txt")
```

### 🧰 Tools

- `black`: automatic code formatting  
- `flake8`: style guide enforcement  

---

## 🧩 2. Functions and Modular Code

### ✨ Best Practices

- Functions should do **one thing only**  
- Keep them short (<= 50 lines is a good rule of thumb)  
- Use meaningful names  
- Use type hints  

### Example

```python
# Bad
def calc(x, y, z):
    return (x + y) / z

# Good
def average(a: float, b: float, divisor: float = 2.0) -> float:
    return (a + b) / divisor
```

### Organizing Code

Structure your project like:

```
myproject/
│
├── main.py
├── utils/
│   └── file_helpers.py
├── models/
│   └── user.py
└── tests/
    └── test_file_helpers.py
```

---

## 3. Writing Pythonic Code

### 💡 Use Idiomatic Python

- Use list comprehensions  
- Use built-in functions  
- Prefer `enumerate()` over `range(len())`  

### Examples

```python
# Not Pythonic
squares = []
for i in range(10):
    squares.append(i * i)

# Pythonic
squares = [i * i for i in range(10)]
```

### Unpacking

```python
# Better unpacking
a, b = b, a
```

---

##  4. Error Handling and Exceptions

### Best Practices

- Use exceptions instead of returning error codes  
- Catch specific exceptions  
- Avoid bare `except:` clauses  
- Use custom exceptions for clarity  

### Example

```python
# Bad
try:
    result = 10 / x
except:
    print("Error")

# Good
try:
    result = 10 / x
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### Custom Exceptions

```python
class InvalidInputError(Exception):
    pass

def process(data):
    if not isinstance(data, list):
        raise InvalidInputError("Expected a list")
```

---

##  5. Code Documentation and Comments

### ✍️ Comments

- Explain **why**, not **what**  
- Keep them updated  

```python
# Bad
i = 0  # initialize i

# Good
i = 0  # index counter for iterating over students
```

### Docstrings (PEP257)

```python
def greet(name: str) -> str:
    """
    Returns a greeting string.

    Args:
        name (str): Name of the person

    Returns:
        str: Greeting message
    """
    return f"Hello, {name}!"
```

---

## 🧪 6. Testing and Debugging

### ✅ Testing

- Use `unittest`, `pytest`  
- Write tests for every function  
- Use descriptive test names  

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
```

### 🐞 Debugging Tips

- Use `print()` or `logging` during development  
- Use `pdb` for interactive debugging  

```python
import pdb; pdb.set_trace()
```

---

## 🗂️ 7. Version Control and Final Review

### 🧬 Use Git

- Initialize with `git init`  
- Use `.gitignore`  
- Write meaningful commit messages  

### Example Commit Message

```
feat: add helper function for email validation
```

### 🌐 Good `.gitignore` for Python

```
__pycache__/
*.pyc
.env
*.log
```

---

## 📚 Resources

- [PEP8 Style Guide](https://peps.python.org/pep-0008/)  
- [Real Python](https://realpython.com)  
- [Black](https://github.com/psf/black)  
- [Pytest](https://docs.pytest.org/)  

---

## Wrap-Up

- Write clean, readable, modular code  
- Use tools to automate formatting and testing  
- Follow community conventions  
- Write for humans first, machines second  

Happy Coding! 🎉

