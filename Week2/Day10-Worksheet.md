# Week 2, Day 10 Worksheet: Deployment & Maintenance

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: CI/CD automation, monitoring, incident management, runbooks with AI

---

## Learning Objectives

By the end of Day 10, you will be able to:
- Create CI/CD workflows using prompts
- Use LLMs for monitoring and observability tasks
- Generate runbooks and postmortems with AI
- Set up automated testing in CI
- Create incident response templates
- **Apply prompt engineering tailored to the deployment/maintenance phase of the SDLC** (Learning Objective)

---

## Pre-Activity: Why Automation Matters

**CI/CD benefits**:
- Catch bugs early
- Deploy consistently
- Save time
- Reduce human error
- Enable rapid iteration

**Think about**:
- What happens if you deploy manually and forget a step?
- How do you know if a deployment broke something?
- What if you need to deploy at 2 AM?

**Your thoughts on automation**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Understanding CI/CD

### CI/CD Concepts

**CI (Continuous Integration)**:
- Automatically test code on every commit
- Catch issues early
- Ensure code quality

**CD (Continuous Deployment/Delivery)**:
- Automatically deploy when tests pass
- Consistent deployments
- Fast feedback

### GitHub Actions Basics

**Workflow file**: `.github/workflows/ci.yml`

**Basic structure**:
```yaml
name: CI
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'
      - name: Install dependencies
        run: pip install -r requirements.txt
      - name: Run tests
        run: pytest
```

---

## Activity 2: Generate CI Workflow with AI

### Activity: Create CI Workflow

**Prompt**:
```
Create a GitHub Actions CI workflow for a Python FastAPI project.

Requirements:
- Run on Python 3.11
- Install dependencies from requirements.txt
- Run pytest with coverage
- Check code formatting (black, flake8)
- Run on push and pull requests
- Fail if tests fail or coverage is below 70%

Include proper error handling and clear step names.
```

**AI-Generated Workflow**:
```yaml
[Paste workflow YAML]
```

**Review**:
- [ ] Python version correct?
- [ ] Dependencies installed?
- [ ] Tests run?
- [ ] Coverage checked?
- [ ] Triggers correct?

**Your customized workflow**:
_______________________________________________________________________

### Activity: Add More CI Steps

**Prompt**:
```
Enhance this CI workflow: [your workflow]

Add:
- Security scanning (dependabot or similar)
- Linting checks
- Type checking (mypy)
- Build verification
- Artifact upload (test results)
```

**Enhanced workflow**:
```yaml
[Paste enhanced workflow]
```

---

## Activity 3: Set Up CI Workflow

### Activity: Create Workflow File

**Step 1: Create Directory**
```bash
mkdir -p .github/workflows
```

**Step 2: Create Workflow File**

**File**: `.github/workflows/ci.yml`

**Paste your AI-generated workflow**

**File created?** [ ] Yes

**Step 3: Test Workflow**

**Commit and push**:
```bash
git add .github/workflows/ci.yml
git commit -m "Add CI workflow"
git push
```

**Check GitHub Actions**:
- Go to your repository
- Click "Actions" tab
- Watch workflow run

**Workflow status**: [ ] Passing [ ] Failing

**If failing, fix with AI help**:
- Issue: _______________________________________________________________________
- AI prompt: _______________________________________________________________________
- Solution: _______________________________________________________________________

---

## Activity 4: CD (Deployment) Workflow

### Activity: Generate Deployment Workflow

**Prompt**:
```
Create a GitHub Actions deployment workflow for a FastAPI app.

Requirements:
- Deploy only when tests pass
- Deploy only from main branch
- Use environment secrets for credentials
- Deploy to [platform: Heroku/Railway/Render/etc.]
- Run database migrations
- Health check after deployment
- Rollback on failure

Include proper error handling.
```

**Your deployment target**: _______________________________________________________________________

**AI-Generated Deployment Workflow**:
```yaml
[Paste workflow]
```

**Note**: You may not actually deploy today, but create the workflow

**Workflow created?** [ ] Yes

---

## Activity 5: Monitoring and Observability

### Understanding Observability

**Three pillars**:
- **Logs**: What happened?
- **Metrics**: How is the system performing?
- **Traces**: How did a request flow through the system?

### Activity: Generate Logging Strategy

**Prompt**:
```
Design a logging strategy for a FastAPI application.

Include:
- What to log (requests, errors, important events)
- Log levels (DEBUG, INFO, WARNING, ERROR)
- Log format (structured JSON)
- Where to log (stdout, files, external service)
- Best practices for production logging
```

**AI-Generated Logging Strategy**:
_______________________________________________________________________
_______________________________________________________________________

### Activity: Add Logging to Your App

**Prompt**:
```
Add structured logging to this FastAPI application: [your app]

Use Python's logging module.
Log:
- All HTTP requests (method, path, status, duration)
- Errors with stack traces
- Important business events
- Use appropriate log levels

Include a logging configuration.
```

**AI-Generated Logging Code**:
```python
[Paste logging code]
```

**Added to your app?** [ ] Yes

---

## Activity 6: Incident Management with AI

### Understanding Incidents

**Incident** = Something is broken or degraded

**Incident response**:
1. Detect the problem
2. Assess impact
3. Mitigate/restore service
4. Document what happened
5. Learn and improve

### Activity: Generate Incident Summary Template

**Prompt**:
```
Create an incident summary template for documenting production issues.

Include sections for:
- Incident title and severity
- Timeline (detection, response, resolution)
- Impact (users affected, services down)
- Root cause analysis
- Resolution steps
- Prevention measures
- Lessons learned

Format as a markdown template.
```

**AI-Generated Template**:
```markdown
[Paste template]
```

**Template created?** [ ] Yes  
**File**: `docs/incident-template.md`

### Activity: Generate Runbook Template

**Prompt**:
```
Create a runbook template for common operational tasks.

Include:
- Task description
- Prerequisites
- Step-by-step instructions
- Verification steps
- Rollback procedures
- Common issues and solutions
- Contact information

Format as a structured markdown document.
```

**AI-Generated Runbook Template**:
```markdown
[Paste template]
```

**Template created?** [ ] Yes  
**File**: `docs/runbook-template.md`

### Activity: Generate Specific Runbook

**Prompt**:
```
Create a detailed runbook for: [specific task]

Examples:
- Deploying the application
- Rolling back a deployment
- Restarting the database
- Clearing cache
- Scaling the application

Include all necessary steps, commands, and verification.
```

**Your task**: _______________________________________________________________________

**AI-Generated Runbook**:
```markdown
[Paste runbook]
```

**Runbook created?** [ ] Yes

---

## Activity 7: Incident Summarization with AI

### Activity: Summarize a Hypothetical Incident

**Scenario**: Your API was down for 30 minutes due to a database connection issue

**Prompt**:
```
Summarize this incident for a postmortem report:

Incident: API downtime
Duration: 30 minutes
Time: 2:00 AM - 2:30 AM
Impact: All API endpoints unavailable, 500 users affected
Root cause: Database connection pool exhausted
Resolution: Restarted application, increased connection pool size
Detection: Monitoring alerts triggered

Create a professional incident summary following SRE best practices.
```

**AI-Generated Summary**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Review**: Does it capture the key information?

---

## Activity 8: Create Operational Documentation

### Organize Your Docs

**Create structure**:
```
docs/
├── runbooks/
│   ├── deployment.md
│   ├── rollback.md
│   └── common-tasks.md
├── incidents/
│   └── incident-template.md
└── monitoring.md
```

**All docs created?** [ ] Yes

---

## Activity 9: Create Deliverables

### Deliverable 1: CI Workflow

**File**: `.github/workflows/ci.yml`

**Workflow includes**:
- [ ] Python setup
- [ ] Dependency installation
- [ ] Test execution
- [ ] Coverage checking
- [ ] Linting/formatting
- [ ] Runs on push/PR

**CI workflow created?** [ ] Yes  
**CI passing?** [ ] Yes

### Deliverable 2: Incident Summary Template

**File**: `docs/incident-template.md`

**Template created?** [ ] Yes

### Deliverable 3: Runbook Template

**File**: `docs/runbook-template.md`

**Template created?** [ ] Yes

### Deliverable 4: AI Usage Log

**File**: `week2/day10/AI-Usage-Log.md`

**Document**:
- CI workflow generation prompts
- Deployment workflow prompts
- Logging strategy prompts
- Incident template prompts
- Runbook generation prompts
- What worked well

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Created CI workflow with AI
- [ ] CI workflow tested and passing
- [ ] Created deployment workflow (even if not deployed)
- [ ] Designed logging strategy
- [ ] Added logging to application
- [ ] Created incident summary template
- [ ] Created runbook template
- [ ] Generated at least one specific runbook
- [ ] Documented all AI usage
- [ ] Committed to repository
- [ ] Created PR with CI workflow and docs

---

## Reflection Questions

1. **How did AI help you create CI/CD workflows?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What operational tasks would benefit from runbooks?**
   _______________________________________________________________________

3. **Why is automation important for software projects?**
   _______________________________________________________________________

4. **How will you use AI for operational tasks in the future?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ CI catches issues early
- ✅ Automation saves time and reduces errors
- ✅ Runbooks make operations repeatable
- ✅ Incident documentation helps prevent future issues
- ✅ Monitoring is essential for production
- ✅ AI can help generate all of this!

**Best practices**:
- Test your CI workflows
- Document operational procedures
- Learn from incidents
- Automate repetitive tasks
- Monitor what matters

---

## Additional Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Google SRE: Postmortem Culture](https://sre.google/sre-book/postmortem-culture/)
- [Incident.io Templates](https://incident.io/templates)
- [FastAPI Deployment](https://fastapi.tiangolo.com/deployment/)

---

## Next Steps

**Week 2 Complete!** 🎉

Next week (Week 3), you'll dive deeper into:
- Advanced code generation techniques
- External tools integration
- Your capstone project

**Make sure you**:
- Have all Week 2 deliverables complete
- CI is working
- Documentation is in place
- Ready for Week 3!

**Congratulations on completing Week 2!** 🚀

