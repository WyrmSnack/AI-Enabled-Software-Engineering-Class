# Week 3, Day 13 Worksheet: Capstone Day 1

**Estimated Time**: 6–8 hours  
**Focus**: Finalize PRD and architecture, scaffold API, create database schema

---

## Learning Objectives

By the end of Day 13, you will be able to:
- Finalize your Product Requirements Document
- Complete system architecture design
- Scaffold a FastAPI REST API
- Design and generate database schema
- Set up project structure for full-stack application
- **Begin building a working prototype demonstrating GenAI‑enhanced workflows** (Learning Objective)

---

## Pre-Activity: Capstone Overview

**Your capstone project** = Full-stack application demonstrating GenAI across the SDLC

**What you'll build**:
- REST API with Python FastAPI
- Database with schema and migrations
- React frontend
- Tests and CI/CD
- Complete documentation

**Today's goals**:
- ✅ Finalize planning documents
- ✅ Complete architecture
- ✅ Scaffold API
- ✅ Create database schema

**Your project idea** (from Week 2):
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Finalize PRD

### Review Your Week 2 PRD

**From Day 6, review your PRD**:
- [ ] Problem statement clear?
- [ ] User stories complete?
- [ ] Acceptance criteria defined?
- [ ] Non-functional requirements included?

**What needs updating?**
_______________________________________________________________________
_______________________________________________________________________

### Activity: Refine PRD with AI

**Prompt**:
```
Review and improve this PRD: [your PRD]

Ensure:
- All sections are complete
- User stories are clear and testable
- Acceptance criteria are specific
- Non-functional requirements are included
- Success metrics are defined
- The document is ready for implementation

Provide an improved version.
```

**AI Improvements**:
_______________________________________________________________________
_______________________________________________________________________

**Your finalized PRD**:
- File: `capstone/PRD.md`
- Status: [ ] Finalized

---

## Activity 2: Complete Architecture

### Review Your Week 2 Architecture

**From Day 7, review your architecture**:
- [ ] Components defined?
- [ ] Data model designed?
- [ ] API endpoints planned?
- [ ] Technology stack confirmed?

**What needs updating?**
_______________________________________________________________________
_______________________________________________________________________

### Activity: Finalize Architecture with AI

**Prompt**:
```
Finalize the architecture for this project: [project description]

Based on the PRD: [your PRD]

Create a complete architecture including:
- System architecture diagram (Mermaid)
- Component descriptions
- Database schema (ER diagram)
- API endpoint specifications
- Frontend component structure
- Technology stack with versions
- Deployment architecture

Ensure everything aligns with the PRD.
```

**AI-Generated Architecture**:
_______________________________________________________________________
_______________________________________________________________________

**Your finalized architecture**:
- File: `capstone/Architecture.md`
- Diagrams: `capstone/diagrams/`
- Status: [ ] Complete

---

## Activity 3: Scaffold FastAPI API

### Activity: Generate Project Structure

**Prompt**:
```
Create a complete FastAPI project structure for: [project description]

Structure:
- main.py (app initialization, middleware, routes)
- routers/ (API route handlers)
- models/ (Pydantic models)
- database.py (database connection, session)
- schemas/ (SQLAlchemy models)
- config.py (configuration)
- requirements.txt (all dependencies)
- .env.example (environment variables template)
- README.md (setup and usage)

Follow FastAPI best practices and include:
- CORS configuration
- Error handling middleware
- Logging setup
- Health check endpoint
- API documentation enabled
```

**AI-Generated Structure**:
_______________________________________________________________________
_______________________________________________________________________

**Project structure created?** [ ] Yes

### Activity: Generate Main Application File

**Prompt**:
```
Create the main.py file for this FastAPI application: [project description]

Include:
- FastAPI app initialization
- CORS middleware
- Database session management
- Router registration
- Error handlers
- Logging configuration
- Health check endpoint
- Root endpoint with API info

Use the architecture: [your architecture]
```

**AI-Generated main.py**:
```python
[Paste code]
```

**Review and customize**: [ ] Done

### Activity: Generate Database Configuration

**Prompt**:
```
Create database.py for this FastAPI application.

Requirements:
- SQLAlchemy setup
- Database session management
- Connection pooling
- Database URL from environment
- Support for PostgreSQL (production) and SQLite (development)
- Proper error handling
- Session dependency for FastAPI
```

**AI-Generated database.py**:
```python
[Paste code]
```

**Database config created?** [ ] Yes

---

## Activity 4: Generate Database Schema

### Activity: Design Schema with AI

**Prompt**:
```
Design a database schema for: [project description]

Based on requirements: [your PRD requirements]

Include:
- All necessary tables
- Relationships between tables
- Primary and foreign keys
- Indexes for performance
- Constraints (unique, not null, etc.)
- Data types appropriate for each field

Create:
1. ER diagram (Mermaid)
2. SQLAlchemy models
3. Migration-ready schema
```

**AI-Generated Schema**:
_______________________________________________________________________
_______________________________________________________________________

**ER Diagram**:
```mermaid
[Paste Mermaid ER diagram]
```

### Activity: Generate SQLAlchemy Models

**Prompt**:
```
Create SQLAlchemy models for this schema: [your schema]

Include:
- All tables as SQLAlchemy models
- Proper relationships (one-to-many, many-to-many)
- Indexes where needed
- Timestamps (created_at, updated_at)
- Proper data types
- Docstrings for each model

Follow SQLAlchemy best practices.
```

**AI-Generated Models**:
```python
[Paste models]
```

**Models created?** [ ] Yes  
**File**: `capstone/schemas/models.py`

### Activity: Generate Database Migrations

**Prompt**:
```
Create Alembic migration files for this database schema: [your models]

Include:
- Initial migration (create all tables)
- Proper migration structure
- Rollback support
- Index creation
- Foreign key constraints

Use Alembic best practices.
```

**AI-Generated Migrations**:
_______________________________________________________________________

**Migrations created?** [ ] Yes

**Test migrations**:
```bash
# Initialize Alembic (if not done)
alembic init migrations

# Create migration
alembic revision --autogenerate -m "Initial schema"

# Apply migration
alembic upgrade head
```

**Migrations working?** [ ] Yes

---

## Activity 5: Generate API Endpoints

### Activity: Create Endpoints from User Stories

**From your PRD, select 3-5 key user stories**:

1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________

**For each, generate endpoint**:

**Prompt template**:
```
Create a FastAPI endpoint for: [user story]

Acceptance criteria:
- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

Use:
- Appropriate HTTP method
- Request/response models (Pydantic)
- Database models (SQLAlchemy)
- Error handling
- Input validation
- Documentation

Follow RESTful conventions.
```

**Endpoint 1**: _______________________________________________________________________
**Code**:
```python
[Paste code]
```

**Endpoint 2**: _______________________________________________________________________
**Code**:
```python
[Paste code]
```

**Continue for all endpoints...**

**All endpoints created?** [ ] Yes

---

## Activity 6: Set Up Project Configuration

### Activity: Generate Configuration

**Prompt**:
```
Create a config.py for this FastAPI application.

Include:
- Environment variable loading (python-dotenv)
- Database configuration
- API settings
- Security settings (secret keys, etc.)
- Logging configuration
- Development vs production settings

Use pydantic-settings for configuration management.
```

**AI-Generated config.py**:
```python
[Paste code]
```

**Config created?** [ ] Yes

### Activity: Create Requirements File

**Prompt**:
```
Create a comprehensive requirements.txt for this FastAPI project.

Include:
- FastAPI and uvicorn
- SQLAlchemy and Alembic
- Database drivers (psycopg2, sqlite)
- Pydantic and pydantic-settings
- Testing (pytest, pytest-cov, httpx)
- Code quality (black, flake8, mypy)
- Other dependencies from your project

Include version pins for stability.
```

**AI-Generated requirements.txt**:
_______________________________________________________________________

**Requirements file created?** [ ] Yes

**Install dependencies**:
```bash
pip install -r requirements.txt
```

**Dependencies installed?** [ ] Yes

---

## Activity 7: Test Your Scaffold

### Activity: Verify Setup

**Test 1: Start the server**
```bash
uvicorn main:app --reload
```

**Server starts?** [ ] Yes  
**Issues**: _______________________________________________________________________

**Test 2: Check API docs**
- Visit: http://localhost:8000/docs
- Can you see your endpoints? [ ] Yes

**Test 3: Test health check**
- Visit: http://localhost:8000/health
- Returns 200? [ ] Yes

**Test 4: Database connection**
- Can you connect to database? [ ] Yes
- Tables created? [ ] Yes

**All tests passing?** [ ] Yes

---

## Activity 8: Create Deliverables

### Deliverable Checklist

- [ ] **Finalized PRD** (`capstone/PRD.md`)
- [ ] **Complete Architecture** (`capstone/Architecture.md`)
- [ ] **API Scaffold** (main.py, routers, models)
- [ ] **Database Schema** (SQLAlchemy models)
- [ ] **Migrations** (Alembic migrations)
- [ ] **API Endpoints** (3-5 key endpoints)
- [ ] **Configuration** (config.py, requirements.txt)
- [ ] **Project runs** (server starts, database connects)
- [ ] **AI Usage Log** (`capstone/day13/AI-Usage-Log.md`)

### AI Usage Log

**Document all prompts used today**:
- PRD refinement prompts
- Architecture finalization prompts
- Scaffolding prompts
- Schema generation prompts
- Endpoint generation prompts
- What worked well
- What needed adjustment

**AI Usage Log created?** [ ] Yes

---

## Day 13 Milestone Checklist

**Per Capstone Rubric**:
- [ ] PRD finalized
- [ ] Architecture complete
- [ ] API scaffolded
- [ ] Database schema created
- [ ] Migrations working
- [ ] Basic endpoints functional
- [ ] Project structure organized
- [ ] All AI usage documented

---

## Reflection Questions

1. **How did AI help you scaffold the project faster?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What was most challenging about Day 13?**
   _______________________________________________________________________

3. **Is your architecture ready for Day 14?**
   _______________________________________________________________________

4. **What do you need to focus on tomorrow?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Solid foundation is critical
- ✅ AI accelerates scaffolding
- ✅ Architecture guides everything
- ✅ Database schema is foundational
- ✅ Test as you build

**Tomorrow (Day 14)**:
- Implement tests
- Security review
- SQL optimization
- Build core UI

**Great progress! Keep going!** 🚀

---

## Next Steps

**Before Day 14**:
- [ ] Review your architecture
- [ ] Ensure API is running
- [ ] Database is set up
- [ ] Have your PRD handy
- [ ] Get a good night's sleep!

**See you tomorrow for Day 14!** 💪

