# Week 3, Day 11 Worksheet: In-Depth Code Generation

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: Advanced context scoping, repo-wide prompting, refactoring, generating UI from designs

---

## Learning Objectives

By the end of Day 11, you will be able to:
- Use repo-wide and multi-file context effectively
- Refactor code across multiple files with AI
- Generate UI components from design screenshots
- Understand how context packaging affects code quality
- Master advanced prompting techniques for complex tasks

---

## Pre-Activity: Context is King

**Key insight**: The quality of AI-generated code directly depends on the context you provide.

**Context levels**:
1. **Code block**: Just the function
2. **File**: Entire file
3. **Multi-file**: Related files
4. **Repo-wide**: Entire codebase

**More context = better, more consistent code**

**Your experience with context so far**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Repo-Wide Context Prompting

### Understanding Repo-Wide Context

**When to use**:
- Refactoring across multiple files
- Adding features that touch many files
- Ensuring consistency across codebase
- Understanding project structure

### Activity: Explore Your Codebase with AI

**Prompt** (Ask mode):
```
Analyze this entire codebase and provide:
1. Overall architecture
2. Main components and their relationships
3. Code patterns used
4. Potential improvements
5. Areas that need refactoring

[Include repo-wide context]
```

**AI Analysis**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**What did you learn about your codebase?**
_______________________________________________________________________

### Activity: Multi-File Feature Addition

**Scenario**: Add a new feature that requires changes to multiple files

**Your feature**: _______________________________________________________________________

**Prompt** (Agent or Ask mode with repo context):
```
Add this feature: [feature description]

This feature needs to:
- Add a new endpoint in routers/
- Create a new model in models/
- Update database schema
- Add tests in tests/
- Update documentation

Ensure consistency with existing code patterns and style.
Use the entire codebase as context.
```

**AI-Generated Changes**:
_______________________________________________________________________
_______________________________________________________________________

**Review the changes**:
- [ ] Consistent with existing patterns?
- [ ] All files updated correctly?
- [ ] Tests included?
- [ ] Documentation updated?

**What worked well?** _______________________________________________________________________
**What needed adjustment?** _______________________________________________________________________

---

## Activity 2: Advanced Refactoring

### Activity: Refactor Across Files

**Identify code to refactor**:
- Duplicate code across files
- Inconsistent patterns
- Code that could be extracted

**Your refactoring target**:
_______________________________________________________________________

**Prompt** (with repo-wide context):
```
Refactor this codebase to:

[Your refactoring goals]

Changes needed:
- [File 1]: [What to change]
- [File 2]: [What to change]
- [File 3]: [What to change]

Requirements:
- Maintain existing functionality
- Follow existing code patterns
- Update all related files
- Update tests
- Update documentation

Show all changes needed across the codebase.
```

**AI Refactoring Plan**:
_______________________________________________________________________
_______________________________________________________________________

**Apply refactoring**: [ ] Done

**Test after refactoring**: [ ] All tests pass

### Activity: Extract Common Patterns

**Prompt**:
```
I notice this pattern repeated in multiple files: [describe pattern]

Extract this into a reusable utility/helper.

Requirements:
- Create a new utility file
- Update all files using this pattern
- Maintain backward compatibility
- Add tests for the utility
- Update documentation
```

**Your repeated pattern**:
_______________________________________________________________________

**AI Extraction**:
_______________________________________________________________________
_______________________________________________________________________

**Applied?** [ ] Yes  
**Tests pass?** [ ] Yes

---

## Activity 3: Generating Components from Design Screenshots

### Understanding Design-to-Code

**Process**:
1. Provide design screenshot/image
2. AI analyzes the design
3. AI generates code to match
4. You refine and integrate

### Activity: Prepare a Design

**Option 1: Use an existing design**
- Find a UI design (Figma, screenshot, mockup)
- Save as image file

**Option 2: Describe a design**
- Write a detailed description
- Include layout, colors, components

**Your design** (describe or reference):
_______________________________________________________________________
_______________________________________________________________________

### Activity: Generate React Component

**Prompt** (with design image or description):
```
Create a React component that matches this design: [design/image]

Requirements:
- Use modern React (hooks, functional components)
- Match the layout exactly
- Use appropriate styling (CSS modules, Tailwind, or styled-components)
- Make it responsive
- Include proper TypeScript types
- Follow React best practices
- Make components reusable where appropriate

Break down into smaller components if needed.
```

**AI-Generated Component**:
```tsx
[Paste React code]
```

**Review**:
- [ ] Matches design?
- [ ] Properly structured?
- [ ] Responsive?
- [ ] TypeScript types correct?

**Refinements needed**:
_______________________________________________________________________

### Activity: Refine Component with Iterative Prompts

**If component needs adjustment**:

**Prompt 1**: "Make the spacing match the design more closely"

**Prompt 2**: "Update colors to match the design palette"

**Prompt 3**: "Add hover states and interactions"

**Iterative refinements**:
_______________________________________________________________________
_______________________________________________________________________

**Final component**: [ ] Matches design

---

## Activity 4: Context Packaging Best Practices

### Activity: Practice Different Context Levels

**Scenario**: Add a new API endpoint

**Test 1: Minimal Context**
- Just the endpoint code
- Prompt: "Add error handling"

**Result**:
_______________________________________________________________________

**Test 2: File Context**
- Include entire router file
- Same prompt

**Result**:
_______________________________________________________________________

**Test 3: Multi-File Context**
- Include router, models, database files
- Same prompt

**Result**:
_______________________________________________________________________

**Which was best?** [ ] Minimal [ ] File [ ] Multi-file

**Why?**
_______________________________________________________________________

### Activity: Create Context Package

**For complex tasks, prepare context**:

**Prompt template**:
```
[Context: Include relevant files]

Task: [Your task]

Use the provided context to ensure:
- Consistency with existing code
- Proper use of existing utilities
- Following established patterns
- Integration with existing systems
```

**Your context package**:
- Files to include: _______________________________________________________________________
- Why these files: _______________________________________________________________________

**Result quality**: [ ] Better [ ] Same [ ] Worse

---

## Activity 5: Advanced Prompting Techniques

### Technique 1: Step-by-Step Breakdown

**Prompt**:
```
Break down this task into steps: [complex task]

For each step:
1. Explain what needs to be done
2. Show the code changes
3. Explain why

Then implement all steps.
```

**Your complex task**:
_______________________________________________________________________

**AI Breakdown and Implementation**:
_______________________________________________________________________
_______________________________________________________________________

### Technique 2: Constraint-Based Generation

**Prompt**:
```
Generate code with these constraints:
- Must use async/await (no callbacks)
- Must include error handling
- Must be type-annotated
- Must follow PEP 8 style
- Must include docstrings
- Must be testable

Task: [Your task]
```

**Your task with constraints**:
_______________________________________________________________________

**AI-Generated Code**:
_______________________________________________________________________

**Check constraints**: [ ] All met

### Technique 3: Example-Driven Generation

**Prompt**:
```
Generate code following this pattern: [example code]

Apply the same pattern to: [your task]

Maintain the same:
- Structure
- Naming conventions
- Error handling approach
- Documentation style
```

**Your example pattern**:
_______________________________________________________________________

**Your task**:
_______________________________________________________________________

**AI-Generated Code**:
_______________________________________________________________________

**Matches pattern?** [ ] Yes

---

## Activity 6: Refactoring Large Codebases

### Activity: Identify Refactoring Opportunities

**Prompt** (repo-wide):
```
Analyze this codebase for refactoring opportunities:

Focus on:
- Code duplication
- Long functions (>50 lines)
- Complex conditionals
- Missing abstractions
- Inconsistent patterns
- Performance issues

Prioritize by impact and effort.
```

**AI Analysis**:
_______________________________________________________________________
_______________________________________________________________________

**Top 3 refactoring opportunities**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

### Activity: Plan Refactoring

**Pick one opportunity**:

**Prompt**:
```
Plan a refactoring for: [refactoring opportunity]

Include:
- Current state analysis
- Proposed changes
- Files affected
- Risk assessment
- Testing strategy
- Rollback plan
```

**Your refactoring**:
_______________________________________________________________________

**AI Refactoring Plan**:
_______________________________________________________________________
_______________________________________________________________________

**Execute refactoring**: [ ] Done  
**Tests pass?** [ ] Yes

---

## Activity 7: Create Deliverables

### Deliverable 1: Significant Refactor

**What you refactored**:
_______________________________________________________________________

**Files changed**:
- _______________________________________________________________________
- _______________________________________________________________________
- _______________________________________________________________________

**Refactor documented?** [ ] Yes  
**Tests updated?** [ ] Yes

### Deliverable 2: Generated UI Component

**Component description**:
_______________________________________________________________________

**Files created**:
- _______________________________________________________________________

**Component matches design?** [ ] Yes

### Deliverable 3: AI Usage Log

**File**: `week3/day11/AI-Usage-Log.md`

**Document**:
- Repo-wide context prompts
- Refactoring prompts
- Component generation prompts
- Advanced techniques used
- What worked best
- Lessons learned

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Used repo-wide context for analysis
- [ ] Performed multi-file refactoring
- [ ] Generated UI component from design
- [ ] Practiced different context levels
- [ ] Used advanced prompting techniques
- [ ] Identified refactoring opportunities
- [ ] Completed significant refactor
- [ ] Created generated UI component
- [ ] Documented all AI usage
- [ ] Committed to repository
- [ ] Created PR with refactor and component

---

## Reflection Questions

1. **How did repo-wide context improve AI suggestions?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What was most challenging about multi-file refactoring?**
   _______________________________________________________________________

3. **How effective was AI at generating components from designs?**
   _______________________________________________________________________

4. **What advanced techniques will you use going forward?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Context quality = code quality
- ✅ Repo-wide context for large changes
- ✅ Multi-file context for features
- ✅ Iterate and refine AI output
- ✅ Always test after refactoring
- ✅ Design-to-code works with good prompts

**Best practices**:
- Provide maximum relevant context
- Break complex tasks into steps
- Use constraints for consistency
- Follow examples for patterns
- Review and test everything

---

## Additional Resources

- [Copilot Chat Cookbook](https://docs.github.com/en/copilot/copilot-chat-cookbook)
- [React Documentation](https://react.dev/learn)
- [Refactoring Guide](https://refactoring.guru/refactoring)
- [Context Management Best Practices](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat)

---

## Next Steps

Tomorrow (Day 12), you'll work on External Tools Integration. Make sure you:
- Understand repo-wide context
- Can refactor effectively
- Are ready to work with agents and MCP

**Excellent advanced work!** 🚀

