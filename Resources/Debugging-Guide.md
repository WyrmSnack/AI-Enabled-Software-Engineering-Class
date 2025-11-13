# Debugging Guide

Comprehensive guide to debugging AI-generated code and common issues.

## Common AI-Generated Code Bugs

### 1. Off-by-One Errors
**Problem**: Loops or array access off by one index.

**Example**:
```python
# AI might generate:
for i in range(len(items)):
    process(items[i + 1])  # Wrong: goes out of bounds
```

**Fix**:
```python
for i in range(len(items)):
    process(items[i])  # Correct
```

### 2. Missing Error Handling
**Problem**: AI generates code without error handling.

**Example**:
```python
# AI might generate:
def get_user(user_id):
    return db.query(User).filter(User.id == user_id).first()
```

**Fix**:
```python
def get_user(user_id):
    user = db.query(User).filter(User.id == user_id).first()
    if not user:
        raise HTTPException(status_code=404, detail="User not found")
    return user
```

### 3. Incorrect Type Assumptions
**Problem**: AI assumes wrong data types.

**Example**:
```python
# AI might generate:
def calculate_total(items):
    return sum(items)  # Assumes items is numeric
```

**Fix**:
```python
def calculate_total(items):
    if not items:
        return 0
    return sum(item.price for item in items)
```

### 4. Missing Validation
**Problem**: No input validation.

**Example**:
```python
# AI might generate:
def create_user(email, password):
    user = User(email=email, password=password)
    db.add(user)
    db.commit()
```

**Fix**:
```python
def create_user(email: str, password: str):
    if not email or "@" not in email:
        raise ValueError("Invalid email")
    if len(password) < 8:
        raise ValueError("Password too short")
    # ... rest of code
```

### 5. Race Conditions
**Problem**: Concurrent access issues.

**Example**:
```python
# AI might generate:
def increment_counter():
    counter = get_counter()
    counter.value += 1
    save_counter(counter)
```

**Fix**:
```python
def increment_counter():
    with db.begin():
        counter = db.query(Counter).with_for_update().first()
        counter.value += 1
        db.commit()
```

---

## Debugging AI Suggestions

### Step 1: Understand the Code
1. Read the AI-generated code carefully
2. Trace through the logic
3. Identify assumptions
4. Check edge cases

### Step 2: Test the Code
1. Write tests for happy path
2. Test edge cases
3. Test error cases
4. Run the code

### Step 3: Identify Issues
1. Check for common bugs (see above)
2. Verify error handling
3. Check input validation
4. Review security

### Step 4: Fix and Verify
1. Fix identified issues
2. Re-test
3. Verify with AI if needed

---

## Debugging Tools and Techniques

### Python Debugging

#### Print Debugging
```python
def process_data(data):
    print(f"Input data: {data}")  # Debug print
    result = complex_calculation(data)
    print(f"Result: {result}")  # Debug print
    return result
```

#### Python Debugger (pdb)
```python
import pdb

def process_data(data):
    pdb.set_trace()  # Breakpoint
    result = complex_calculation(data)
    return result
```

#### Logging
```python
import logging

logger = logging.getLogger(__name__)

def process_data(data):
    logger.debug(f"Processing data: {data}")
    try:
        result = complex_calculation(data)
        logger.info(f"Success: {result}")
        return result
    except Exception as e:
        logger.error(f"Error: {e}", exc_info=True)
        raise
```

### React Debugging

#### Console Logging
```jsx
function Component() {
  const [data, setData] = useState(null);
  
  useEffect(() => {
    console.log('Fetching data...');
    fetchData().then(result => {
      console.log('Data received:', result);
      setData(result);
    });
  }, []);
  
  return <div>{data}</div>;
}
```

#### React DevTools
- Install React DevTools browser extension
- Inspect component state
- View props
- Check component tree

#### Debugger Statement
```jsx
function processData(data) {
  debugger;  // Breakpoint in browser
  const result = complexCalculation(data);
  return result;
}
```

---

## Debugging Strategies

### 1. Divide and Conquer
- Isolate the problem
- Test components separately
- Narrow down the issue

### 2. Check Assumptions
- Verify input data
- Check expected outputs
- Validate assumptions

### 3. Use Print Statements
- Log key variables
- Track execution flow
- Identify where it fails

### 4. Read Error Messages
- Read full error messages
- Check stack traces
- Look for line numbers

### 5. Simplify
- Remove complexity
- Test with simple data
- Build up gradually

---

## Common Issues and Solutions

### Issue: "Undefined is not a function"
**Cause**: Calling method on undefined object

**Solution**:
```javascript
// Check if object exists
if (user && user.getName) {
  user.getName();
}
```

### Issue: "Cannot read property of null"
**Cause**: Accessing property on null

**Solution**:
```javascript
// Use optional chaining
const name = user?.profile?.name;
```

### Issue: Database Connection Errors
**Cause**: Database not running or wrong credentials

**Solution**:
```python
# Check connection
try:
    db.connect()
except Exception as e:
    logger.error(f"Database connection failed: {e}")
    # Check DATABASE_URL, credentials, etc.
```

### Issue: CORS Errors
**Cause**: Frontend and backend on different origins

**Solution**:
```python
# Add CORS middleware
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:5173"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)
```

---

## Using AI for Debugging

### Ask AI to Explain Code
```
Explain what this code does and identify potential bugs:

[Code snippet]
```

### Ask AI to Fix Bugs
```
This code has a bug. Fix it:

[Code with bug]

Error: [Error message]
```

### Ask AI to Review Code
```
Review this code for:
- Bugs
- Security issues
- Performance problems
- Best practices

[Code]
```

---

## Debugging Checklist

### Before Debugging
- [ ] Understand what the code should do
- [ ] Reproduce the issue
- [ ] Check error messages
- [ ] Review recent changes

### During Debugging
- [ ] Add logging/print statements
- [ ] Test with simple inputs
- [ ] Isolate the problem
- [ ] Check assumptions

### After Fixing
- [ ] Test the fix
- [ ] Test edge cases
- [ ] Remove debug code
- [ ] Document the fix

---

## Best Practices

### Do's
✅ Test code after AI generation
✅ Review AI suggestions carefully
✅ Add error handling
✅ Validate inputs
✅ Use logging
✅ Write tests
✅ Check edge cases

### Don'ts
❌ Trust AI code blindly
❌ Skip testing
❌ Ignore error messages
❌ Leave debug code in production
❌ Skip code review

---

## Resources

- [Python Debugging](https://docs.python.org/3/library/pdb.html)
- [React Debugging](https://react.dev/learn/react-developer-tools)
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/)
- [VS Code Debugging](https://code.visualstudio.com/docs/editor/debugging)

