# Week 3, Day 15 Worksheet: Capstone Day 3

**Estimated Time**: 6–8 hours  
**Focus**: Wire CI/CD, polish documentation, rehearse and deliver demo

---

## Learning Objectives

By the end of Day 15, you will be able to:
- Set up complete CI/CD pipeline
- Create comprehensive documentation
- Prepare and deliver a professional demo
- Showcase GenAI usage across the SDLC
- Complete your capstone project
- **Build and present a working prototype demonstrating GenAI‑enhanced workflows** (Learning Objective)

---

## Pre-Activity: Final Day Overview

**Today's goals**:
- ✅ Complete CI/CD pipeline
- ✅ Polish all documentation
- ✅ Create AI usage log
- ✅ Rehearse demo
- ✅ Deliver presentation

**Your project status**:
- API complete? [ ] Yes
- Database working? [ ] Yes
- Tests passing? [ ] Yes
- UI functional? [ ] Yes
- Security reviewed? [ ] Yes

**Let's finish strong!** 💪

---

## Activity 1: Wire CI/CD

### Activity: Complete CI Workflow

**Review your Day 10 CI workflow**:
- [ ] Tests run on push/PR
- [ ] Coverage checked
- [ ] Linting/formatting checked
- [ ] All checks passing

**Enhance if needed**:

**Prompt**:
```
Enhance this CI workflow: [your workflow]

Add:
- Frontend build and test (if applicable)
- Security scanning (dependabot, codeql)
- Multiple Python versions testing
- Database migration testing
- Artifact uploads
- Notifications on failure

Ensure comprehensive coverage.
```

**Enhanced CI workflow**:
```yaml
[Paste workflow]
```

**CI workflow complete?** [ ] Yes

### Activity: Set Up CD (Deployment)

**Prompt**:
```
Create a complete deployment workflow for this full-stack application.

Stack:
- Backend: FastAPI on [platform]
- Frontend: React on [platform]
- Database: [PostgreSQL/SQLite]

Include:
- Deploy only on main branch
- Run tests before deployment
- Database migrations
- Environment variable setup
- Health checks
- Rollback capability
- Deployment notifications
```

**AI-Generated Deployment Workflow**:
```yaml
[Paste workflow]
```

**Deployment workflow created?** [ ] Yes

**Note**: You may not actually deploy, but the workflow should be ready

### Activity: Test CI/CD

**Test CI**:
- [ ] Push code triggers CI
- [ ] All tests run
- [ ] Coverage checked
- [ ] Linting passes
- [ ] CI passes

**CI working?** [ ] Yes

---

## Activity 2: Polish Documentation

### Activity: Complete README

**Prompt**:
```
Create a comprehensive README.md for this full-stack project: [project description]

Include:
- Project overview and purpose
- Features list
- Technology stack
- Architecture overview
- Installation instructions (backend and frontend)
- Configuration (environment variables)
- Running the application
- API documentation
- Testing instructions
- Deployment guide
- Contributing guidelines
- License
- Contact information

Make it professional and complete.
```

**AI-Generated README**:
_______________________________________________________________________
_______________________________________________________________________

**Review and customize**:
- [ ] All sections complete
- [ ] Instructions accurate
- [ ] Examples work
- [ ] Professional tone

**README finalized?** [ ] Yes

### Activity: Create API Documentation

**Prompt**:
```
Create comprehensive API documentation for these endpoints: [list endpoints]

Include:
- Endpoint descriptions
- Request/response examples
- Authentication requirements
- Error responses
- Rate limits (if applicable)
- Code examples (curl, Python, JavaScript)

Format as markdown with clear sections.
```

**AI-Generated API Docs**:
_______________________________________________________________________

**API documentation created?** [ ] Yes  
**File**: `docs/API.md`

### Activity: Create Architecture Documentation

**Enhance your Day 7 architecture doc**:

**Prompt**:
```
Enhance this architecture document: [your architecture]

Add:
- Deployment architecture diagram
- Data flow diagrams
- Security architecture
- Scaling considerations
- Monitoring and logging strategy
- Disaster recovery plan

Make it production-ready documentation.
```

**Enhanced architecture doc**:
_______________________________________________________________________

**Architecture doc complete?** [ ] Yes

### Activity: Create User Guide

**Prompt**:
```
Create a user guide for this application: [application description]

Include:
- Getting started
- Key features walkthrough
- Common tasks
- Troubleshooting
- FAQ

Make it user-friendly with screenshots/examples.
```

**AI-Generated User Guide**:
_______________________________________________________________________

**User guide created?** [ ] Yes  
**File**: `docs/User-Guide.md`

---

## Activity 3: Create AI Usage Log

### Activity: Comprehensive AI Usage Documentation

**This is critical for the rubric!**

**Prompt**:
```
Create a comprehensive AI usage log for this entire capstone project.

Document:
- All prompts used across the SDLC
- AI tools used (Copilot, ChatGPT, Claude, etc.)
- How AI helped in each phase:
  * Planning & Requirements
  * Design & Architecture
  * Development & Coding
  * Testing & QA
  * Deployment & Maintenance
- Code generated by AI (with attribution)
- Prompts that worked well
- Prompts that needed iteration
- Lessons learned
- Best practices discovered

Format as a detailed markdown document with sections for each SDLC phase.
```

**AI-Generated Log Structure**:
_______________________________________________________________________

**Now fill it in with your actual usage**:

**File**: `docs/AI-Usage-Log.md`

**Sections to include**:

1. **Planning & Requirements (Day 6)**
   - Prompts used: _______________________________________________________________________
   - Tools: _______________________________________________________________________
   - Impact: _______________________________________________________________________

2. **Design & Architecture (Day 7)**
   - Prompts used: _______________________________________________________________________
   - Tools: _______________________________________________________________________
   - Impact: _______________________________________________________________________

3. **Development (Days 8, 11, 13)**
   - Prompts used: _______________________________________________________________________
   - Tools: _______________________________________________________________________
   - Impact: _______________________________________________________________________

4. **Testing (Days 9, 14)**
   - Prompts used: _______________________________________________________________________
   - Tools: _______________________________________________________________________
   - Impact: _______________________________________________________________________

5. **Deployment (Days 10, 15)**
   - Prompts used: _______________________________________________________________________
   - Tools: _______________________________________________________________________
   - Impact: _______________________________________________________________________

**AI Usage Log complete?** [ ] Yes

---

## Activity 4: Prepare Demo

### Activity: Create Demo Script

**Prompt**:
```
Create a demo script for presenting this application: [application description]

Include:
- Introduction (30 seconds)
- Problem statement (1 minute)
- Solution overview (1 minute)
- Live demo walkthrough (3-4 minutes)
  * Key features
  * User workflows
  * Technical highlights
- GenAI usage showcase (2 minutes)
  * How AI helped
  * Key prompts used
  * Results achieved
- Conclusion (30 seconds)

Total: 8-10 minutes

Make it engaging and clear.
```

**AI-Generated Demo Script**:
_______________________________________________________________________
_______________________________________________________________________

**Your customized script**:
_______________________________________________________________________

**Demo script created?** [ ] Yes

### Activity: Prepare Demo Environment

**Checklist**:
- [ ] Application running locally
- [ ] Database populated with sample data
- [ ] All features working
- [ ] No bugs visible
- [ ] Browser bookmarks ready
- [ ] Screen sharing tested
- [ ] Backup plan if demo fails

**Demo environment ready?** [ ] Yes

### Activity: Create Demo Slides (Optional)

**If creating slides**:

**Prompt**:
```
Create presentation slides for this capstone project demo.

Include:
- Title slide
- Problem statement
- Solution overview
- Architecture diagram
- Key features
- GenAI usage highlights
- Demo walkthrough
- Results and metrics
- Lessons learned
- Q&A

Keep slides minimal and visual.
```

**Slides created?** [ ] Yes

---

## Activity 5: Rehearse Demo

### Activity: Practice Run

**Run through your demo**:
- [ ] Timing (8-10 minutes)
- [ ] All features work
- [ ] Transitions smooth
- [ ] Key points covered
- [ ] GenAI usage explained

**Practice run completed?** [ ] Yes

**Timing**: _____ minutes

**Adjustments needed**:
_______________________________________________________________________

### Activity: Prepare for Questions

**Anticipate questions**:

**Common questions**:
1. "How did AI help you build this?"
2. "What was most challenging?"
3. "What would you do differently?"
4. "How would you scale this?"
5. "What security measures did you implement?"

**Prepare answers**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________

---

## Activity 6: Final Project Review

### Activity: Rubric Self-Assessment

**Review capstone rubric**:

**Functionality and correctness (25%)**:
- [ ] All features work
- [ ] No critical bugs
- [ ] API endpoints functional
- [ ] Frontend-backend integrated
- **Self-score**: _____/25

**Effective GenAI usage (20%)**:
- [ ] Prompts documented
- [ ] AI usage across SDLC
- [ ] Quality prompts used
- [ ] Context properly scoped
- **Self-score**: _____/20

**Code quality (15%)**:
- [ ] Readable code
- [ ] Good structure
- [ ] Type hints
- [ ] Documentation
- **Self-score**: _____/15

**Test quality (15%)**:
- [ ] 80%+ coverage
- [ ] Tests pass
- [ ] Edge cases covered
- [ ] Integration tests
- **Self-score**: _____/15

**Security (10%)**:
- [ ] Vulnerabilities addressed
- [ ] Best practices followed
- [ ] Security documented
- **Self-score**: _____/10

**Performance (5%)**:
- [ ] SQL optimized
- [ ] Indexes created
- [ ] Performance documented
- **Self-score**: _____/5

**Documentation (10%)**:
- [ ] README complete
- [ ] API docs complete
- [ ] Architecture documented
- [ ] AI usage logged
- **Self-score**: _____/10

**Total self-score**: _____/100

**Target**: 70%+ (70/100)

**Target met?** [ ] Yes

---

## Activity 7: Final Deliverables

### Complete Deliverable Checklist

**Repository Structure**:
```
capstone/
├── README.md
├── requirements.txt
├── main.py
├── routers/
├── models/
├── schemas/
├── tests/
├── frontend/
├── .github/workflows/
│   ├── ci.yml
│   └── deploy.yml
├── docs/
│   ├── PRD.md
│   ├── Architecture.md
│   ├── API.md
│   ├── User-Guide.md
│   └── AI-Usage-Log.md
└── capstone/
    ├── day13/
    ├── day14/
    └── day15/
```

**All files present?** [ ] Yes

### Final Commit

**Commit everything**:
```bash
git add .
git commit -m "Complete capstone project"
git push
```

**Everything committed?** [ ] Yes

### Create Final PR

**PR should include**:
- [ ] All code
- [ ] All documentation
- [ ] AI usage log
- [ ] CI passing
- [ ] Clear description

**Final PR created?** [ ] Yes

---

## Activity 8: Deliver Demo

### During Demo

**Follow your script**:
- [ ] Introduction clear
- [ ] Problem explained
- [ ] Solution demonstrated
- [ ] GenAI usage highlighted
- [ ] Questions answered
- [ ] Professional presentation

**Demo delivered?** [ ] Yes

**How did it go?**
_______________________________________________________________________

---

## Final Reflection

### Course Reflection

**Answer these questions**:

1. **What was your biggest learning from this course?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **How has your approach to software development changed?**
   _______________________________________________________________________

3. **What GenAI techniques will you use going forward?**
   _______________________________________________________________________

4. **What would you do differently if starting over?**
   _______________________________________________________________________

5. **What are you most proud of in your capstone?**
   _______________________________________________________________________

---

## Congratulations! 🎉

**You've completed**:
- ✅ Week 0: Foundations
- ✅ Week 1: Assessments
- ✅ Week 2: SDLC with GenAI
- ✅ Week 3: Advanced topics & Capstone

**You've learned**:
- ✅ How to use GenAI across the SDLC
- ✅ Prompt engineering for software engineering
- ✅ AI pair programming
- ✅ Testing AI-generated code
- ✅ Building full-stack applications
- ✅ Professional software development practices

**You've built**:
- ✅ A complete full-stack application
- ✅ Comprehensive test suite
- ✅ CI/CD pipeline
- ✅ Complete documentation
- ✅ Professional demo

**You're now ready to**:
- Apply GenAI in your work
- Build software faster and better
- Use AI tools effectively
- Continue learning and growing

---

## Final Checklist

- [ ] CI/CD complete and working
- [ ] All documentation polished
- [ ] AI usage log comprehensive
- [ ] Demo script prepared
- [ ] Demo rehearsed
- [ ] Demo delivered
- [ ] Final PR created
- [ ] Repository complete
- [ ] Self-assessment done
- [ ] Reflection completed

---

## Next Steps

**After the course**:
- Continue practicing with AI tools
- Build more projects
- Share your learnings
- Help others learn
- Stay updated on AI developments

**Resources to continue learning**:
- GitHub Copilot updates
- New AI coding tools
- Prompt engineering techniques
- Software engineering best practices

---

## Thank You!

**You've worked hard and accomplished a lot!**

**Remember**:
- AI is a tool—you're the engineer
- Keep learning and experimenting
- Build things that matter
- Share your knowledge

**Good luck with your future projects!** 🚀

**Congratulations on completing the AI-Enabled Software Engineering course!** 🎓

