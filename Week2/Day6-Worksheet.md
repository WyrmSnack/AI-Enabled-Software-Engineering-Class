# Week 2, Day 6 Worksheet: Planning & Requirements

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: Requirements elicitation with LLMs, user stories, acceptance criteria, and AI-assisted backlog creation

---

## Learning Objectives

By the end of Day 6, you will be able to:
- Understand the GenAI landscape for software engineering
- Use LLMs to elicit and document requirements
- Create user stories and acceptance criteria with AI assistance
- Build a product backlog using AI tools
- Frame problem statements that AI tools can effectively act on
- **Apply prompt engineering tailored to the planning/requirements phase of the SDLC** (Learning Objective)

---

## Pre-Activity: Understanding Requirements

**Why requirements matter**:
- Clear requirements = better code (whether written by you or AI)
- AI tools need clear, specific instructions to be effective
- Good requirements prevent rework and confusion
- Requirements are the foundation of everything that follows

**Think about a project you've worked on**:
- What made the requirements clear or unclear?
- How did unclear requirements cause problems?
- How could AI have helped clarify requirements?

**Your thoughts**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: GenAI Landscape for Software Engineering

### Understanding the Tools

**GenAI tools for requirements**:
- **ChatGPT/Claude**: For brainstorming, requirements elicitation, documentation
- **GitHub Copilot Chat**: For technical requirements, code-related questions
- **Specialized tools**: For PRD generation, user story creation

**When to use AI for requirements**:
- ✅ Brainstorming features and capabilities
- ✅ Generating user stories from high-level ideas
- ✅ Creating acceptance criteria
- ✅ Organizing and prioritizing backlog items
- ✅ Identifying edge cases and scenarios
- ❌ Final decision-making (you decide!)
- ❌ Understanding domain-specific business rules (you provide context)

### Activity: Explore GenAI Capabilities

**Try this prompt with an AI tool**:

```
I'm building a task management application. Help me brainstorm 
key features and user needs. Consider:
- Different user types (individuals, teams)
- Core functionality needed
- Nice-to-have features
```

**AI Response** (paste key points):
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**What did the AI help you think of that you might have missed?**
_______________________________________________________________________

---

## Activity 2: Requirements Elicitation with LLMs

### Prompt Patterns for Requirements

**Pattern 1: Problem Statement to Requirements**

**Example prompt**:
```
I need to build a system for [problem description].

Help me identify:
1. Who are the users?
2. What are their main goals?
3. What problems does this solve?
4. What are the key features needed?
5. What are potential constraints or limitations?
```

**Your turn**: Write a problem statement for a project idea:

**Problem Statement**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Now use AI to elicit requirements**:

**Prompt**:
_______________________________________________________________________
_______________________________________________________________________

**AI-Generated Requirements**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

### Pattern 2: Stakeholder Interview Simulation

**Prompt template**:
```
Act as a [stakeholder type] for a [project type]. 
I'm interviewing you to understand requirements.

As a [stakeholder], what are your main concerns?
What features are most important to you?
What would make this project successful for you?
```

**Try it**: Interview a "product manager" for your project idea

**Key insights from AI stakeholder**:
_______________________________________________________________________
_______________________________________________________________________

### Pattern 3: Requirements Refinement

**Prompt template**:
```
I have these requirements: [list requirements]

Help me:
1. Identify any missing requirements
2. Clarify ambiguous requirements
3. Identify potential conflicts
4. Suggest prioritization
```

**Your requirements**:
_______________________________________________________________________
_______________________________________________________________________

**AI refinement suggestions**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 3: User Stories with AI

### Understanding User Stories

**Format**: "As a [user type], I want [goal] so that [benefit]"

**Example**:
- "As a project manager, I want to see task completion rates so that I can track team progress"

**Components**:
- **User type**: Who needs this?
- **Goal**: What do they want to do?
- **Benefit**: Why is this valuable?

### Activity: Generate User Stories

**Prompt template**:
```
Based on these requirements: [your requirements]

Generate user stories following this format:
"As a [user type], I want [goal] so that [benefit]"

Include:
- 5-10 user stories
- Different user types
- Mix of core features and nice-to-haves
```

**Your requirements** (from Activity 2):
_______________________________________________________________________

**AI-Generated User Stories**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________
6. _______________________________________________________________________
7. _______________________________________________________________________
8. _______________________________________________________________________

**Review and refine**: Which stories are most important? Which need clarification?

**Prioritized user stories**:
- **Must have**: _______________________________________________________________________
- **Should have**: _______________________________________________________________________
- **Nice to have**: _______________________________________________________________________

---

## Activity 4: Acceptance Criteria with AI

### Understanding Acceptance Criteria

**Acceptance criteria** define when a user story is "done". They should be:
- Specific and testable
- Clear and unambiguous
- Focused on user value

**Example**:
- **Story**: "As a user, I want to log in so that I can access my account"
- **Acceptance Criteria**:
  - User can enter email and password
  - System validates credentials
  - Successful login redirects to dashboard
  - Failed login shows error message
  - Password is hidden during entry

### Activity: Generate Acceptance Criteria

**Prompt template**:
```
For this user story: "[user story]"

Generate detailed acceptance criteria that are:
- Specific and testable
- Cover happy path and edge cases
- Focus on user value
- Include 5-7 criteria
```

**Your user story**:
_______________________________________________________________________

**AI-Generated Acceptance Criteria**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________
4. _______________________________________________________________________
5. _______________________________________________________________________

**Review**: Are these testable? Do they cover edge cases?

**Refined acceptance criteria**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 5: AI-Assisted Sprint Planning

### Understanding Backlogs

**Product Backlog**: All features, enhancements, and fixes
**Sprint Backlog**: Items selected for current sprint

**Backlog items should include**:
- User story
- Acceptance criteria
- Priority
- Estimated effort
- Dependencies

### Activity: Create Backlog with AI

**Prompt template**:
```
I have these user stories: [list user stories]

Help me create a product backlog by:
1. Organizing stories into themes/epics
2. Suggesting priorities (High/Medium/Low)
3. Identifying dependencies between stories
4. Suggesting which stories should be in the first sprint
5. Format as a table with: Story, Priority, Theme, Dependencies
```

**Your user stories** (from Activity 3):
_______________________________________________________________________
_______________________________________________________________________

**AI-Generated Backlog**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Review and adjust priorities** (you decide!):
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 6: Create Your PRD (Product Requirements Document)

### PRD Structure

**Standard PRD sections**:
1. **Overview**: What are we building and why?
2. **Goals**: What are we trying to achieve?
3. **User Personas**: Who are the users?
4. **User Stories**: What do users need?
5. **Acceptance Criteria**: How do we know it's done?
6. **Non-functional Requirements**: Performance, security, etc.
7. **Constraints**: Limitations and assumptions
8. **Success Metrics**: How do we measure success?

### Activity: Generate PRD with AI

**Prompt template**:
```
Create a Product Requirements Document (PRD) for: [project description]

Include:
1. Executive Summary
2. Problem Statement
3. Goals and Objectives
4. User Personas (2-3)
5. User Stories (8-10)
6. Acceptance Criteria for top 3 stories
7. Non-functional Requirements
8. Constraints and Assumptions
9. Success Metrics

Format as a structured document with clear sections.
```

**Your project description**:
_______________________________________________________________________
_______________________________________________________________________

**AI-Generated PRD** (key sections):
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

### Refine Your PRD

**Review the AI-generated PRD**:
- [ ] Does it capture the problem clearly?
- [ ] Are user stories realistic and valuable?
- [ ] Are acceptance criteria testable?
- [ ] Are constraints identified?
- [ ] Does it feel complete?

**Your refinements**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 7: Create Your Deliverables

### Deliverable 1: Draft PRD

**Create a file**: `week2/day6/PRD.md`

**Structure your PRD**:
```markdown
# Product Requirements Document: [Project Name]

## 1. Overview
[What and why]

## 2. Problem Statement
[The problem we're solving]

## 3. Goals and Objectives
[What we want to achieve]

## 4. User Personas
[Who are the users]

## 5. User Stories
[Your prioritized user stories]

## 6. Acceptance Criteria
[For key user stories]

## 7. Non-functional Requirements
[Performance, security, etc.]

## 8. Constraints and Assumptions
[Limitations and assumptions]

## 9. Success Metrics
[How we measure success]

## 10. AI Usage Log
[Document prompts used, AI tools, and how AI helped]
```

**PRD created?** [ ] Yes  
**Location**: `week2/day6/PRD.md`

### Deliverable 2: Product Backlog

**Create a file**: `week2/day6/Backlog.md`

**Format**:
```markdown
# Product Backlog

## Epic 1: [Theme Name]

### Story 1: [User Story]
- **Priority**: High/Medium/Low
- **Acceptance Criteria**:
  - [ ] Criterion 1
  - [ ] Criterion 2
- **Dependencies**: [Other stories]
- **Estimated Effort**: [Story points or hours]

### Story 2: [User Story]
...
```

**Backlog created?** [ ] Yes  
**Location**: `week2/day6/Backlog.md`

### Deliverable 3: AI Usage Log

**Document your AI usage**:

**File**: `week2/day6/AI-Usage-Log.md`

**Template**:
```markdown
# AI Usage Log - Day 6: Planning & Requirements

## Prompts Used

### Prompt 1: Requirements Elicitation
**Tool**: [ChatGPT/Claude/Copilot]
**Prompt**: [Your prompt]
**Result**: [What you got]
**How it helped**: [How it improved your work]

### Prompt 2: User Story Generation
**Tool**: [Tool used]
**Prompt**: [Your prompt]
**Result**: [What you got]
**How it helped**: [How it improved your work]

[... continue for all prompts ...]

## Reflection
[How did AI help? What worked well? What would you do differently?]
```

**AI Usage Log created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Completed requirements elicitation activities
- [ ] Generated user stories with AI assistance
- [ ] Created acceptance criteria for key stories
- [ ] Built product backlog with priorities
- [ ] Created draft PRD document
- [ ] Documented all AI usage in log
- [ ] Committed deliverables to repository
- [ ] Created PR with PRD and backlog

---

## Reflection Questions

1. **How did AI help you think about requirements differently?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What prompt patterns worked best for you?**
   _______________________________________________________________________

3. **What challenges did you face when using AI for requirements?**
   _______________________________________________________________________

4. **How will you use AI for requirements in future projects?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ AI is great for brainstorming and generating options
- ✅ You make the final decisions on priorities and requirements
- ✅ Clear, specific prompts yield better results
- ✅ Always review and refine AI-generated content
- ✅ Document your AI usage for transparency

**Prompt patterns that work**:
- Be specific about what you need
- Provide context about your project
- Ask for structured output (tables, lists, sections)
- Iterate and refine based on results

---

## Additional Resources

- [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)
- [Anthropic Prompt Engineering](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering)
- [Atlassian PRD Template](https://www.atlassian.com/agile/product-management/product-requirements)
- [User Story Mapping Guide](https://www.atlassian.com/agile/project-management/user-stories)

---

## Next Steps

Tomorrow (Day 7), you'll work on Design & Architecture. Make sure you:
- Have your PRD and backlog ready
- Understand your user stories and requirements
- Are ready to translate requirements into system design

**Great work today!** 🎉

