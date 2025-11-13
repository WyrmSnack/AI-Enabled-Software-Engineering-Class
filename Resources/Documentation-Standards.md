# Documentation Standards

Standards for documenting code and projects.

## README Structure

### Required Sections
1. Project Title and Description
2. Features
3. Installation
4. Usage
5. Configuration
6. API Documentation (if applicable)
7. Testing
8. Contributing
9. License

### Example README
```markdown
# Project Name

Brief description of the project.

## Features

- Feature 1
- Feature 2
- Feature 3

## Installation

\`\`\`bash
pip install -r requirements.txt
\`\`\`

## Usage

\`\`\`python
from app import create_app
app = create_app()
\`\`\`

## API Documentation

See [API Docs](docs/api.md)

## Testing

\`\`\`bash
pytest
\`\`\`

## License

MIT
```

---

## Code Documentation

### Python Docstrings
```python
def calculate_total(items: list[float], tax_rate: float = 0.10) -> float:
    """
    Calculate total price with tax.
    
    Args:
        items: List of item prices
        tax_rate: Tax rate as decimal (default: 0.10)
    
    Returns:
        Total price including tax
    
    Raises:
        ValueError: If items list is empty
    
    Example:
        >>> calculate_total([10.0, 20.0], 0.10)
        33.0
    """
    if not items:
        raise ValueError("Items list cannot be empty")
    
    subtotal = sum(items)
    return subtotal * (1 + tax_rate)
```

### JavaScript/React Comments
```jsx
/**
 * UserCard component displays user information.
 * 
 * @param {Object} user - User object with name and email
 * @param {Function} onEdit - Callback when edit button is clicked
 * @returns {JSX.Element} User card component
 */
function UserCard({ user, onEdit }) {
  return (
    <div className="user-card">
      <h3>{user.name}</h3>
      <p>{user.email}</p>
      <button onClick={onEdit}>Edit</button>
    </div>
  );
}
```

---

## API Documentation

### OpenAPI/Swagger
```python
@app.post(
    "/users",
    response_model=UserResponse,
    summary="Create a new user",
    description="Create a new user with the provided information",
    responses={
        201: {"description": "User created successfully"},
        400: {"description": "Invalid input"},
        409: {"description": "User already exists"}
    }
)
async def create_user(user: UserCreate):
    """
    Create a new user.
    
    - **name**: User's full name
    - **email**: User's email address (must be unique)
    - **password**: User's password (min 8 characters)
    """
    ...
```

---

## Using AI for Documentation

### Generate README
**Prompt**:
```
Create a comprehensive README for this project:

[Project description]

Include all standard sections.
```

### Generate Docstrings
**Prompt**:
```
Add docstrings to this function:

[Function code]

Follow Google style docstring format.
```

---

## Resources

- [Google Style Guide](https://google.github.io/styleguide/)
- [Sphinx Documentation](https://www.sphinx-doc.org/)
- [JSDoc](https://jsdoc.app/)

