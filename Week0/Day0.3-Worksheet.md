# Day 0.3 Worksheet: Python Fundamentals

**Estimated Time**: 1–2 hours  
**Focus**: Writing and running simple Python scripts; understanding basic programming concepts

---

## Learning Objectives

By the end of this session, you will be able to:
- Write and run simple Python scripts
- Understand variables, data types, and control flow
- Use an IDE with AI assistance (optional)
- Create a Python program that prints your name and current date

---

## Pre-Activity: Setup Check

**Verify Python Installation**:

Open a terminal/command prompt and run:
```bash
python --version
# OR
python3 --version
```

**Your Python version**: _________________________ (should be 3.11 or higher)

**If Python is not installed**:
- Windows: Download from [python.org](https://www.python.org/downloads/)
- Mac: Usually pre-installed, or use Homebrew: `brew install python3`
- Linux: `sudo apt-get install python3` (Ubuntu/Debian)

---

## Activity 1: Install and Configure Your IDE

**Choose one**:
- [ ] **VS Code** — [Download here](https://code.visualstudio.com/)
- [ ] **Cursor** — [Download here](https://cursor.com/)

**After installation**:
1. Install the Python extension (VS Code) or ensure Python support is enabled (Cursor)
2. (Optional) Install GitHub Copilot extension if you have access
3. Open a new folder for your Week 0 work

**IDE installed?** [ ] Yes  
**Python extension installed?** [ ] Yes  
**Copilot enabled?** [ ] Yes [ ] No (optional)

---

## Activity 2: Python Tutorial — Sections 1–4

**Resource**: [Python.org Tutorial](https://docs.python.org/3/tutorial/index.html#tutorial-index)

**Focus on these sections**:
1. **Whetting Your Appetite** — Overview
2. **Using the Python Interpreter** — Running Python
3. **An Informal Introduction to Python** — Basic syntax
4. **More Control Flow Tools** — if/else, loops

**As you read, practice each concept in your IDE**:

### Section 1: Basic Operations

**Try in Python**:
```python
# Variables
name = "Your Name"
age = 25
height = 5.9

# Print statements
print("Hello, World!")
print(f"My name is {name} and I am {age} years old")
```

**Run this code and note the output**:
_______________________________________________________________________

### Section 2: Data Types

**Fill in the table**:

| Code Example | Data Type | What It Represents |
|--------------|-----------|-------------------|
| `name = "Alice"` | | |
| `age = 30` | | |
| `price = 19.99` | | |
| `is_student = True` | | |
| `grades = [85, 90, 78]` | | |

### Section 3: Control Flow

**Write code for each scenario**:

**If/Else Example**:
```python
# Write code that checks if a number is positive, negative, or zero
number = 5  # Try different values

# Your code here:

```

**For Loop Example**:
```python
# Write a loop that prints numbers 1 through 5
# Your code here:

```

**While Loop Example**:
```python
# Write a while loop that counts from 1 to 3
# Your code here:

```

---

## Activity 3: Functions

**Learn about functions** (continue reading the tutorial or try this):

**Example**:
```python
def greet(name):
    """This function greets a person by name."""
    return f"Hello, {name}! Welcome to Python."

# Call the function
message = greet("Alice")
print(message)
```

**Your turn**: Write a function that:
- Takes two numbers as parameters
- Returns their sum

**Your code**:
```python

```

---

## Activity 4: AI-Assisted Practice (Optional)

**If you have Copilot Chat or Cursor AI enabled**:

1. **Generate a "Hello World" script**:
   - Prompt: "Write a Python script that prints 'Hello, World!'"
   - Copy the generated code and run it

2. **Generate a loop**:
   - Prompt: "Write a Python loop that prints numbers 1 through 5"
   - Run the code

3. **Reflect**: How did the AI help? Was the code correct?

**Your reflection**:
_______________________________________________________________________

---

## Activity 5: Main Deliverable — Name and Date Script

**Task**: Create a Python file called `main.py` that:
1. Prints your name
2. Prints the current date

**Starter code**:
```python
# Import the datetime module
from datetime import datetime

# Your code here to print your name
# Your code here to print the current date
```

**Hints**:
- Use `print()` for output
- Use `datetime.now()` to get the current date/time
- Format the date nicely (e.g., "January 15, 2024")

**Your complete code**:
```python

```

**Test your code**:
- Run it: `python main.py` or `python3 main.py`
- Verify it prints your name and the current date

**Output when you run it**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 6: Practice Exercises

**Exercise 1: Variables and Types**
```python
# Create variables for:
# - Your favorite color (string)
# - Your age (integer)
# - Your height in meters (float)
# - Whether you like Python (boolean)

# Print all of them with descriptive messages
```

**Your code**:
```python

```

**Exercise 2: Conditional Logic**
```python
# Write code that:
# - Asks for a number (or set a variable)
# - Checks if it's greater than 10
# - Prints "Large number" if true, "Small number" if false
```

**Your code**:
```python

```

**Exercise 3: Lists and Loops**
```python
# Create a list of 3 programming languages
# Loop through the list and print each one with "I want to learn: [language]"
```

**Your code**:
```python

```

---

## Deliverable Checklist

- [ ] Python 3.11+ installed and verified
- [ ] IDE (VS Code or Cursor) installed with Python extension
- [ ] Completed Python tutorial sections 1–4
- [ ] Practiced basic operations, data types, and control flow
- [ ] Created `main.py` that prints name and current date
- [ ] Tested `main.py` and verified it works
- [ ] Completed practice exercises
- [ ] (Optional) Tried AI-assisted code generation
- [ ] Uploaded `main.py` to your GitHub Week0 folder

---

## Common Python Concepts Reference

**Variables**:
```python
name = "Alice"        # String
age = 30              # Integer
price = 19.99         # Float
is_active = True      # Boolean
```

**Control Flow**:
```python
# If/Else
if age >= 18:
    print("Adult")
else:
    print("Minor")

# For loop
for i in range(5):
    print(i)

# While loop
count = 0
while count < 3:
    print(count)
    count += 1
```

**Functions**:
```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8
```

---

## Reflection Questions

1. **What Python concept was easiest to understand?**
   _______________________________________________________________________

2. **What Python concept was most challenging?**
   _______________________________________________________________________

3. **How did using an IDE help (or not help) your learning?**
   _______________________________________________________________________

4. **If you used AI assistance, how did it change your experience?**
   _______________________________________________________________________

---

## Additional Resources (Optional)

- [Python.org Official Tutorial](https://docs.python.org/3/tutorial/)
- [Real Python: Python Basics](https://realpython.com/python-basics/)
- [Python for Everybody (Coursera)](https://www.coursera.org/specializations/python)

---

## Troubleshooting

**Common Issues**:

- **"Python not found"**: Make sure Python is in your PATH, or use `python3` instead of `python`
- **Syntax errors**: Check for missing colons (`:`) after if/for/while/def statements
- **Indentation errors**: Python uses indentation (spaces/tabs) to define code blocks

**Error you encountered?** Note it here:
_______________________________________________________________________
_______________________________________________________________________

---

## Next Steps

Tomorrow (Day 0.4), you'll learn about databases and SQL. No special setup needed—we'll use online tools!

