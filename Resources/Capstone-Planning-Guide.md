# Capstone Planning Guide

A comprehensive guide to planning and scoping your 3-day capstone project.

## Timeline Overview

### Day 13: Planning & Setup
- Finalize PRD and architecture
- Scaffold API and database
- Set up project structure

### Day 14: Core Development
- Implement core features
- Write tests
- Security review
- Build UI

### Day 15: Polish & Deploy
- CI/CD setup
- Documentation
- Demo preparation
- Presentation

---

## Feature Prioritization Framework

### Must-Have (MVP)
Features without which the app doesn't work:
- [ ] User authentication (login/register)
- [ ] Core CRUD operations
- [ ] Basic UI to interact with API
- [ ] Database schema and migrations
- [ ] Basic error handling

### Should-Have
Features that significantly improve the app:
- [ ] Input validation
- [ ] Search/filter functionality
- [ ] Basic styling
- [ ] Error messages
- [ ] Loading states

### Nice-to-Have
Features that enhance but aren't critical:
- [ ] Advanced filtering
- [ ] Pagination
- [ ] Rich UI components
- [ ] Analytics
- [ ] Export functionality

### Won't-Have (This Time)
Features explicitly out of scope:
- [ ] Real-time updates
- [ ] File uploads
- [ ] Email notifications
- [ ] Mobile app
- [ ] Advanced analytics

---

## MVP vs. Full Feature Set

### MVP Approach (Recommended)
**Goal**: Working application with core features

**Benefits**:
- Achievable in 3 days
- Demonstrates all key concepts
- Can be extended later
- Less stress, more learning

**Example MVP for Task Manager**:
- ✅ Create, read, update, delete tasks
- ✅ Mark tasks complete
- ✅ User authentication
- ✅ Basic UI
- ❌ Categories (nice-to-have)
- ❌ Due dates (nice-to-have)
- ❌ Sharing (nice-to-have)

### Full Feature Set (Advanced)
**Goal**: Complete application with all features

**Risks**:
- May not finish in time
- Quality may suffer
- More stress
- Less time for polish

**Only attempt if**:
- You have strong prior experience
- You're comfortable with the tech stack
- You can work efficiently with AI tools

---

## Scoping Your Project

### Step 1: Define Core Value
**Question**: What's the one thing your app does?

**Example**: "A task manager that helps users track their to-dos"

### Step 2: Identify Core Entities
**Question**: What are the main data objects?

**Example**:
- User (authentication)
- Task (core entity)

### Step 3: Define Core Actions
**Question**: What can users do?

**Example**:
- Create a task
- View all tasks
- Update a task
- Delete a task
- Mark task complete

### Step 4: Identify Relationships
**Question**: How do entities relate?

**Example**:
- User has many Tasks
- Task belongs to one User

### Step 5: Scope to MVP
**Question**: What's the minimum to demonstrate value?

**Answer**: Core actions on core entities with authentication

---

## Time Allocation Guide

### Day 13 (8 hours)
- **Planning** (2 hours): PRD, architecture, database design
- **Setup** (2 hours): Project structure, dependencies, database
- **Backend Scaffold** (3 hours): Models, schemas, basic endpoints
- **Documentation** (1 hour): Initial README, API docs

### Day 14 (8 hours)
- **Backend Completion** (3 hours): All endpoints, error handling
- **Testing** (2 hours): Unit tests, integration tests
- **Frontend** (2 hours): Core UI, API integration
- **Security** (1 hour): Security review, fixes

### Day 15 (8 hours)
- **Frontend Polish** (2 hours): Styling, error handling
- **CI/CD** (2 hours): GitHub Actions, deployment prep
- **Documentation** (2 hours): Complete README, API docs
- **Demo Prep** (2 hours): Rehearse, prepare slides

---

## Common Scoping Mistakes

### ❌ Too Ambitious
**Problem**: Trying to build too much

**Solution**: Focus on MVP, add features only if time allows

### ❌ Too Vague
**Problem**: "I'll build a social network"

**Solution**: Be specific: "A simple post-sharing app with comments"

### ❌ Ignoring Constraints
**Problem**: Planning features that need external services

**Solution**: Stick to what you can build with your stack

### ❌ Perfectionism
**Problem**: Spending too much time on one feature

**Solution**: Get it working, then improve

---

## Using AI for Planning

### Generate PRD
```
I need to build a [project type] for [target users].

Help me create a PRD with:
1. Problem statement
2. User stories
3. Acceptance criteria
4. Technical requirements
5. Success metrics

Scope for a 3-day MVP.
```

### Generate Architecture
```
Design the architecture for [project description].

Include:
- System components
- Database schema
- API endpoints
- Technology choices
- Deployment strategy

Keep it simple and achievable in 3 days.
```

### Generate Backlog
```
Create a prioritized backlog for [project].

Break down into:
- Must-have features (MVP)
- Should-have features
- Nice-to-have features

Estimate effort for each.
```

---

## Project Selection Worksheet

### 1. Project Idea
**Name**: _________________________________

**One-sentence description**: _________________________________

### 2. Core Entities
- _________________________________
- _________________________________
- _________________________________

### 3. Core Actions
- _________________________________
- _________________________________
- _________________________________

### 4. MVP Features
- [ ] _________________________________
- [ ] _________________________________
- [ ] _________________________________

### 5. Out of Scope
- _________________________________
- _________________________________

### 6. Success Criteria
- [ ] Working authentication
- [ ] Core CRUD operations
- [ ] Functional UI
- [ ] Tests written
- [ ] Deployed (or deployable)

---

## Final Checklist

Before starting development:

- [ ] PRD finalized and approved
- [ ] Architecture designed
- [ ] Database schema defined
- [ ] API endpoints planned
- [ ] MVP features identified
- [ ] Timeline realistic
- [ ] Tools and access ready
- [ ] Project repository created

---

## Remember

1. **MVP first**: Get something working, then enhance
2. **Use AI strategically**: Let AI handle boilerplate, you handle logic
3. **Test as you go**: Don't leave testing until the end
4. **Document continuously**: Use AI to generate docs
5. **Stay focused**: Resist feature creep
6. **Ask for help**: Use AI, instructors, peers

Good luck with your capstone! 🚀

