# Week 2, Day 7 Worksheet: Design & Architecture

**Estimated Time**: 4–5 hours (90 min lecture + 3–4 hr lab)  
**Focus**: Prompt-assisted system design, UML generation, trade-off analysis with LLMs

---

## Learning Objectives

By the end of Day 7, you will be able to:
- Use LLMs to propose system architectures
- Generate UML and design diagrams from prompts (Mermaid/PlantUML)
- Evaluate architectural trade-offs with AI assistance
- Create comprehensive architecture documentation
- Scope context effectively for architecture prompts
- **Apply prompt engineering tailored to the design phase of the SDLC** (Learning Objective)

---

## Pre-Activity: Understanding System Design

**Why architecture matters**:
- Good architecture = easier to build, maintain, and scale
- AI can help explore options and evaluate trade-offs
- Clear architecture guides all development decisions
- Poor architecture leads to technical debt

**Think about architecture like building a house**:
- You need a blueprint before construction
- Different designs have different trade-offs
- The foundation affects everything built on top

**Your thoughts on system architecture**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Prompt-Assisted System Design

### Understanding Context Scoping

**Context levels for prompts**:
1. **High-level**: Just the problem statement
2. **Requirements**: Include PRD and user stories
3. **Technical constraints**: Tech stack, performance needs
4. **Existing systems**: If integrating with other systems

**More context = better AI suggestions**

### Activity: Generate Initial Architecture

**Step 1: Prepare Your Context**

**From your Day 6 PRD, extract**:
- Problem statement: _______________________________________________________________________
- Key features: _______________________________________________________________________
- User types: _______________________________________________________________________
- Expected scale: _______________________________________________________________________

**Technical constraints**:
- Tech stack (Python/FastAPI, React): _______________________________________________________________________
- Database requirements: _______________________________________________________________________
- Performance needs: _______________________________________________________________________
- Integration needs: _______________________________________________________________________

**Step 2: Prompt for Architecture**

**Prompt template**:
```
I'm designing a system for: [problem statement]

Requirements:
- [Key requirement 1]
- [Key requirement 2]
- [Key requirement 3]

Tech stack: [Python/FastAPI, React, PostgreSQL/SQLite]

Help me design the system architecture by:
1. Identifying main components
2. Suggesting how components interact
3. Recommending data flow
4. Identifying key design patterns to use
5. Highlighting potential challenges

Format as a structured architecture description.
```

**Your prompt**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**AI-Generated Architecture**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Review**: What makes sense? What needs clarification?

---

## Activity 2: Generate UML Diagrams with Mermaid

### Introduction to Mermaid

**Mermaid** is a text-based diagramming tool that AI can generate.

**Common diagram types**:
- **Flowchart**: Process flows
- **Sequence Diagram**: Interactions over time
- **Class Diagram**: Object relationships
- **Entity Relationship Diagram**: Database schema

### Activity: Generate Flowchart

**Prompt template**:
```
Create a Mermaid flowchart showing the user flow for: [feature]

Include:
- User actions
- System responses
- Decision points
- Error handling

Output as Mermaid code that I can render.
```

**Your feature** (from your PRD):
_______________________________________________________________________

**AI-Generated Mermaid Code**:
```mermaid
[Paste Mermaid code here]
```

**Test it**: Go to [Mermaid Live Editor](https://mermaid.live/) and paste the code

**Does it render correctly?** [ ] Yes [ ] No  
**Refinements needed**: _______________________________________________________________________

### Activity: Generate Sequence Diagram

**Prompt template**:
```
Create a Mermaid sequence diagram for: [interaction scenario]

Show interactions between:
- User
- Frontend
- API
- Database

Include request/response flows and error cases.
```

**Your scenario**:
_______________________________________________________________________

**AI-Generated Sequence Diagram**:
```mermaid
[Paste Mermaid code here]
```

**Test in Mermaid Live Editor**: [ ] Rendered successfully

### Activity: Generate ER Diagram

**Prompt template**:
```
Based on these requirements: [your requirements]

Create a Mermaid Entity Relationship Diagram showing:
- Main entities (tables)
- Relationships between entities
- Key attributes for each entity
- Primary and foreign keys

Output as Mermaid ER diagram code.
```

**Your requirements** (from PRD):
_______________________________________________________________________

**AI-Generated ER Diagram**:
```mermaid
[Paste Mermaid code here]
```

**Test in Mermaid Live Editor**: [ ] Rendered successfully

**Review**: Does this match your data model? What's missing?

---

## Activity 3: Generate Diagrams with PlantUML

### Introduction to PlantUML

**PlantUML** is another text-based diagramming tool, great for:
- Class diagrams
- Component diagrams
- Deployment diagrams
- Activity diagrams

### Activity: Generate Component Diagram

**Prompt template**:
```
Create a PlantUML component diagram for this system: [system description]

Show:
- Main components/modules
- Dependencies between components
- External services/interfaces
- Data stores

Output as PlantUML code.
```

**Your system**:
_______________________________________________________________________

**AI-Generated PlantUML Code**:
```plantuml
[Paste PlantUML code here]
```

**Test it**: Use [PlantUML Online Server](http://www.plantuml.com/plantuml/uml/) or install locally

**Rendered successfully?** [ ] Yes [ ] No

---

## Activity 4: LLM-Driven Trade-Off Analysis

### Understanding Trade-Offs

**Common architectural trade-offs**:
- **Monolith vs Microservices**: Simplicity vs scalability
- **SQL vs NoSQL**: Structure vs flexibility
- **Synchronous vs Asynchronous**: Simplicity vs performance
- **Build vs Buy**: Control vs speed

### Activity: Analyze Trade-Offs with AI

**Prompt template**:
```
I'm deciding between [Option A] and [Option B] for [decision point].

Context:
- [Relevant context 1]
- [Relevant context 2]
- [Constraints]

Help me analyze:
1. Pros and cons of each option
2. When to choose Option A
3. When to choose Option B
4. Recommendation for my use case
5. Risks and mitigations

Format as a structured comparison.
```

**Your trade-off decision** (e.g., SQLite vs PostgreSQL, Monolith vs Microservices):
_______________________________________________________________________

**AI Analysis**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Your decision** (based on AI analysis + your judgment):
_______________________________________________________________________
_______________________________________________________________________

### Activity: Build vs Buy Analysis

**Prompt template**:
```
For this feature: [feature description]

Should I build it custom or use an existing solution?

Consider:
- Development time
- Maintenance burden
- Feature fit
- Cost
- Control/flexibility needs

Provide a recommendation with reasoning.
```

**Your feature**:
_______________________________________________________________________

**AI Recommendation**:
_______________________________________________________________________
_______________________________________________________________________

**Your decision**: [ ] Build [ ] Buy  
**Reasoning**: _______________________________________________________________________

---

## Activity 5: Design Patterns with AI

### Understanding Design Patterns

**Common patterns**:
- **MVC (Model-View-Controller)**: Separation of concerns
- **Repository Pattern**: Data access abstraction
- **Factory Pattern**: Object creation
- **Singleton Pattern**: Single instance

### Activity: Identify Patterns for Your System

**Prompt template**:
```
For this system architecture: [your architecture]

Suggest appropriate design patterns by:
1. Identifying where patterns would help
2. Recommending specific patterns
3. Explaining benefits for this use case
4. Showing how to implement (high-level)

Focus on patterns that add real value.
```

**Your architecture**:
_______________________________________________________________________

**AI Pattern Recommendations**:
_______________________________________________________________________
_______________________________________________________________________

**Which patterns will you use?**
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

---

## Activity 6: Risk Analysis with AI

### Activity: Identify Architecture Risks

**Prompt template**:
```
For this system design: [your architecture]

Identify potential risks and challenges:
1. Technical risks
2. Scalability concerns
3. Security considerations
4. Maintenance challenges
5. Integration risks

For each risk, suggest:
- Likelihood (High/Medium/Low)
- Impact (High/Medium/Low)
- Mitigation strategies
```

**Your architecture**:
_______________________________________________________________________

**AI Risk Analysis**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

**Top 3 risks to address**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

---

## Activity 7: Create Architecture Documentation

### Architecture Document Structure

**Standard sections**:
1. **Overview**: System purpose and scope
2. **Architecture Diagram**: High-level view
3. **Component Description**: What each part does
4. **Data Model**: Database schema
5. **API Design**: Endpoints and contracts
6. **Technology Stack**: Tools and frameworks
7. **Design Patterns**: Patterns used
8. **Trade-offs**: Decisions made and why
9. **Risks and Mitigations**: Known issues and solutions

### Activity: Generate Architecture Doc with AI

**Prompt template**:
```
Create a comprehensive architecture document for: [system description]

Include all standard sections (Overview, Diagrams, Components, Data Model, 
API Design, Tech Stack, Patterns, Trade-offs, Risks).

Use the architecture we discussed: [your architecture]
Include Mermaid diagrams where helpful.

Format as a structured markdown document.
```

**Your system description**:
_______________________________________________________________________

**AI-Generated Architecture Doc** (key sections):
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

### Refine Your Architecture Document

**Create file**: `week2/day7/Architecture.md`

**Structure**:
```markdown
# System Architecture: [Project Name]

## 1. Overview
[System purpose and scope]

## 2. High-Level Architecture
[Mermaid diagram]

## 3. Component Description
[What each component does]

## 4. Data Model
[ER diagram and description]

## 5. API Design
[Endpoints and contracts]

## 6. Technology Stack
[Tools and frameworks]

## 7. Design Patterns
[Patterns used and why]

## 8. Trade-offs and Decisions
[Key decisions and reasoning]

## 9. Risks and Mitigations
[Known issues and solutions]

## 10. Diagrams
[All Mermaid/PlantUML diagrams]

## 11. AI Usage Log
[Prompts used and how AI helped]
```

**Architecture document created?** [ ] Yes

---

## Activity 8: Create All Diagrams

### Organize Your Diagrams

**Create file**: `week2/day7/diagrams/`

**Include**:
- `architecture-flowchart.mmd` - High-level flow
- `sequence-diagram.mmd` - Key interactions
- `er-diagram.mmd` - Database schema
- `component-diagram.puml` - Component structure

**Or create a single file**: `week2/day7/diagrams.md`

**All diagrams created?** [ ] Yes

---

## Deliverable Checklist

- [ ] Generated initial architecture with AI
- [ ] Created Mermaid flowchart for user flow
- [ ] Created Mermaid sequence diagram
- [ ] Created ER diagram (Mermaid or PlantUML)
- [ ] Analyzed key trade-offs with AI
- [ ] Identified design patterns
- [ ] Performed risk analysis
- [ ] Created comprehensive architecture document
- [ ] All diagrams rendered and verified
- [ ] Documented AI usage
- [ ] Committed to repository
- [ ] Created PR with architecture doc

---

## Reflection Questions

1. **How did AI help you think about architecture differently?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What was most valuable: diagrams or written descriptions?**
   _______________________________________________________________________

3. **How did trade-off analysis with AI help your decisions?**
   _______________________________________________________________________

4. **What would you do differently next time?**
   _______________________________________________________________________

---

## Key Takeaways

**Remember**:
- ✅ Provide rich context for better AI architecture suggestions
- ✅ Use diagrams to visualize and communicate design
- ✅ Always evaluate trade-offs—AI suggests, you decide
- ✅ Document your decisions and reasoning
- ✅ Consider risks early, not after building

**Best practices**:
- Start high-level, then drill down
- Use multiple diagram types for different views
- Validate diagrams render correctly
- Review AI suggestions critically

---

## Additional Resources

- [Mermaid Documentation](https://mermaid.js.org/)
- [Mermaid Live Editor](https://mermaid.live/)
- [PlantUML Documentation](https://plantuml.com/)
- [Copilot Chat & Context Tips](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat)
- [System Design Primer](https://github.com/donnemartin/system-design-primer)

---

## Next Steps

Tomorrow (Day 8), you'll start Development & Coding. Make sure you:
- Have your architecture document ready
- Understand your component design
- Know your API endpoints
- Are ready to scaffold your FastAPI application

**Excellent design work!** 🎨

