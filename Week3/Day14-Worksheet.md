# Week 3, Day 14 Worksheet: Capstone Day 2

**Estimated Time**: 6–8 hours  
**Focus**: Implement tests, security review, SQL optimization, build core UI

---

## Learning Objectives

By the end of Day 14, you will be able to:
- Create comprehensive test suite with AI assistance
- Perform security vulnerability assessment
- Optimize SQL queries using AI
- Build core React UI components
- Integrate frontend with backend API

---

## Pre-Activity: Day 14 Overview

**Today's goals**:
- ✅ Comprehensive test suite
- ✅ Security review and fixes
- ✅ SQL query optimization
- ✅ Core UI components
- ✅ Frontend-backend integration

**Your progress so far**:
- API scaffolded? [ ] Yes
- Database schema created? [ ] Yes
- Endpoints working? [ ] Yes

**Ready to build!** 💪

---

## Activity 1: Implement Test Suite

### Activity: Generate Unit Tests

**Prompt**:
```
Generate comprehensive pytest unit tests for this FastAPI application: [project description]

Test files needed:
- test_models.py (database models)
- test_routers.py (API endpoints)
- test_services.py (business logic, if any)
- conftest.py (shared fixtures)

Requirements:
- Test all endpoints (happy path, errors, validation)
- Test database models and relationships
- Use pytest fixtures for test data
- Mock external dependencies
- Achieve 80%+ coverage
- Follow pytest best practices

Include edge cases and error scenarios.
```

**AI-Generated Test Structure**:
_______________________________________________________________________

**Test files created?** [ ] Yes

### Activity: Generate Test Fixtures

**Prompt**:
```
Create comprehensive pytest fixtures for testing this FastAPI app.

Include:
- Test client fixture (FastAPI TestClient)
- Database fixture (setup/teardown with test DB)
- Authentication fixtures (if applicable)
- Sample data fixtures for all models
- Mock external services (if any)

Use appropriate fixture scopes (function, class, module).
```

**AI-Generated Fixtures**:
```python
[Paste fixtures]
```

**Fixtures created?** [ ] Yes  
**File**: `tests/conftest.py`

### Activity: Generate Endpoint Tests

**For each endpoint, generate tests**:

**Prompt template**:
```
Generate pytest tests for this endpoint: [endpoint description]

Test:
- Successful requests (200)
- Validation errors (422)
- Not found errors (404)
- Authentication/authorization (if applicable)
- Edge cases
- Error handling

Use FastAPI TestClient and your fixtures.
```

**Endpoint 1 tests**:
```python
[Paste tests]
```

**Continue for all endpoints...**

**All endpoint tests created?** [ ] Yes

### Activity: Run Tests and Check Coverage

**Run tests**:
```bash
pytest --cov=. --cov-report=html --cov-report=term
```

**Results**:
- Tests written: _____
- Tests passing: _____
- Coverage: _____%

**Target**: 80%+ coverage

**Coverage achieved?** [ ] Yes  
**If not, generate more tests**:

**Prompt**:
```
My test coverage is [X]%. Generate additional tests to reach 80%+.

Focus on:
- Untested functions
- Error paths
- Edge cases
- Boundary conditions
```

**Additional tests generated?** [ ] Yes  
**New coverage**: _____%

---

## Activity 2: Security Review

### Activity: Identify Security Vulnerabilities

**Prompt**:
```
Perform a security review of this FastAPI application: [project description]

Check for:
- OWASP Top 10 vulnerabilities
- OWASP API Security Top 10 issues
- SQL injection risks
- Authentication/authorization issues
- Input validation problems
- Sensitive data exposure
- Security misconfiguration
- Insecure dependencies

Review the codebase and provide:
- List of vulnerabilities found
- Severity (Critical/High/Medium/Low)
- Affected code locations
- Remediation steps
```

**AI Security Review**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Vulnerabilities found**:
1. **Severity**: _____ | **Issue**: _______________________________________________________________________
2. **Severity**: _____ | **Issue**: _______________________________________________________________________
3. **Severity**: _____ | **Issue**: _______________________________________________________________________

### Activity: Fix Security Issues

**For each vulnerability, generate fix**:

**Prompt template**:
```
Fix this security vulnerability: [vulnerability description]

In this code: [affected code]

Provide:
- Secure code replacement
- Explanation of the fix
- Additional security measures
- Tests to verify the fix
```

**Vulnerability 1 fix**:
_______________________________________________________________________

**Vulnerability 2 fix**:
_______________________________________________________________________

**Continue for all vulnerabilities...**

**All vulnerabilities fixed?** [ ] Yes

### Activity: Add Security Best Practices

**Prompt**:
```
Add security best practices to this FastAPI application.

Include:
- Input validation on all endpoints
- Rate limiting
- CORS configuration
- Security headers
- Password hashing (if applicable)
- JWT token handling (if applicable)
- Environment variable security
- Dependency security scanning

Implement security middleware and configurations.
```

**AI Security Enhancements**:
_______________________________________________________________________

**Security improvements added?** [ ] Yes

---

## Activity 3: SQL Optimization

### Activity: Analyze SQL Queries

**Identify slow queries in your application**:

**Queries to optimize**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

### Activity: Optimize Queries with AI

**Prompt**:
```
Optimize this SQL query: [your query]

Context:
- Database: [PostgreSQL/SQLite]
- Table structure: [your schema]
- Expected data volume: [small/medium/large]
- Common access patterns: [read-heavy/write-heavy]

Provide:
- Optimized query
- Explanation of optimizations
- Index recommendations
- Query execution plan analysis
- Performance improvements expected
```

**Query 1 optimization**:
_______________________________________________________________________
_______________________________________________________________________

**Query 2 optimization**:
_______________________________________________________________________
_______________________________________________________________________

**Continue for all queries...**

### Activity: Generate Indexes

**Prompt**:
```
Based on this database schema: [your schema]

And these query patterns: [your queries]

Recommend database indexes for optimal performance.

Include:
- Indexes needed
- Index types (B-tree, composite, etc.)
- Columns to index
- Index creation SQL
- Performance impact explanation
```

**AI Index Recommendations**:
_______________________________________________________________________

**Indexes created?** [ ] Yes

**Test performance**:
- Before optimization: _____ ms
- After optimization: _____ ms
- Improvement: _____%

---

## Activity 4: Build Core UI

### Activity: Set Up React Project

**Create React app** (if not done):
```bash
npm create vite@latest frontend -- --template react
cd frontend
npm install
```

**Or use Next.js**:
```bash
npx create-next-app@latest frontend
cd frontend
```

**React project created?** [ ] Yes

### Activity: Generate UI Components

**From your PRD, identify UI components needed**:

**Components**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________

**Generate each component**:

**Prompt template**:
```
Create a React component for: [component description]

Requirements:
- Functional component with hooks
- TypeScript types
- Styling (CSS modules, Tailwind, or styled-components)
- Responsive design
- Accessibility (ARIA labels, keyboard navigation)
- Error handling
- Loading states
- Follow React best practices

Props: [list props needed]
State: [list state needed]
```

**Component 1**: _______________________________________________________________________
**Code**:
```tsx
[Paste component code]
```

**Component 2**: _______________________________________________________________________
**Code**:
```tsx
[Paste component code]
```

**Continue for all components...**

**All components created?** [ ] Yes

### Activity: Generate API Integration

**Prompt**:
```
Create API integration code for this React app to connect to FastAPI backend.

Include:
- API client setup (axios or fetch)
- API service functions for all endpoints
- Error handling
- Loading states
- Type definitions for API responses
- Environment configuration

Backend URL: [your API URL]
Endpoints: [list your endpoints]
```

**AI-Generated API Integration**:
_______________________________________________________________________

**API integration created?** [ ] Yes

### Activity: Create Main Pages

**Generate main pages**:

**Prompt**:
```
Create React pages for: [page description]

Include:
- Page component
- Data fetching
- State management
- Error handling
- Loading states
- Integration with API
- Responsive layout

Pages needed: [list pages]
```

**Page 1**: _______________________________________________________________________
**Code**:
```tsx
[Paste page code]
```

**Continue for all pages...**

**All pages created?** [ ] Yes

---

## Activity 5: Integrate Frontend and Backend

### Activity: Configure CORS

**In your FastAPI app, ensure CORS is configured**:

**Check main.py**:
- [ ] CORS middleware added
- [ ] Frontend URL allowed
- [ ] Credentials allowed (if needed)

**CORS working?** [ ] Yes

### Activity: Test Integration

**Test 1: API connection**
- Frontend can call backend? [ ] Yes
- CORS working? [ ] Yes

**Test 2: Data flow**
- Can create data from frontend? [ ] Yes
- Can read data in frontend? [ ] Yes
- Can update data? [ ] Yes
- Can delete data? [ ] Yes

**Test 3: Error handling**
- Errors displayed properly? [ ] Yes
- Loading states work? [ ] Yes

**All integration tests passing?** [ ] Yes

---

## Activity 6: Create Deliverables

### Deliverable Checklist

- [ ] **Test Suite** (80%+ coverage)
  - [ ] Unit tests for models
  - [ ] Tests for all endpoints
  - [ ] Integration tests
  - [ ] Test fixtures
  - [ ] Coverage report

- [ ] **Security Review**
  - [ ] Vulnerabilities identified
  - [ ] Vulnerabilities fixed
  - [ ] Security best practices implemented
  - [ ] Security documentation

- [ ] **SQL Optimization**
  - [ ] Queries optimized
  - [ ] Indexes created
  - [ ] Performance improved
  - [ ] Optimization documented

- [ ] **Core UI**
  - [ ] React app set up
  - [ ] Components created
  - [ ] Pages created
  - [ ] API integration working
  - [ ] Frontend-backend connected

- [ ] **AI Usage Log** (`capstone/day14/AI-Usage-Log.md`)

---

## Day 14 Milestone Checklist

**Per Capstone Rubric**:
- [ ] Tests implemented and passing
- [ ] Security review completed
- [ ] SQL queries optimized
- [ ] Core UI built
- [ ] Frontend-backend integrated
- [ ] All AI usage documented

---

## Reflection Questions

1. **How did AI help you write comprehensive tests?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What security issues did you find and fix?**
   _______________________________________________________________________

3. **How much did SQL optimization improve performance?**
   _______________________________________________________________________

4. **What was most challenging about building the UI?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Tests are essential, especially with AI code
- ✅ Security can't be an afterthought
- ✅ Performance optimization matters
- ✅ UI should be functional and responsive
- ✅ Integration testing is critical

**Tomorrow (Day 15)**:
- Wire CI/CD
- Polish documentation
- Rehearse demo
- Present your work!

**Almost there!** 🎉

---

## Next Steps

**Before Day 15**:
- [ ] All tests passing
- [ ] Security issues resolved
- [ ] UI is functional
- [ ] Frontend-backend working together
- [ ] Prepare for final polish

**See you tomorrow for the final day!** 🚀

