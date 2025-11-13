# Week 2, Day 9 Worksheet: Testing & Quality Assurance

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: GenAI for test generation, test fixtures, edge cases, coverage, bug analysis

---

## Learning Objectives

By the end of Day 9, you will be able to:
- Use GenAI for unit and integration test generation
- Generate test fixtures and edge cases with AI
- Use AI for bug analysis and test prioritization
- Integrate test coverage tools
- **Apply prompt engineering tailored to the testing phase of the SDLC** (Learning Objective)

**Note**: This day addresses the learning objective: "Use LLMs and GenAI tools for requirements, design, code generation, and **testing**."

---

## Pre-Activity: Why Testing Matters with AI

**Critical insight**: When AI writes code, testing becomes even more important!

**Why**:
- AI can introduce bugs
- AI might miss edge cases
- AI doesn't know your business logic perfectly
- Tests verify AI suggestions work correctly
- Tests document expected behavior

**Think about**:
- What happens if AI-generated code has a bug?
- How do you know AI code works correctly?
- What edge cases might AI miss?

**Your thoughts**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Understanding pytest Basics

### pytest Overview

**pytest** is Python's testing framework:
- Simple syntax
- Great for AI-generated tests
- Excellent error messages
- Plugin ecosystem

### Basic Test Structure

```python
def test_function_name():
    # Arrange: Set up test data
    # Act: Execute the code
    # Assert: Check the result
    assert result == expected
```

### Activity: Write Your First Test (Manually)

**Test this function**:
```python
def add(a, b):
    return a + b
```

**Your test**:
```python
def test_add():
    # Your test here
    pass
```

**Now let AI help you write better tests!**

---

## Activity 2: Generate Unit Tests with AI

### Activity: Generate Tests for a Function

**Step 1: Provide Function to AI**

**Your function** (from Day 8):
```python
[Paste a function from your API]
```

**Step 2: Ask AI to Generate Tests**

**Prompt**:
```
Generate comprehensive pytest unit tests for this function:

[Your function code]

Include:
- Happy path tests
- Edge cases
- Error cases
- Boundary conditions
- Use pytest fixtures where appropriate
- Follow pytest best practices
```

**AI-Generated Tests**:
```python
[Paste generated tests]
```

**Step 3: Review Tests**

**Checklist**:
- [ ] Tests cover happy path
- [ ] Edge cases included
- [ ] Error cases handled
- [ ] Assertions are clear
- [ ] Test names are descriptive

**What's missing?**
_______________________________________________________________________

**Step 4: Run Tests**

```bash
pytest test_your_file.py -v
```

**Results**:
- Tests passed: _____
- Tests failed: _____
- Issues: _______________________________________________________________________

### Activity: Generate Tests for API Endpoints

**Prompt**:
```
Generate pytest tests for this FastAPI endpoint:

[Your endpoint code]

Include:
- Test successful requests
- Test validation errors
- Test authentication (if applicable)
- Test error responses
- Use TestClient from FastAPI
- Test different status codes
```

**Your endpoint**:
_______________________________________________________________________

**AI-Generated Tests**:
```python
[Paste tests]
```

**Run the tests**: [ ] All passed [ ] Some failed

**Fix issues with AI help**:
- Prompt: _______________________________________________________________________
- Solution: _______________________________________________________________________

---

## Activity 3: Generate Test Fixtures with AI

### Understanding Fixtures

**Fixtures** = Reusable test data and setup

**Common fixtures**:
- Database connections
- Test data
- Mock objects
- API clients

### Activity: Create Fixtures with AI

**Prompt**:
```
Create pytest fixtures for testing a FastAPI application:

Include:
- Test client fixture
- Database fixture (setup/teardown)
- Sample data fixtures
- Authentication fixture (if needed)

Use pytest best practices for fixture scope and cleanup.
```

**AI-Generated Fixtures**:
```python
[Paste fixtures]
```

**Use fixtures in your tests**:
```python
def test_endpoint(test_client, sample_data):
    # Use fixtures here
    pass
```

---

## Activity 4: Edge Cases and Boundary Testing

### Activity: Identify Edge Cases with AI

**Prompt**:
```
For this function: [your function]

Identify potential edge cases and boundary conditions that should be tested.

Include:
- Empty inputs
- Null/None values
- Very large numbers
- Negative numbers
- Invalid types
- Boundary values
```

**Your function**:
_______________________________________________________________________

**AI-Identified Edge Cases**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________

### Activity: Generate Edge Case Tests

**Prompt**:
```
Generate pytest tests for these edge cases: [edge cases from above]

Make sure each edge case has a specific test with clear assertions.
```

**AI-Generated Edge Case Tests**:
```python
[Paste tests]
```

**Run edge case tests**: [ ] All passed

---

## Activity 5: Integration Tests with AI

### Understanding Integration Tests

**Integration tests** = Test how components work together

**Examples**:
- API + Database
- Multiple endpoints
- Full user workflows

### Activity: Generate Integration Tests

**Prompt**:
```
Generate integration tests for this FastAPI application:

[Describe your app structure]

Test:
- Complete user workflows
- Database interactions
- Multiple endpoints working together
- Error propagation
- Data consistency

Use pytest and FastAPI TestClient.
```

**Your app structure**:
_______________________________________________________________________

**AI-Generated Integration Tests**:
```python
[Paste tests]
```

**Run integration tests**: [ ] All passed

---

## Activity 6: Test Coverage

### Understanding Coverage

**Coverage** = What percentage of code is tested

**Why it matters**:
- Shows what's not tested
- Helps find gaps
- Ensures important code is tested

### Activity: Set Up Coverage

**Install coverage**:
```bash
pip install pytest-cov
```

**Run with coverage**:
```bash
pytest --cov=your_module --cov-report=html
```

**View report**: Open `htmlcov/index.html`

**Initial coverage**: _____%

### Activity: Improve Coverage with AI

**Prompt**:
```
My test coverage is [X]%. 

Here's my code: [your code]
Here are my current tests: [your tests]

Identify what's not covered and generate tests to improve coverage.

Focus on:
- Untested functions
- Untested branches
- Error paths
- Edge cases
```

**Coverage before**: _____%  
**Coverage after**: _____%

**What tests were added?**
_______________________________________________________________________

---

## Activity 7: AI-Driven Bug Analysis

### Activity: Analyze Bugs with AI

**Scenario**: You found a bug in your code

**Bug description**:
_______________________________________________________________________

**Prompt**:
```
I found this bug: [bug description]

Here's the code: [relevant code]

Help me:
1. Understand what's causing the bug
2. Identify the root cause
3. Suggest a fix
4. Write a test that would have caught this bug
```

**AI Analysis**:
_______________________________________________________________________
_______________________________________________________________________

**Fix applied?** [ ] Yes  
**Test added?** [ ] Yes

### Activity: Prioritize Tests with AI

**Prompt**:
```
I have these functions/endpoints: [list]

Help me prioritize which ones need the most testing based on:
- Business criticality
- Complexity
- Risk of failure
- User impact

Suggest a testing priority order.
```

**Your functions/endpoints**:
_______________________________________________________________________

**AI Priority Order**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

**Why these priorities?**
_______________________________________________________________________

---

## Activity 8: Test Organization and Structure

### Activity: Organize Tests with AI

**Prompt**:
```
Help me organize my test files for this FastAPI project:

[Project structure]

Suggest:
- Test file structure
- Naming conventions
- How to organize unit vs integration tests
- Fixture organization
- Test data management

Create a clear test structure.
```

**Your project structure**:
_______________________________________________________________________

**AI-Suggested Structure**:
```
tests/
├── 
├── 
└── 
```

**Implement the structure**: [ ] Done

---

## Activity 9: Create Test Suite

### Organize Your Tests

**Create test structure**:
```
tests/
├── __init__.py
├── conftest.py          # Shared fixtures
├── test_models.py       # Model tests
├── test_routers.py      # Endpoint tests
├── test_integration.py  # Integration tests
└── fixtures/            # Test data
```

**All tests created?** [ ] Yes

### Run Full Test Suite

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=. --cov-report=html

# Run specific test file
pytest tests/test_routers.py

# Run with verbose output
pytest -v
```

**Test results**:
- Total tests: _____
- Passed: _____
- Failed: _____
- Coverage: _____%

**Fix any failures**: [ ] All fixed

---

## Activity 10: Create Deliverables

### Deliverable 1: Test Suite

**Your test files**:
- [ ] `tests/conftest.py` (fixtures)
- [ ] `tests/test_models.py`
- [ ] `tests/test_routers.py`
- [ ] `tests/test_integration.py`

**All tests passing?** [ ] Yes

### Deliverable 2: Coverage Report

**Generate coverage report**:
```bash
pytest --cov=. --cov-report=html --cov-report=term
```

**Coverage percentage**: _____%

**Coverage report location**: `htmlcov/index.html`

**Report generated?** [ ] Yes

### Deliverable 3: AI Usage Log

**File**: `week2/day9/AI-Usage-Log.md`

**Document**:
- Test generation prompts
- Fixture creation prompts
- Edge case identification prompts
- Bug analysis prompts
- What worked well
- What didn't work

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Generated unit tests for key functions
- [ ] Generated tests for API endpoints
- [ ] Created test fixtures
- [ ] Identified and tested edge cases
- [ ] Created integration tests
- [ ] Set up coverage reporting
- [ ] Achieved reasonable coverage (aim for 70%+)
- [ ] Used AI for bug analysis
- [ ] Organized test structure
- [ ] All tests passing
- [ ] Documented AI usage
- [ ] Committed to repository
- [ ] Created PR with test suite

---

## Reflection Questions

1. **How did AI help you write better tests?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What edge cases did AI identify that you might have missed?**
   _______________________________________________________________________

3. **How important is testing when using AI-generated code?**
   _______________________________________________________________________

4. **What testing practices will you continue using?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Always test AI-generated code
- ✅ AI is great at generating test cases
- ✅ Coverage helps find gaps
- ✅ Edge cases are critical
- ✅ Tests document expected behavior
- ✅ Integration tests catch system-level issues

**Best practices**:
- Test happy paths and error cases
- Use fixtures for reusable setup
- Aim for good coverage (70%+)
- Organize tests clearly
- Run tests frequently

---

## Additional Resources

- [pytest Documentation](https://docs.pytest.org/en/stable/)
- [pytest-cov Documentation](https://pytest-cov.readthedocs.io/)
- [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/)
- [Test-Driven Development Guide](https://testdriven.io/test-driven-development/)

---

## Next Steps

Tomorrow (Day 10), you'll work on Deployment & Maintenance. Make sure you:
- Have a working test suite
- Understand your test coverage
- Are ready to set up CI/CD
- Have tests that can run in CI

**Excellent testing work!** 🧪

