# Week 2, Day 8 Worksheet: Development & Coding

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: AI pair programming, FastAPI scaffold, Ask/Edit/Agent modes, refactoring with AI

---

## Learning Objectives

By the end of Day 8, you will be able to:
- Use AI pair programming tools effectively (Copilot, Cursor, Cody)
- **Integrate GitHub Copilot into development environments to improve speed and accuracy** (Learning Objective)
- Understand and use Ask/Edit/Agent modes appropriately
- Generate API scaffolds with AI assistance
- Refactor code using AI tools
- Generate documentation (docstrings, READMEs) with AI
- Scope context correctly for different coding tasks
- **Apply prompt engineering tailored to the development phase of the SDLC** (Learning Objective)

---

## Pre-Activity: Understanding AI Pair Programming

**AI pair programming is like**:
- Having a coding partner who never gets tired
- Getting suggestions as you type
- Asking questions and getting code examples
- Getting help with refactoring and debugging

**But remember**:
- You're still the driver—you make decisions
- Always review AI-generated code
- Test everything, even AI suggestions
- Understand what the code does

**Your experience with AI coding tools so far**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Understanding Copilot Modes

### Ask Mode (Chat/Conversation)

**When to use**:
- Understanding code
- Getting explanations
- Asking "how do I..." questions
- Getting code examples

**Example prompts**:
- "How do I create a FastAPI endpoint?"
- "Explain what this code does"
- "Show me how to handle errors in FastAPI"

### Edit Mode (Inline Suggestions)

**When to use**:
- Writing new code
- Getting autocomplete suggestions
- Getting function implementations
- Code generation as you type

**How it works**:
- Type a comment or function signature
- AI suggests implementation
- Accept, reject, or modify

### Agent Mode (Autonomous Tasks)

**When to use**:
- Multi-step tasks
- Refactoring across files
- Setting up project structure
- Complex implementations

**How it works**:
- Give high-level task description
- Agent breaks it down and executes
- You review and approve changes

### Activity: Practice Each Mode

**Try Ask Mode**:
- Open Copilot Chat (Ctrl+Shift+I or Cmd+Shift+I)
- Ask: "How do I create a FastAPI app with a GET endpoint?"
- Review the explanation and code

**AI Response**:
_______________________________________________________________________
_______________________________________________________________________

**Try Edit Mode**:
- Create a new file: `test_endpoint.py`
- Type: `# Create a FastAPI app with a health check endpoint`
- Let AI suggest code
- Accept or modify

**Code generated**:
```python
[Paste code here]
```

**Try Agent Mode** (if available):
- Ask: "Set up a FastAPI project structure with main.py, routers folder, and requirements.txt"
- Review what agent creates

**Agent created**:
_______________________________________________________________________

---

## Activity 2: Scaffold FastAPI Application

### Understanding FastAPI Structure

**Typical structure**:
```
project/
├── main.py          # Application entry point
├── routers/         # API route handlers
├── models/          # Data models
├── database.py      # Database connection
├── requirements.txt # Dependencies
└── README.md        # Documentation
```

### Activity: Generate FastAPI Scaffold

**Step 1: Use AI to Generate Project Structure**

**Prompt** (Ask or Agent mode):
```
Create a FastAPI project structure for a [your project type] application.

Include:
- main.py with FastAPI app initialization
- routers/ folder with example router
- models/ folder for data models
- database.py for database connection
- requirements.txt with FastAPI, uvicorn, sqlalchemy
- README.md with setup instructions

Create the folder structure and basic files.
```

**AI created**:
_______________________________________________________________________

**Step 2: Review Generated Code**

**Check main.py**:
- [ ] FastAPI app created correctly
- [ ] CORS configured (if needed)
- [ ] Basic structure looks good

**Check router example**:
- [ ] Router created correctly
- [ ] Example endpoint included
- [ ] Follows FastAPI patterns

**Your review notes**:
_______________________________________________________________________
_______________________________________________________________________

**Step 3: Customize for Your Project**

**Based on your Day 7 architecture, add**:
- Your specific routers
- Your data models
- Your database setup

**What you added**:
_______________________________________________________________________

---

## Activity 3: Generate API Endpoints with AI

### Activity: Create Endpoints from Requirements

**From your Day 6 PRD, pick a user story**:
_______________________________________________________________________

**Use AI to generate endpoint**:

**Prompt** (Edit or Ask mode):
```
Create a FastAPI endpoint for: [user story description]

Requirements:
- [Acceptance criteria 1]
- [Acceptance criteria 2]
- [Acceptance criteria 3]

Include:
- Proper HTTP method and path
- Request/response models
- Error handling
- Input validation
- Docstring documentation
```

**Your prompt**:
_______________________________________________________________________

**AI-Generated Endpoint**:
```python
[Paste code here]
```

**Review the code**:
- [ ] HTTP method correct?
- [ ] Path makes sense?
- [ ] Validation included?
- [ ] Error handling present?
- [ ] Documentation clear?

**Refinements needed**:
_______________________________________________________________________

### Activity: Generate Multiple Endpoints

**Create endpoints for 3-5 user stories from your backlog**

**Endpoint 1**: _______________________________________________________________________
**AI code**:
```python
[Paste code]
```

**Endpoint 2**: _______________________________________________________________________
**AI code**:
```python
[Paste code]
```

**Endpoint 3**: _______________________________________________________________________
**AI code**:
```python
[Paste code]
```

---

## Activity 4: Context Scoping for Better Results

### Understanding Context Levels

**Code block context**: Just the function you're working on
**File context**: The entire file
**Multi-file context**: Related files
**Repo-wide context**: Entire codebase

**More context = better AI suggestions**

### Activity: Practice Context Scoping

**Scenario 1: Code Block Context**

**You have**:
```python
def calculate_total(items):
    # TODO: Calculate total with tax
    pass
```

**Prompt**: "Implement this function to calculate total with 10% tax"

**AI suggestion** (with just function context):
_______________________________________________________________________

**Scenario 2: File Context**

**You have a file with**:
- Data models
- Helper functions
- The function you're working on

**Same prompt, but AI sees entire file**:
_______________________________________________________________________

**Which was better?** [ ] Code block [ ] File context

**Why?**
_______________________________________________________________________

### Activity: Use Multi-File Context

**When working on a router, include**:
- The router file
- Related model files
- Database connection file

**Try it**: Generate an endpoint that uses your data models

**Prompt**:
```
[Include context from models.py and database.py]

Create an endpoint that:
- Uses the User model
- Connects to database
- Handles errors properly
```

**Result**:
_______________________________________________________________________

---

## Activity 5: Refactoring with AI

### Understanding Refactoring

**Refactoring** = Improving code without changing functionality

**Common refactoring tasks**:
- Extract functions
- Rename variables
- Simplify logic
- Improve structure
- Add error handling

### Activity: Refactor Code with AI

**Step 1: Find Code to Refactor**

**Take some AI-generated code and improve it**:

**Original code**:
```python
[Paste code that needs refactoring]
```

**Step 2: Ask AI to Refactor**

**Prompt**:
```
Refactor this code to:
- Improve readability
- Add proper error handling
- Follow Python best practices
- Add type hints
- Improve function names

Keep the same functionality.
```

**Refactored code**:
```python
[Paste refactored code]
```

**What improved?**
_______________________________________________________________________

### Activity: Extract Functions

**Prompt**:
```
This function is too long. Break it into smaller, 
well-named functions. Each function should have a 
single responsibility.
```

**Original**:
```python
[Paste long function]
```

**Refactored**:
```python
[Paste refactored functions]
```

---

## Activity 6: Generate Documentation with AI

### Activity: Generate Docstrings

**Prompt**:
```
Add comprehensive docstrings to this function following 
Google or NumPy style:

[Your function code]

Include:
- Description
- Parameters
- Returns
- Raises
- Examples
```

**Function**:
```python
[Your function]
```

**With docstrings**:
```python
[Function with docstrings]
```

### Activity: Generate README

**Prompt**:
```
Create a comprehensive README.md for this FastAPI project:

[Include context about your project]

Include:
- Project description
- Features
- Installation instructions
- Usage examples
- API documentation
- Development setup
- Contributing guidelines
```

**Your project context**:
_______________________________________________________________________

**AI-Generated README**:
_______________________________________________________________________
_______________________________________________________________________

**Review and customize**:
- [ ] Installation steps correct?
- [ ] Examples work?
- [ ] All features documented?

**Your customized README**:
_______________________________________________________________________

### Activity: Generate Commit Messages

**Prompt**:
```
Generate a clear, descriptive commit message for these changes:

[Describe what changed]

Follow conventional commit format:
- Type (feat/fix/docs/style/refactor/test)
- Brief description
- Optional detailed explanation
```

**Your changes**:
_______________________________________________________________________

**AI commit message**:
_______________________________________________________________________

---

## Activity 7: Test Your API

### Activity: Run Your FastAPI App

**Start the server**:
```bash
uvicorn main:app --reload
```

**Test endpoints**:
- [ ] Health check works
- [ ] GET endpoints return data
- [ ] POST endpoints accept data
- [ ] Error handling works

**Issues encountered**:
_______________________________________________________________________

**Fixed with AI help?**
- Prompt used: _______________________________________________________________________
- Solution: _______________________________________________________________________

---

## Activity 8: Create Your Deliverables

### Deliverable 1: Scaffolded API

**Your project structure**:
```
week2/day8/
├── main.py
├── routers/
├── models/
├── database.py
├── requirements.txt
└── README.md
```

**API scaffolded?** [ ] Yes  
**Endpoints created?** [ ] Yes (list count: _____)

### Deliverable 2: README Generated by AI

**File**: `week2/day8/README.md`

**README created?** [ ] Yes  
**Customized?** [ ] Yes

### Deliverable 3: AI Usage Log

**File**: `week2/day8/AI-Usage-Log.md`

**Document**:
- Prompts used for scaffolding
- Prompts for endpoint generation
- Refactoring prompts
- Documentation prompts
- What worked well
- What didn't work

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Understood Ask/Edit/Agent modes
- [ ] Practiced each mode
- [ ] Generated FastAPI project scaffold
- [ ] Created 3-5 API endpoints with AI
- [ ] Practiced context scoping
- [ ] Refactored code with AI
- [ ] Generated docstrings
- [ ] Generated README with AI
- [ ] Tested API endpoints
- [ ] Documented all AI usage
- [ ] Committed to repository
- [ ] Created PR with API scaffold

---

## Reflection Questions

1. **Which AI mode (Ask/Edit/Agent) was most useful for you?**
   _______________________________________________________________________

2. **How did context scoping affect AI suggestions?**
   _______________________________________________________________________

3. **What challenges did you face when using AI for coding?**
   _______________________________________________________________________

4. **How will you use AI pair programming in future projects?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Use Ask mode for learning and explanations
- ✅ Use Edit mode for code generation
- ✅ Use Agent mode for multi-step tasks
- ✅ Provide good context for better results
- ✅ Always review and test AI-generated code
- ✅ Refactor to improve code quality
- ✅ Document your code and AI usage

**Best practices**:
- Start with clear requirements
- Provide relevant context
- Review all AI suggestions
- Test everything
- Iterate and improve

---

## Additional Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [GitHub Skills: Getting Started with Copilot](https://github.com/skills/getting-started-with-github-copilot)
- [Cursor Documentation](https://docs.cursor.com/)
- [FastAPI Tutorial](https://fastapi.tiangolo.com/)
- [FastAPI Best Practices](https://fastapi.tiangolo.com/tutorial/)

---

## Next Steps

Tomorrow (Day 9), you'll work on Testing & Quality Assurance. Make sure you:
- Have your API scaffolded
- Have endpoints to test
- Understand your code structure
- Are ready to generate tests with AI

**Great coding work!** 💻

