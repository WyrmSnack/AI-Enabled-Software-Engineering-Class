# OWASP Application Guide

How to apply OWASP Top 10 security principles with AI assistance.

## OWASP Top 10 (2021) with AI

### A01: Broken Access Control

**Problem**: Users can access resources they shouldn't.

**AI Prompt for Prevention**:
```
Add authorization checks to this endpoint to ensure users can only access their own data:

[Endpoint code]

Requirements:
- Check user ID matches resource owner
- Return 403 if unauthorized
- Log unauthorized access attempts
```

**Example Fix**:
```python
@app.get("/users/{user_id}/tasks")
async def get_user_tasks(
    user_id: int,
    current_user: User = Depends(get_current_user),
    db: Session = Depends(get_db)
):
    # Authorization check
    if current_user.id != user_id:
        raise HTTPException(status_code=403, detail="Not authorized")
    
    tasks = db.query(Task).filter(Task.user_id == user_id).all()
    return tasks
```

---

### A02: Cryptographic Failures

**Problem**: Sensitive data not properly protected.

**AI Prompt for Prevention**:
```
Review this code for cryptographic failures:

[Code with sensitive data]

Ensure:
- Passwords are hashed with bcrypt
- Sensitive data is encrypted
- Keys are in environment variables
- No secrets in code
```

**Example Fix**:
```python
from passlib.context import CryptContext

pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")

def hash_password(password: str) -> str:
    return pwd_context.hash(password)

def verify_password(plain: str, hashed: str) -> bool:
    return pwd_context.verify(plain, hashed)
```

---

### A03: Injection

**Problem**: SQL injection, NoSQL injection, command injection.

**AI Prompt for Prevention**:
```
Review this code for injection vulnerabilities:

[Code with database queries]

Ensure:
- Use parameterized queries
- No string concatenation in SQL
- Input validation
- Use ORM methods
```

**Example Fix**:
```python
# ❌ Vulnerable
query = f"SELECT * FROM users WHERE email = '{email}'"

# ✅ Secure
user = db.query(User).filter(User.email == email).first()
```

---

### A04: Insecure Design

**Problem**: Security not considered in design.

**AI Prompt for Design**:
```
Design a secure authentication system for this application:

[Application description]

Include:
- Password requirements
- Session management
- Rate limiting
- Security headers
- Error handling
```

---

### A05: Security Misconfiguration

**Problem**: Default or insecure configurations.

**AI Prompt for Configuration**:
```
Review this configuration for security issues:

[Configuration code]

Check:
- Debug mode disabled in production
- Default passwords changed
- Security headers set
- CORS configured properly
- Error handling secure
```

**Example Fix**:
```python
# Security headers
@app.middleware("http")
async def add_security_headers(request, call_next):
    response = await call_next(request)
    response.headers["X-Content-Type-Options"] = "nosniff"
    response.headers["X-Frame-Options"] = "DENY"
    response.headers["X-XSS-Protection"] = "1; mode=block"
    return response
```

---

### A06: Vulnerable Components

**Problem**: Using outdated or vulnerable dependencies.

**AI Prompt for Review**:
```
Review dependencies for security vulnerabilities:

[requirements.txt or package.json]

Check:
- All dependencies up to date
- Known vulnerabilities
- Unnecessary dependencies
- Version pinning
```

**Commands**:
```bash
# Python
pip-audit
pip list --outdated

# Node.js
npm audit
npm outdated
```

---

### A07: Authentication Failures

**Problem**: Weak authentication mechanisms.

**AI Prompt for Implementation**:
```
Implement secure authentication with:

[Requirements]

Include:
- Password hashing (bcrypt)
- JWT tokens with expiration
- Session management
- Account lockout
- Password complexity
```

**Example**:
```python
from jose import jwt
from datetime import datetime, timedelta

SECRET_KEY = os.getenv("SECRET_KEY")
ALGORITHM = "HS256"
ACCESS_TOKEN_EXPIRE_MINUTES = 30

def create_access_token(data: dict):
    to_encode = data.copy()
    expire = datetime.utcnow() + timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    to_encode.update({"exp": expire})
    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)
```

---

### A08: Software and Data Integrity

**Problem**: Unverified dependencies or CI/CD issues.

**AI Prompt for CI/CD Security**:
```
Review this CI/CD pipeline for security:

[GitHub Actions workflow]

Ensure:
- Secrets managed securely
- Dependencies verified
- Code signing
- Secure deployment
```

---

### A09: Security Logging Failures

**Problem**: Insufficient logging and monitoring.

**AI Prompt for Logging**:
```
Add security logging to this application:

[Application code]

Log:
- Authentication attempts
- Authorization failures
- Sensitive operations
- Error conditions
- Security events

Don't log:
- Passwords
- Tokens
- Sensitive data
```

**Example**:
```python
import logging

security_logger = logging.getLogger("security")

def log_security_event(event_type: str, user_id: int, details: dict):
    security_logger.warning(f"{event_type}: user={user_id}, {details}")
```

---

### A10: Server-Side Request Forgery (SSRF)

**Problem**: Making requests to internal resources.

**AI Prompt for Prevention**:
```
Review this code for SSRF vulnerabilities:

[Code making HTTP requests]

Ensure:
- URL validation
- Whitelist allowed domains
- No internal network access
- Input sanitization
```

**Example Fix**:
```python
ALLOWED_DOMAINS = ["api.example.com", "public-api.com"]

def validate_url(url: str) -> bool:
    parsed = urlparse(url)
    return parsed.netloc in ALLOWED_DOMAINS

def fetch_data(url: str):
    if not validate_url(url):
        raise ValueError("URL not allowed")
    # ... fetch data
```

---

## OWASP API Security Top 10 (2023)

### API1: Broken Object Level Authorization

**AI Prompt**:
```
Add object-level authorization to this API endpoint:

[Endpoint code]

Ensure users can only access their own objects.
```

### API2: Broken Authentication

**AI Prompt**:
```
Review authentication implementation:

[Auth code]

Check for:
- Token expiration
- Secure token storage
- Strong password requirements
```

### API3: Broken Object Property Level Authorization

**AI Prompt**:
```
Add property-level authorization:

[Code accessing object properties]

Ensure users can only access allowed properties.
```

### API4: Unrestricted Resource Consumption

**AI Prompt**:
```
Add rate limiting to this API:

[API endpoints]

Implement:
- Rate limiting per user
- Request size limits
- Timeout handling
```

**Example**:
```python
from slowapi import Limiter
from slowapi.util import get_remote_address

limiter = Limiter(key_func=get_remote_address)

@app.get("/api/data")
@limiter.limit("10/minute")
async def get_data():
    return {"data": "..."}
```

---

## Security Testing with AI

### Generate Security Tests

**Prompt**:
```
Generate security tests for this endpoint:

[Endpoint code]

Test for:
- SQL injection
- XSS
- CSRF
- Authorization bypass
- Input validation
```

### Review Code for Vulnerabilities

**Prompt**:
```
Review this code for security vulnerabilities:

[Code]

Check for:
- Injection attacks
- Authentication issues
- Authorization problems
- Data exposure
- Configuration issues
```

---

## Security Checklist with AI

**Prompt**:
```
Create a security checklist for this application:

[Application description]

Include OWASP Top 10 items and API security considerations.
```

---

## Resources

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP API Security](https://owasp.org/API-Security/editions/2023/en/)
- [OWASP Cheat Sheets](https://cheatsheetseries.owasp.org/)
- [Security Headers](https://securityheaders.com/)

