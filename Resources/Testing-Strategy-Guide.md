# Testing Strategy Guide

Comprehensive guide to testing strategies for software development.

## Test Pyramid

### Unit Tests (Base - Most Tests)
- Test individual functions/methods
- Fast execution
- Isolated from dependencies
- High coverage

### Integration Tests (Middle - Some Tests)
- Test component interactions
- Test with real dependencies (DB, APIs)
- Slower than unit tests
- Moderate coverage

### E2E Tests (Top - Few Tests)
- Test complete user flows
- Test entire system
- Slowest execution
- Low coverage but high value

---

## When to Write Tests

### Test-Driven Development (TDD)
1. Write test first
2. Write code to pass test
3. Refactor
4. Repeat

**Best for**: New features, critical logic

### Test-After Development
1. Write code
2. Write tests
3. Refactor

**Best for**: Learning, prototyping, AI-generated code

---

## Unit Testing with pytest

### Basic Test
```python
def test_add():
    assert add(2, 3) == 5
```

### Test with Fixtures
```python
@pytest.fixture
def sample_user():
    return User(name="Test", email="test@example.com")

def test_user_creation(sample_user):
    assert sample_user.name == "Test"
```

### Parametrized Tests
```python
@pytest.mark.parametrize("input,expected", [
    (2, 4),
    (3, 9),
    (4, 16),
])
def test_square(input, expected):
    assert square(input) == expected
```

---

## Integration Testing

### Database Tests
```python
@pytest.fixture
def db_session():
    Base.metadata.create_all(bind=engine)
    session = SessionLocal()
    yield session
    session.close()
    Base.metadata.drop_all(bind=engine)

def test_create_user(db_session):
    user = User(name="Test", email="test@example.com")
    db_session.add(user)
    db_session.commit()
    assert user.id is not None
```

### API Tests
```python
def test_create_task(client):
    response = client.post("/tasks", json={
        "title": "Test Task",
        "description": "Test"
    })
    assert response.status_code == 201
    assert response.json()["title"] == "Test Task"
```

---

## Test Coverage

### Measure Coverage
```bash
pytest --cov=app --cov-report=html
```

### Coverage Goals
- **Minimum**: 60%
- **Good**: 70-80%
- **Excellent**: 80%+

### What to Test
- ✅ Happy paths
- ✅ Edge cases
- ✅ Error cases
- ✅ Boundary conditions
- ✅ Business logic

### What Not to Test
- ❌ Framework code
- ❌ Third-party libraries
- ❌ Trivial getters/setters
- ❌ Generated code (unless critical)

---

## Using AI for Test Generation

### Generate Unit Tests
**Prompt**:
```
Generate comprehensive pytest unit tests for this function:

[Function code]

Include:
- Happy path tests
- Edge cases
- Error cases
- Boundary conditions
- Use pytest fixtures where appropriate
```

### Generate Integration Tests
**Prompt**:
```
Generate integration tests for this API endpoint:

[Endpoint code]

Test:
- Successful requests
- Error cases
- Authentication
- Authorization
- Validation
```

### Review Tests
**Prompt**:
```
Review these tests for:
- Missing test cases
- Test quality
- Coverage gaps
- Best practices

[Test code]
```

---

## Test Best Practices

### Do's
✅ Test behavior, not implementation
✅ Use descriptive test names
✅ Keep tests independent
✅ Use fixtures for setup
✅ Test edge cases
✅ Mock external dependencies
✅ Keep tests fast

### Don'ts
❌ Test implementation details
❌ Write slow tests unnecessarily
❌ Skip error cases
❌ Write flaky tests
❌ Test framework code
❌ Ignore test failures

---

## Resources

- [pytest Documentation](https://docs.pytest.org/)
- [Test-Driven Development](https://en.wikipedia.org/wiki/Test-driven_development)
- [Testing Best Practices](https://testingjavascript.com/)

