# Error Handling Patterns

Comprehensive guide to error handling in FastAPI and React applications.

## FastAPI Error Handling

### Basic Error Handling

```python
from fastapi import FastAPI, HTTPException, status

app = FastAPI()

@app.get("/items/{item_id}")
async def get_item(item_id: int):
    if item_id < 1:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail="Item ID must be positive"
        )
    
    item = get_item_from_db(item_id)
    if not item:
        raise HTTPException(
            status_code=status.HTTP_404_NOT_FOUND,
            detail=f"Item {item_id} not found"
        )
    
    return item
```

### Custom Exception Classes

```python
class NotFoundError(Exception):
    """Custom exception for not found errors"""
    pass

class ValidationError(Exception):
    """Custom exception for validation errors"""
    pass

@app.exception_handler(NotFoundError)
async def not_found_handler(request, exc):
    return JSONResponse(
        status_code=404,
        content={"detail": str(exc)}
    )
```

### Database Error Handling

```python
from sqlalchemy.exc import IntegrityError, SQLAlchemyError

@app.post("/users")
async def create_user(user_data: UserCreate, db: Session = Depends(get_db)):
    try:
        user = User(**user_data.dict())
        db.add(user)
        db.commit()
        return user
    except IntegrityError:
        db.rollback()
        raise HTTPException(
            status_code=400,
            detail="User already exists"
        )
    except SQLAlchemyError as e:
        db.rollback()
        logger.error(f"Database error: {e}")
        raise HTTPException(
            status_code=500,
            detail="Database error occurred"
        )
```

### Validation Error Handling

```python
from fastapi.exceptions import RequestValidationError
from fastapi.responses import JSONResponse

@app.exception_handler(RequestValidationError)
async def validation_exception_handler(request, exc):
    return JSONResponse(
        status_code=422,
        content={
            "detail": exc.errors(),
            "body": exc.body
        }
    )
```

### Global Exception Handler

```python
@app.exception_handler(Exception)
async def global_exception_handler(request, exc):
    logger.error(f"Unhandled exception: {exc}", exc_info=True)
    return JSONResponse(
        status_code=500,
        content={"detail": "Internal server error"}
    )
```

---

## React Error Handling

### Error Boundaries

```jsx
import React from 'react';

class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false, error: null };
  }

  static getDerivedStateFromError(error) {
    return { hasError: true, error };
  }

  componentDidCatch(error, errorInfo) {
    console.error('Error caught:', error, errorInfo);
  }

  render() {
    if (this.state.hasError) {
      return (
        <div>
          <h2>Something went wrong.</h2>
          <p>{this.state.error?.message}</p>
        </div>
      );
    }
    return this.props.children;
  }
}

// Usage
function App() {
  return (
    <ErrorBoundary>
      <YourComponent />
    </ErrorBoundary>
  );
}
```

### API Error Handling

```jsx
async function fetchData() {
  try {
    const response = await fetch('/api/items');
    
    if (!response.ok) {
      if (response.status === 404) {
        throw new Error('Item not found');
      } else if (response.status === 401) {
        throw new Error('Unauthorized');
      } else {
        throw new Error('Request failed');
      }
    }
    
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error fetching data:', error);
    throw error;
  }
}
```

### Form Error Handling

```jsx
function TaskForm() {
  const [error, setError] = useState(null);
  const [loading, setLoading] = useState(false);

  const handleSubmit = async (e) => {
    e.preventDefault();
    setError(null);
    setLoading(true);

    try {
      const response = await fetch('/api/tasks', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(formData)
      });

      if (!response.ok) {
        const errorData = await response.json();
        throw new Error(errorData.detail || 'Failed to create task');
      }

      const data = await response.json();
      // Handle success
    } catch (error) {
      setError(error.message);
    } finally {
      setLoading(false);
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      {error && <div className="error">{error}</div>}
      {/* Form fields */}
      <button disabled={loading}>
        {loading ? 'Creating...' : 'Create Task'}
      </button>
    </form>
  );
}
```

---

## API Error Response Formats

### Standard Format

```json
{
  "detail": "Error message",
  "type": "error_type",
  "code": "ERROR_CODE",
  "timestamp": "2024-01-15T10:30:00Z"
}
```

### Validation Error Format

```json
{
  "detail": [
    {
      "loc": ["body", "email"],
      "msg": "value is not a valid email",
      "type": "value_error.email"
    }
  ]
}
```

### Implementation

```python
from pydantic import BaseModel
from datetime import datetime

class ErrorResponse(BaseModel):
    detail: str
    type: str
    code: str | None = None
    timestamp: datetime = datetime.utcnow()

@app.exception_handler(HTTPException)
async def http_exception_handler(request, exc):
    return JSONResponse(
        status_code=exc.status_code,
        content=ErrorResponse(
            detail=exc.detail,
            type="http_error",
            code=f"HTTP_{exc.status_code}"
        ).dict()
    )
```

---

## Common Error Scenarios

### 1. Not Found (404)
```python
raise HTTPException(status_code=404, detail="Resource not found")
```

### 2. Bad Request (400)
```python
raise HTTPException(status_code=400, detail="Invalid request data")
```

### 3. Unauthorized (401)
```python
raise HTTPException(
    status_code=401,
    detail="Not authenticated",
    headers={"WWW-Authenticate": "Bearer"}
)
```

### 4. Forbidden (403)
```python
raise HTTPException(status_code=403, detail="Not authorized")
```

### 5. Conflict (409)
```python
raise HTTPException(status_code=409, detail="Resource already exists")
```

### 6. Internal Server Error (500)
```python
logger.error(f"Unexpected error: {exc}")
raise HTTPException(status_code=500, detail="Internal server error")
```

---

## Best Practices

### Do's
✅ Use appropriate HTTP status codes
✅ Provide clear error messages
✅ Log errors for debugging
✅ Handle errors at appropriate levels
✅ Use error boundaries in React
✅ Validate input early
✅ Provide user-friendly messages

### Don'ts
❌ Expose internal errors to users
❌ Return stack traces in production
❌ Ignore errors silently
❌ Use generic error messages
❌ Return 500 for client errors
❌ Log sensitive information

---

## Error Handling with AI

### Using AI to Generate Error Handlers

**Prompt**:
```
Create error handling for this FastAPI endpoint:

[Endpoint code]

Include:
- Validation errors
- Database errors
- Not found errors
- Proper HTTP status codes
- User-friendly messages
```

### Using AI to Review Error Handling

**Prompt**:
```
Review this error handling code for:
- Missing error cases
- Appropriate status codes
- Security concerns
- Best practices

[Error handling code]
```

---

## Testing Error Handling

```python
def test_not_found_error(client):
    response = client.get("/items/999")
    assert response.status_code == 404
    assert "not found" in response.json()["detail"].lower()

def test_validation_error(client):
    response = client.post("/items", json={"invalid": "data"})
    assert response.status_code == 422
    assert "detail" in response.json()
```

---

## Resources

- [FastAPI Error Handling](https://fastapi.tiangolo.com/tutorial/handling-errors/)
- [React Error Boundaries](https://react.dev/reference/react/Component#catching-rendering-errors-with-an-error-boundary)
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

