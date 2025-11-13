# API Design Standards

Best practices for designing RESTful APIs.

## RESTful Principles

### Resource-Based URLs
```
✅ GET /users
✅ GET /users/123
✅ POST /users
✅ PUT /users/123
✅ DELETE /users/123

❌ GET /getUsers
❌ POST /createUser
❌ GET /userById?id=123
```

### HTTP Methods
- **GET**: Retrieve resources
- **POST**: Create resources
- **PUT**: Update entire resource
- **PATCH**: Partial update
- **DELETE**: Delete resources

### Status Codes
- **200 OK**: Success
- **201 Created**: Resource created
- **204 No Content**: Success, no response body
- **400 Bad Request**: Invalid request
- **401 Unauthorized**: Not authenticated
- **403 Forbidden**: Not authorized
- **404 Not Found**: Resource not found
- **422 Unprocessable Entity**: Validation error
- **500 Internal Server Error**: Server error

---

## Endpoint Naming

### Use Nouns, Not Verbs
```
✅ GET /users
✅ GET /tasks
✅ POST /orders

❌ GET /getUsers
❌ POST /createTask
❌ DELETE /removeOrder
```

### Use Plural Nouns
```
✅ GET /users
✅ GET /tasks
✅ GET /orders

❌ GET /user
❌ GET /task
```

### Use Hyphens, Not Underscores
```
✅ GET /user-profiles
✅ GET /order-items

❌ GET /user_profiles
❌ GET /orderItems
```

---

## Request/Response Formats

### Request Body
```json
{
  "name": "John Doe",
  "email": "john@example.com"
}
```

### Response Format
```json
{
  "id": 123,
  "name": "John Doe",
  "email": "john@example.com",
  "created_at": "2024-01-15T10:30:00Z"
}
```

### Error Response
```json
{
  "detail": "User not found",
  "type": "not_found",
  "code": "USER_404"
}
```

---

## Versioning

### URL Versioning
```
/api/v1/users
/api/v2/users
```

### Header Versioning
```
Accept: application/vnd.api+json;version=1
```

### Best Practice: URL Versioning
- Clear and explicit
- Easy to understand
- Cache-friendly

---

## Pagination

### Query Parameters
```
GET /users?page=1&limit=20
```

### Response Format
```json
{
  "data": [...],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 100,
    "pages": 5
  }
}
```

### Implementation
```python
@app.get("/users")
async def list_users(
    page: int = Query(1, ge=1),
    limit: int = Query(20, ge=1, le=100),
    db: Session = Depends(get_db)
):
    skip = (page - 1) * limit
    users = db.query(User).offset(skip).limit(limit).all()
    total = db.query(User).count()
    
    return {
        "data": users,
        "pagination": {
            "page": page,
            "limit": limit,
            "total": total,
            "pages": (total + limit - 1) // limit
        }
    }
```

---

## Filtering and Sorting

### Filtering
```
GET /users?status=active&role=admin
```

### Sorting
```
GET /users?sort=name&order=asc
GET /users?sort=-created_at  # Descending
```

### Implementation
```python
@app.get("/users")
async def list_users(
    status: str | None = None,
    role: str | None = None,
    sort: str = "id",
    order: str = "asc",
    db: Session = Depends(get_db)
):
    query = db.query(User)
    
    if status:
        query = query.filter(User.status == status)
    if role:
        query = query.filter(User.role == role)
    
    if order == "desc":
        query = query.order_by(desc(getattr(User, sort)))
    else:
        query = query.order_by(getattr(User, sort))
    
    return query.all()
```

---

## API Documentation

### OpenAPI/Swagger
```python
app = FastAPI(
    title="My API",
    description="API description",
    version="1.0.0",
    docs_url="/docs",
    redoc_url="/redoc"
)
```

### Endpoint Documentation
```python
@app.post(
    "/users",
    response_model=UserResponse,
    status_code=201,
    summary="Create a new user",
    description="Create a new user with the provided information",
    responses={
        201: {"description": "User created"},
        400: {"description": "Invalid input"},
        409: {"description": "User already exists"}
    }
)
async def create_user(user: UserCreate):
    """Create a new user."""
    ...
```

---

## Best Practices

### Do's
✅ Use RESTful conventions
✅ Use appropriate HTTP methods
✅ Return proper status codes
✅ Version your API
✅ Document your API
✅ Handle errors consistently
✅ Use pagination for lists
✅ Validate input
✅ Use HTTPS

### Don'ts
❌ Use verbs in URLs
❌ Return 200 for errors
❌ Expose internal errors
❌ Skip input validation
❌ Return too much data
❌ Use inconsistent formats
❌ Ignore security

---

## Using AI for API Design

### Generate API Endpoints
**Prompt**:
```
Design RESTful API endpoints for a [resource] management system.

Include:
- CRUD operations
- Proper HTTP methods
- Request/response formats
- Error handling
- Status codes
```

### Review API Design
**Prompt**:
```
Review this API design for:
- RESTful principles
- Best practices
- Consistency
- Security

[API endpoints]
```

---

## Resources

- [REST API Tutorial](https://restfulapi.net/)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [OpenAPI Specification](https://swagger.io/specification/)

