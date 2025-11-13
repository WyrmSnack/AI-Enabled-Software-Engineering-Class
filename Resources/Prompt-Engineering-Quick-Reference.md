# Prompt Engineering Quick Reference

## Core Principles

### 1. Be Specific
❌ **Bad**: "Write code"  
✅ **Good**: "Write a Python function that takes a list of numbers and returns the sum"

### 2. Provide Context
❌ **Bad**: "Create an endpoint"  
✅ **Good**: "Create a FastAPI GET endpoint at /users/{id} that retrieves a user from the database and returns JSON"

### 3. Use Examples
❌ **Bad**: "Make it better"  
✅ **Good**: "Refactor this code following the same pattern as [example code]"

### 4. Iterate and Refine
- Start broad, then narrow
- Build on previous responses
- Ask for specific improvements

---

## Prompt Patterns by SDLC Phase

### Planning & Requirements

**Requirements Elicitation**:
```
I need to build a system for [problem]. Help me identify:
1. Who are the users?
2. What are their main goals?
3. What problems does this solve?
4. What are the key features needed?
```

**User Story Generation**:
```
Based on these requirements: [requirements]
Generate user stories in format: "As a [user], I want [goal] so that [benefit]"
Include 5-10 stories with different user types.
```

### Design & Architecture

**Architecture Design**:
```
Design a system architecture for: [problem]
Tech stack: [stack]
Requirements: [requirements]
Include: components, data flow, technology choices, trade-offs
```

**Diagram Generation**:
```
Create a Mermaid [diagram type] showing: [what to show]
Include: [key elements]
Output as Mermaid code.
```

### Development

**Code Generation**:
```
Write a [language] function that [does what]
Requirements:
- [Requirement 1]
- [Requirement 2]
Include: error handling, type hints, docstrings
```

**Refactoring**:
```
Refactor this code to:
- Improve readability
- Add error handling
- Follow [language] best practices
Maintain the same functionality.
```

### Testing

**Test Generation**:
```
Generate pytest tests for: [function/endpoint]
Include: happy path, edge cases, error cases
Use fixtures where appropriate.
Achieve 80%+ coverage.
```

**Edge Case Identification**:
```
Identify edge cases for: [function]
Include: empty inputs, null values, boundary conditions, invalid types
```

### Deployment

**CI/CD Workflow**:
```
Create a GitHub Actions workflow for: [project type]
Include: tests, coverage, linting, deployment
Run on: push and pull requests
```

**Runbook Generation**:
```
Create a runbook for: [task]
Include: prerequisites, step-by-step instructions, verification, rollback
```

---

## Context Scoping

### Code Block Context
- Just the function you're working on
- Use for: simple functions, isolated changes

### File Context
- Entire file
- Use for: refactoring within a file, understanding patterns

### Multi-File Context
- Related files
- Use for: features spanning multiple files, consistency

### Repo-Wide Context
- Entire codebase
- Use for: large refactorings, architecture changes

---

## Common Prompt Templates

### Code Generation
```
Write a [language] [component type] that [purpose].
It should [requirements].
Handle [edge cases].
Include [specific features].
```

### Code Explanation
```
Explain what this code does:
[code block]

Focus on: [specific aspect]
Use [simple/technical] language.
```

### Code Review
```
Review this code for:
- Code quality
- Security issues
- Performance concerns
- Best practices

Provide specific suggestions.
```

### Debugging
```
This code has an error: [error message]
Code: [code block]

Help me:
1. Understand the error
2. Find the root cause
3. Fix it
4. Prevent it in the future
```

---

## Advanced Techniques

### Step-by-Step Breakdown
```
Break down this task: [complex task]
For each step:
1. Explain what needs to be done
2. Show the code
3. Explain why
Then implement all steps.
```

### Constraint-Based
```
Generate code with these constraints:
- [Constraint 1]
- [Constraint 2]
- [Constraint 3]

Task: [task]
```

### Example-Driven
```
Generate code following this pattern: [example]
Apply to: [your task]
Maintain: structure, naming, error handling, documentation style
```

---

## Tips for Better Results

1. **Start with "Act as"** for role-based prompts
2. **Use "Think step by step"** for complex tasks
3. **Ask for explanations** to understand AI reasoning
4. **Request alternatives** to see options
5. **Specify format** (markdown, JSON, code blocks)
6. **Include constraints** (style, performance, security)
7. **Ask for improvements** iteratively

---

## Red Flags (When to Review Carefully)

- AI suggests security-sensitive code
- AI proposes breaking changes without warning
- AI-generated code lacks error handling
- AI suggests deprecated patterns
- AI output doesn't match your requirements

**Always**: Review, test, and understand AI-generated code!

---

## Resources

- OpenAI Prompt Engineering Guide
- Anthropic Prompt Engineering
- GitHub Copilot Documentation
- This course's worksheets (Week 2-3)

