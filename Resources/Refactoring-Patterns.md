# Refactoring Patterns

Common refactoring scenarios and how to use AI to assist.

## What is Refactoring?

Refactoring is improving code structure without changing functionality.

**Key Principles**:
- Behavior stays the same
- Tests should still pass
- Small, incremental changes
- One refactoring at a time

---

## Common Refactoring Scenarios

### 1. Extract Function/Method

**Problem**: Long function doing multiple things

**Before**:
```python
def process_order(order):
    # Calculate subtotal
    subtotal = 0
    for item in order.items:
        subtotal += item.price * item.quantity
    
    # Calculate tax
    tax = subtotal * 0.10
    
    # Calculate shipping
    if subtotal > 100:
        shipping = 0
    else:
        shipping = 10
    
    # Calculate total
    total = subtotal + tax + shipping
    
    # Apply discount
    if order.customer.is_premium:
        total *= 0.90
    
    return total
```

**After**:
```python
def calculate_subtotal(items):
    return sum(item.price * item.quantity for item in items)

def calculate_tax(subtotal, rate=0.10):
    return subtotal * rate

def calculate_shipping(subtotal):
    return 0 if subtotal > 100 else 10

def apply_discount(total, customer):
    return total * 0.90 if customer.is_premium else total

def process_order(order):
    subtotal = calculate_subtotal(order.items)
    tax = calculate_tax(subtotal)
    shipping = calculate_shipping(subtotal)
    total = subtotal + tax + shipping
    return apply_discount(total, order.customer)
```

**AI Prompt**:
```
Refactor this function by extracting smaller functions:

[Function code]

Each extracted function should have a single responsibility.
```

---

### 2. Rename Variable/Function

**Problem**: Unclear or misleading names

**Before**:
```python
def calc(x, y):
    return x * y * 1.1
```

**After**:
```python
def calculate_total_with_tax(price, quantity):
    return price * quantity * 1.1
```

**AI Prompt**:
```
Rename variables and functions in this code to be more descriptive:

[Code]

Use clear, descriptive names that explain purpose.
```

---

### 3. Replace Magic Numbers

**Problem**: Hardcoded values without meaning

**Before**:
```python
if age >= 18:
    discount = price * 0.10
```

**After**:
```python
LEGAL_ADULT_AGE = 18
STANDARD_DISCOUNT_RATE = 0.10

if age >= LEGAL_ADULT_AGE:
    discount = price * STANDARD_DISCOUNT_RATE
```

**AI Prompt**:
```
Replace magic numbers in this code with named constants:

[Code]

Extract all hardcoded values to constants with descriptive names.
```

---

### 4. Simplify Conditionals

**Problem**: Complex if-else chains

**Before**:
```python
def get_status(user):
    if user.is_active:
        if user.has_subscription:
            return "premium"
        else:
            return "active"
    else:
        return "inactive"
```

**After**:
```python
def get_status(user):
    if not user.is_active:
        return "inactive"
    if user.has_subscription:
        return "premium"
    return "active"
```

**AI Prompt**:
```
Simplify this conditional logic:

[Code]

Use early returns and guard clauses where appropriate.
```

---

### 5. Extract Class

**Problem**: Functions that should be grouped

**Before**:
```python
def calculate_user_score(user_id):
    # Complex calculation
    pass

def get_user_rank(user_id):
    # Uses calculate_user_score
    pass

def update_user_score(user_id, points):
    # Updates score
    pass
```

**After**:
```python
class UserScoring:
    def __init__(self, user_id):
        self.user_id = user_id
    
    def calculate_score(self):
        # Complex calculation
        pass
    
    def get_rank(self):
        # Uses calculate_score
        pass
    
    def update_score(self, points):
        # Updates score
        pass
```

**AI Prompt**:
```
Refactor these related functions into a class:

[Functions]

Group related functionality together.
```

---

### 6. Remove Duplication

**Problem**: Repeated code

**Before**:
```python
def create_user(name, email):
    if not name or not email:
        raise ValueError("Name and email required")
    # ... create user

def update_user(user_id, name, email):
    if not name or not email:
        raise ValueError("Name and email required")
    # ... update user
```

**After**:
```python
def validate_user_data(name, email):
    if not name or not email:
        raise ValueError("Name and email required")

def create_user(name, email):
    validate_user_data(name, email)
    # ... create user

def update_user(user_id, name, email):
    validate_user_data(name, email)
    # ... update user
```

**AI Prompt**:
```
Remove code duplication in this code:

[Code]

Extract common logic into reusable functions.
```

---

## When to Refactor

### Good Times to Refactor
- ✅ Before adding new features
- ✅ When fixing bugs
- ✅ During code review
- ✅ When code is hard to understand
- ✅ When tests are hard to write

### Not Good Times
- ❌ Right before a deadline
- ❌ When code works and won't change
- ❌ Without tests
- ❌ When you don't understand the code

---

## Refactoring with AI

### Step 1: Identify What to Refactor
**Prompt**:
```
Identify refactoring opportunities in this code:

[Code]

Look for:
- Long functions
- Code duplication
- Magic numbers
- Complex conditionals
- Poor naming
```

### Step 2: Plan the Refactoring
**Prompt**:
```
Create a refactoring plan for this code:

[Code]

Break down into small, safe steps.
```

### Step 3: Execute Refactoring
**Prompt**:
```
Refactor this code to [specific improvement]:

[Code]

Maintain existing functionality. Show step-by-step changes.
```

### Step 4: Verify
- Run tests
- Check functionality
- Review changes
- Ensure no regressions

---

## Refactoring Checklist

### Before Refactoring
- [ ] Code is under version control
- [ ] Tests exist and pass
- [ ] Understand what code does
- [ ] Have a clear goal

### During Refactoring
- [ ] Make small changes
- [ ] Run tests frequently
- [ ] Commit often
- [ ] One refactoring at a time

### After Refactoring
- [ ] All tests pass
- [ ] Functionality unchanged
- [ ] Code is cleaner
- [ ] Documentation updated

---

## Common Refactoring Patterns

### Extract Method
- Break long methods into smaller ones
- Each method has single responsibility

### Extract Variable
- Replace complex expressions with variables
- Improves readability

### Replace Conditional with Polymorphism
- Use inheritance/classes instead of if-else
- More extensible

### Move Method
- Move method to appropriate class
- Better organization

### Replace Parameter with Method
- Remove parameters by calculating them
- Simpler interface

---

## Best Practices

### Do's
✅ Refactor in small steps
✅ Keep tests passing
✅ Commit frequently
✅ Understand before changing
✅ One thing at a time

### Don'ts
❌ Refactor without tests
❌ Change behavior while refactoring
❌ Refactor everything at once
❌ Skip code review
❌ Refactor code you don't understand

---

## Resources

- [Refactoring.com](https://refactoring.com/)
- [Martin Fowler's Refactoring Catalog](https://refactoring.com/catalog/)
- [Refactoring Guru](https://refactoring.guru/)

