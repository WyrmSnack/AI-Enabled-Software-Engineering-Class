# Code Smell Detection

How to identify code smells and use AI to help detect them.

## What are Code Smells?

Code smells are indicators that code might need refactoring. They're not bugs, but signs of potential problems.

**Key Point**: Code smells suggest issues, but don't always require fixing. Context matters.

---

## Common Code Smells

### 1. Long Method/Function

**Smell**: Function is too long (usually > 20-30 lines)

**Why It's Bad**:
- Hard to understand
- Hard to test
- Hard to maintain
- Does too many things

**Detection**:
```python
# Smell: 50+ line function
def process_order(order):
    # 50 lines of code doing multiple things
    pass
```

**Fix**: Extract smaller functions

**AI Prompt**:
```
This function is too long. Break it into smaller functions:

[Function code]

Each function should have a single responsibility.
```

---

### 2. Large Class

**Smell**: Class has too many responsibilities

**Why It's Bad**:
- Violates single responsibility
- Hard to understand
- Hard to test
- Hard to maintain

**Detection**:
- Class has 10+ methods
- Methods don't relate to each other
- Class does multiple things

**Fix**: Split into multiple classes

**AI Prompt**:
```
This class is too large. Suggest how to split it:

[Class code]

Identify distinct responsibilities and suggest separate classes.
```

---

### 3. Duplicate Code

**Smell**: Same code appears in multiple places

**Why It's Bad**:
- Changes need to be made in multiple places
- Easy to miss updates
- Inconsistent behavior

**Detection**:
- Similar code blocks
- Copy-paste patterns
- Repeated logic

**Fix**: Extract to function/class

**AI Prompt**:
```
Find duplicate code in this codebase:

[Code snippets]

Suggest how to extract common functionality.
```

---

### 4. Long Parameter List

**Smell**: Function has too many parameters (usually > 5)

**Why It's Bad**:
- Hard to remember order
- Easy to pass wrong values
- Hard to test
- Indicates missing abstraction

**Detection**:
```python
def create_user(name, email, phone, address, city, state, zip, country, dob, gender):
    # Too many parameters
    pass
```

**Fix**: Use object/class for parameters

**AI Prompt**:
```
This function has too many parameters. Refactor to use a parameter object:

[Function code]

Create a class or dataclass for the parameters.
```

---

### 5. Magic Numbers

**Smell**: Hardcoded numbers without meaning

**Why It's Bad**:
- Unclear what number means
- Hard to change
- Easy to make mistakes

**Detection**:
```python
if age >= 18:  # What does 18 mean?
    discount = price * 0.10  # What does 0.10 mean?
```

**Fix**: Use named constants

**AI Prompt**:
```
Replace magic numbers with named constants:

[Code]

Extract all hardcoded numbers to constants with descriptive names.
```

---

### 6. Feature Envy

**Smell**: Method uses another object's data more than its own

**Why It's Bad**:
- Method might belong in other class
- Tight coupling
- Poor encapsulation

**Detection**:
```python
class Order:
    def calculate_total(self):
        # Uses customer data more than order data
        if self.customer.is_premium:
            return self.subtotal * 0.90
        return self.subtotal
```

**Fix**: Move method or extract logic

**AI Prompt**:
```
This method seems to belong in another class. Suggest refactoring:

[Code]

Identify where the method should actually live.
```

---

### 7. Data Clumps

**Smell**: Groups of data always used together

**Why It's Bad**:
- Should be an object
- Passed around together
- Indicates missing abstraction

**Detection**:
```python
def create_user(name, email, phone):
    # name, email, phone always together
    pass

def update_user(name, email, phone):
    # Same group again
    pass
```

**Fix**: Create object/class

**AI Prompt**:
```
These parameters are always used together. Extract to a class:

[Function signatures]

Create a class to represent this data group.
```

---

### 8. Primitive Obsession

**Smell**: Using primitives instead of objects

**Why It's Bad**:
- Loses meaning
- No validation
- No behavior

**Detection**:
```python
def calculate_price(price_str, currency_str):
    # Using strings instead of objects
    pass
```

**Fix**: Create value objects

**AI Prompt**:
```
Replace primitive types with value objects:

[Code]

Create classes for Price, Currency, etc.
```

---

### 9. Switch Statements

**Smell**: Long if-else or switch chains

**Why It's Bad**:
- Hard to extend
- Violates open/closed principle
- Often indicates missing polymorphism

**Detection**:
```python
def get_status(user_type):
    if user_type == "admin":
        return "full_access"
    elif user_type == "user":
        return "limited_access"
    elif user_type == "guest":
        return "read_only"
    # ... many more
```

**Fix**: Use polymorphism or dictionary

**AI Prompt**:
```
Replace this switch statement with polymorphism:

[Code]

Use classes or a strategy pattern.
```

---

### 10. Comments

**Smell**: Too many comments or comments explaining "what"

**Why It's Bad**:
- Code should be self-explanatory
- Comments can become outdated
- Indicates unclear code

**Detection**:
```python
# Calculate the total
total = price * quantity  # Multiply price by quantity
# Apply discount
total = total * 0.90  # Apply 10% discount
```

**Fix**: Write self-documenting code

**AI Prompt**:
```
Remove unnecessary comments and make code self-documenting:

[Code]

Code should explain itself. Only keep comments that explain "why".
```

---

## Using AI to Detect Code Smells

### General Detection
**Prompt**:
```
Identify code smells in this code:

[Code]

Check for:
- Long methods
- Duplicate code
- Magic numbers
- Complex conditionals
- Poor naming
- Other common smells
```

### Specific Smell Detection
**Prompt**:
```
Check this code for [specific smell]:

[Code]

Identify instances and suggest fixes.
```

### Refactoring Suggestions
**Prompt**:
```
This code has code smells. Suggest refactoring:

[Code]

Provide specific refactoring suggestions with examples.
```

---

## Code Smell Checklist

### Structure
- [ ] Long methods (> 30 lines)
- [ ] Large classes (> 10 methods)
- [ ] Long parameter lists (> 5 params)
- [ ] Deep nesting (> 3 levels)

### Duplication
- [ ] Duplicate code
- [ ] Similar code blocks
- [ ] Copy-paste patterns

### Naming
- [ ] Unclear names
- [ ] Magic numbers
- [ ] Abbreviations
- [ ] Inconsistent naming

### Complexity
- [ ] Complex conditionals
- [ ] Switch statements
- [ ] Too many responsibilities
- [ ] High cyclomatic complexity

### Design
- [ ] Feature envy
- [ ] Data clumps
- [ ] Primitive obsession
- [ ] God objects

---

## Best Practices

### Do's
✅ Use code smells as indicators
✅ Consider context before fixing
✅ Refactor incrementally
✅ Use AI to help identify smells
✅ Fix smells that cause problems

### Don'ts
❌ Fix every smell blindly
❌ Refactor without tests
❌ Ignore context
❌ Over-engineer solutions
❌ Fix smells in legacy code without care

---

## Tools for Detection

### Static Analysis
- **pylint**: Python code analysis
- **flake8**: Style guide enforcement
- **SonarQube**: Code quality platform
- **CodeClimate**: Automated code review

### AI Tools
- **GitHub Copilot**: Can suggest refactorings
- **ChatGPT/Claude**: Can analyze code for smells
- **Cursor**: AI-assisted code review

---

## Resources

- [Refactoring Guru - Code Smells](https://refactoring.guru/smells)
- [Martin Fowler - Code Smells](https://martinfowler.com/bliki/CodeSmell.html)
- [SourceMaking - Code Smells](https://sourcemaking.com/refactoring/smells)

