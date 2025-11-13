### Course Title
GenAI Across the SDLC: Practical LLM Integration for Software Engineering

> **📌 New to this course?** Start with **[START-HERE.md](START-HERE.md)** for complete navigation and getting started guide.

### Course Overview
A 3-week, hands-on program (preceded by a self-paced Week 0 foundation) that teaches software engineers how to apply large language models (LLMs) and developer AI tools across the software development lifecycle (SDLC)—from planning and design to coding, testing, and deployment—culminating in a full-stack GenAI‑enhanced capstone.

### Learning Objectives
By the end, participants will be able to:
- Explain fundamentals of large language models and effective prompting techniques.
- Identify key integration points of GenAI across the SDLC.
- Use LLMs and GenAI tools for requirements, design, code generation, and testing.
- Apply prompt engineering tailored to different SDLC phases.
- Integrate GitHub Copilot into development environments to improve speed and accuracy.
- Build and present a working prototype demonstrating GenAI‑enhanced workflows.

### Prerequisites and Entry
- Complete and pass Workera assessments: GenAI Essentials, Software Engineering Foundations, Web Apps, Python Fundamentals, SQL Fundamentals.
- Gain career manager approval.
- Validate access to vendor websites and learning platform.
- **Week 0 (Self-Paced Prep)**: Complete foundational prep work (5–7 days, 1–2 hours/day) covering SDLC basics, GitHub workflow, Python fundamentals, SQL, web foundations, and GenAI tool introduction. See Week 0 section below for details.

### Tools and Platforms
- IDE + AI pair programming: GitHub Copilot (including Agent), Cursor, Cody.
- GitHub (issues, PRs, Actions), optional MCP server support for Copilot.
- Python 3.11+, FastAPI, pytest, SQL database (PostgreSQL or SQLite).
- React + Vite or Next.js; component libraries optional.
- Diagramming: PlantUML/Mermaid; UML generators.
- Observability: basic logging; optional APM/synthetic tools.
- Prompt notebooks or prompt logs for traceability.

---

## Schedule and Topics

### Week 0 — Self-Paced Prep: Building Foundations for Success

**Duration**: 5–7 days, 1–2 hours per day (≈ 10 hours total)

**Purpose**: Before diving into the 3-week hands-on program, establish core literacy in how software projects are structured, everyday tools engineers use (GitHub, IDEs, terminals), essential programming and database concepts, and how GenAI fits into the engineering mindset. The goal is **fluency, not mastery** — by the end, you'll be able to follow technical conversations, understand code examples, and confidently use AI coding tools.

- **Day 0.1: Orientation: How the SDLC works**
  - What "Software Development Lifecycle" means; overview of planning → design → code → test → deploy.
  - Watch: "What is the SDLC?" (YouTube – freeCodeCamp, 10 min).
  - Read: [Microsoft Learn – SDLC Overview](https://learn.microsoft.com/en-us/devops/develop/what-is-sdlc).
  - Deliverable: 1-page reflection on which SDLC phase feels most natural and why.
  - Suggested Learning Aids:
    - Microsoft Learn: SDLC Overview — https://learn.microsoft.com/en-us/devops/develop/what-is-sdlc

- **Day 0.2: GitHub & Project Workflow**
  - Repos, commits, pull requests; collaboration basics.
  - Create a GitHub account; follow [GitHub Skills – Introduction to GitHub](https://github.com/skills/introduction-to-github).
  - Practice committing a text file (e.g., `hello.txt`).
  - Deliverable: Screenshot of your repository page with your first commit.
  - Suggested Learning Aids:
    - GitHub Skills: Introduction to GitHub — https://github.com/skills/introduction-to-github
    - GitHub Getting Started — https://docs.github.com/en/get-started

- **Day 0.3: Python Fundamentals**
  - Variables, functions, control flow, packages.
  - Install VS Code or Cursor; follow [Python.org Tutorial](https://docs.python.org/3/tutorial/index.html#tutorial-index) sections 1–4.
  - (Optional AI practice) Use Copilot Chat to generate a "Hello World" script and a loop that prints numbers 1–5.
  - Deliverable: Upload a `main.py` file that prints your name and the current date.
  - Suggested Learning Aids:
    - Python docs Tutorial — https://docs.python.org/3/tutorial/
    - VS Code — https://code.visualstudio.com/ | Cursor — https://cursor.com/

- **Day 0.4: Databases & SQL**
  - Tables, queries, joins.
  - Visit [SQLBolt](https://sqlbolt.com/) — Lessons 1–6.
  - (Optional) Install SQLite Browser for local experiments.
  - Deliverable: Screenshot of a completed SQLBolt lesson.
  - Suggested Learning Aids:
    - SQLBolt (SQL practice) — https://sqlbolt.com/
    - SQLite Browser — https://sqlitebrowser.org/

- **Day 0.5: Web Foundations & APIs**
  - APIs, JSON, client-server concept.
  - Read: [What is an API? by Postman](https://www.postman.com/api-what-is-an-api/).
  - Run in Python: `import requests; res = requests.get("https://api.github.com"); print(res.json())`.
  - Deliverable: Paste a sample of your JSON output.
  - Suggested Learning Aids:
    - Postman: What is an API? — https://www.postman.com/api-what-is-an-api/
    - FastAPI Tutorial — https://fastapi.tiangolo.com/

- **Day 0.6: Introduction to GenAI Tools**
  - LLMs, prompting, Copilot basics.
  - Read: [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering).
  - Try 3 prompt styles: instructional, exploratory, iterative.
  - If you have access, enable Copilot Chat in VS Code or Cursor.
  - Deliverable: Submit your 3 prompts + AI responses as a `.md` file.
  - Suggested Learning Aids:
    - OpenAI Prompt Engineering Guide — https://platform.openai.com/docs/guides/prompt-engineering
    - GitHub Copilot docs — https://docs.github.com/en/copilot
    - Cursor docs — https://docs.cursor.com/

- **Day 0.7: Synthesis & Readiness Check**
  - Review, reflection, troubleshooting.
  - Checklist: GitHub account, VS Code/Cursor with Copilot, Python 3.11+, FastAPI and pytest installed, SQLBolt Lessons 1–6 completed, 3 prompt engineering exercises completed, basic understanding of SDLC phases.
  - Reflection prompt: "In one paragraph, describe how GenAI could help you overcome your current challenges as a learner or developer."
  - Deliverable: Upload your reflection + checklist to your GitHub repo (Week0 folder).
  - Suggested Learning Aids:
    - FastAPI — https://fastapi.tiangolo.com/
    - pytest — https://docs.pytest.org/en/stable/

**Outcome**: By the end of Week 0, you will be able to explain each SDLC phase in plain language, create/edit/push code to GitHub, write and run small Python programs, perform simple SQL queries, prompt AI tools clearly and evaluate their responses, and navigate the course's Week 1–3 content with confidence and minimal friction.

**Optional Enrichment**:
- Command Line Basics: [Codecademy Intro to CLI](https://www.codecademy.com/learn/learn-the-command-line)
- FastAPI Preview: [FastAPI Crash Course – freeCodeCamp](https://www.youtube.com/watch?v=7t2alSnE2-I)
- React Preview: [React Official Tutorial](https://react.dev/learn)
- Secure Coding Mindset: [OWASP Top 10 Overview](https://owasp.org/www-project-top-ten/)

### Week 1
- Days 1–4: Assessment & Selection
  - Complete Workera assessments listed above.
  - Secure career manager approval.
  - Importance: Establish baseline readiness in GenAI, software engineering, Python, SQL, and web apps.
  - Objectives:
    - Verify foundational knowledge and identify any skill gaps.
    - Ensure access to required platforms and tools is in place ahead of hands-on work.
  - Suggested Learning Aids:
    - Microsoft Learn: Copilot path — https://learn.microsoft.com/en-us/training/paths/copilot/
    - Python docs Tutorial — https://docs.python.org/3/tutorial/
    - SQLBolt (SQL practice) — https://sqlbolt.com/
    - FastAPI Tutorial — https://fastapi.tiangolo.com/
- Day 5: Vendor Kickoff
  - Attend kickoff; confirm platform access and project logistics.
  - Importance: Align expectations and remove access blockers before build starts.
  - Objectives:
    - Validate logins for GitHub, learning platforms, and any vendor sites.
    - Confirm repo, branching, and CI/CD conventions for the course projects.
  - Suggested Learning Aids:
    - GitHub Getting Started — https://docs.github.com/en/get-started
    - GitHub Actions Overview — https://docs.github.com/en/actions

### Week 2
- Day 6: Planning & Requirements
  - GenAI landscape for software engineering.
  - Requirements elicitation with LLMs; user stories, acceptance criteria.
  - AI‑assisted sprint planning and backlog creation.
  - Deliverable: draft PRD and backlog with AI‑generated user stories.
  - Importance: Good prompts and clear requirements drive all downstream AI-assisted work.
  - Objectives:
    - Frame problem statements and acceptance criteria that AI tools can act on.
    - Practice prompt patterns for elicitation and backlog shaping.
  - Suggested Learning Aids:
    - OpenAI Prompt Engineering Guide — https://platform.openai.com/docs/guides/prompt-engineering
    - Anthropic Prompt Engineering — https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering
    - Atlassian PRD Template — https://www.atlassian.com/agile/product-management/product-requirements
- Day 7: Design & Architecture
  - Prompt‑assisted system design; context scoping for prompts.
  - Auto‑generate UML and design docs (Mermaid/PlantUML).
  - LLM‑driven trade‑off analysis (build vs buy, patterns, risks).
  - Deliverable: architecture doc + diagrams.
  - Importance: Architectural clarity reduces rework; AI can accelerate options analysis.
  - Objectives:
    - Use LLMs to propose architectures and evaluate trade-offs.
    - Produce diagrams and design docs from prompts.
  - Suggested Learning Aids:
    - Mermaid — https://mermaid.js.org/ and Live Editor — https://mermaid.live/
    - PlantUML — https://plantuml.com/
    - Copilot Chat & context tips — https://docs.github.com/en/copilot/using-github-copilot/copilot-chat
- Day 8: Development & Coding
  - AI pair programming (Copilot, Cody, Cursor); Ask/Edit/Agent intro.
  - Writing/refactoring; docstrings, READMEs, commit messages.
  - Deliverable: scaffolded API and basic endpoints; README generated by AI.
  - Importance: Learn productive collaboration patterns with AI tools.
  - Objectives:
    - Use Ask/Edit/Agent modes effectively with correct context scope.
    - Generate scaffolds and iterate using refactoring prompts.
  - Suggested Learning Aids:
    - GitHub Copilot docs — https://docs.github.com/en/copilot
    - GitHub Skills: Getting Started with Copilot — https://github.com/skills/getting-started-with-github-copilot
    - Cursor docs — https://docs.cursor.com/ | Cody docs — https://docs.sourcegraph.com/cody
- Day 9: Testing & Quality Assurance
  - GenAI for unit/integration test generation; fixtures and edge cases.
  - AI‑driven bug analysis, test prioritization; coverage exploration.
  - Deliverable: test suite with coverage report.
  - Importance: Reliable tests are essential when AI writes significant portions of code.
  - Objectives:
    - Prompt LLMs for high-value tests and edge cases.
    - Integrate coverage and prioritize tests based on risk.
  - Suggested Learning Aids:
    - pytest — https://docs.pytest.org/en/stable/
    - coverage.py — https://coverage.readthedocs.io/
    - pytest-cov — https://pytest-cov.readthedocs.io/
- Day 10: Deployment & Maintenance
  - Prompts for CI/CD automation (workflows, secrets guidance).
  - Monitoring/observability; incident summarization with LLMs.
  - Runbooks and postmortems generated with AI.
  - Deliverable: CI workflow file; incident summary template.
  - Importance: Automation and operability multiply team output and resilience.
  - Objectives:
    - Create CI workflows via prompts; ensure repeatable deployments.
    - Use LLMs to draft runbooks and incident summaries.
  - Suggested Learning Aids:
    - GitHub Actions docs — https://docs.github.com/en/actions
    - Google SRE Postmortems — https://sre.google/sre-book/postmortem-culture/
    - incident.io templates — https://incident.io/templates

### Week 3
- Day 11: In‑Depth Code Generation
  - Copilot/Cursor modes: Ask, Edit, Agent.
  - Providing context: code block, file, multi‑file, repo‑wide.
  - Refactoring with AI; generating components from design screenshots.
  - Deliverable: significant refactor + generated UI component.
  - Importance: Context packaging dramatically impacts the quality of generated code.
  - Objectives:
    - Practice repo-wide and multi-file context prompting.
    - Convert design artifacts to components with high-fidelity prompts.
  - Suggested Learning Aids:
    - Copilot Chat Cookbook — https://docs.github.com/en/copilot/copilot-chat-cookbook
    - React (new docs) — https://react.dev/learn
- Day 12: External Tools Integration
  - Fully autonomous Copilot Agent overview.
  - Assigning issues, setting up unit testing env for the agent, PR review.
  - Add MCP server support to GitHub Copilot; optional: build a Copilot extension.
  - Deliverable: configured agent workflow; sample PR review.
  - Importance: Agents can automate repetitive dev flows; governance matters.
  - Objectives:
    - Configure agent workflows tied to issues and tests.
    - Explore MCP-backed context and extension capabilities.
  - Suggested Learning Aids:
    - Copilot Chat/Agents — https://docs.github.com/en/copilot/using-github-copilot/copilot-chat
    - Copilot Extensions — https://docs.github.com/en/copilot/extensions
    - Model Context Protocol — https://modelcontextprotocol.io/
- Days 13–15: Capstone Project
  - Build a full‑stack product:
    - PRD finalized.
    - Generate a REST API with Python FastAPI.
    - AI‑generated database schema and migrations.
    - AI‑created unit tests; security vulnerability identification.
    - SQL optimization using AI.
    - React frontend app for the API; components from design screenshots.
    - Demo of working front + back end.
  - Deliverables: repo with API, DB schema, tests, frontend, CI, documentation, and live demo.
  - Importance: Synthesize the full SDLC with GenAI, demonstrating end-to-end competency.
  - Objectives (by day):
    - Day 13: Finalize PRD and architecture; scaffold API and schema.
    - Day 14: Implement tests, run security checks, optimize SQL, build core UI.
    - Day 15: Wire CI/CD, polish docs, rehearse and deliver demo.
  - Suggested Learning Aids:
    - FastAPI — https://fastapi.tiangolo.com/
    - OWASP Top 10 — https://owasp.org/www-project-top-ten/ | OWASP API Top 10 (2023) — https://owasp.org/API-Security/editions/2023/en/0x11-t10/
    - Use The Index, Luke! — https://use-the-index-luke.com/
    - PostgreSQL EXPLAIN — https://www.postgresql.org/docs/current/using-explain.html
    - GitHub Actions — https://docs.github.com/en/actions

---

### Capstone Milestones and Rubric
- Milestones
  - Day 13: PRD, architecture, API scaffold, DB schema.
  - Day 14: Tests, security review, SQL optimization, core UI.
  - Day 15: CI/CD, docs, final polish, presentation.
- Rubric (100%)
  - Functionality and correctness: 25%
  - Effective GenAI usage across SDLC (prompt quality, context, traceability): 20%
  - Code quality and maintainability (readability, structure, typing): 15%
  - Test quality and coverage: 15%
  - Security posture (findings + mitigations): 10%
  - Performance/data efficiency (SQL optimization evidence): 5%
  - Documentation and presentation (README, runbooks, demo): 10%

### Assignments and Grading
- Participation and in‑class labs: 15%
- Weekly deliverables (Days 6–12): 35%
- Capstone project (per rubric): 50%
- Pass requirement: complete assessments and ≥70% overall.

### Readings and Resources
- LLM prompting guides; provider docs (OpenAI/Anthropic/OSS).
- GitHub Copilot and Agent documentation; MCP server guides.
- FastAPI, pytest, React official docs.
- Secure coding checklists (OWASP Top 10), SQL performance guides.

### Learning Aids and Resources
- **Prompt engineering**
  - [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)
  - [Anthropic Prompt Engineering](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering)
  - [Microsoft Prompt Engineering for Azure OpenAI](https://learn.microsoft.com/azure/ai-services/openai/concepts/prompt-engineering)
- **AI pair programming and Copilot**
  - [GitHub Copilot documentation](https://docs.github.com/en/copilot)
  - [Microsoft Learn: Copilot learning path](https://learn.microsoft.com/en-us/training/paths/copilot/)
  - [GitHub Skills: Getting started with Copilot](https://github.com/skills/getting-started-with-github-copilot)
  - [Sourcegraph Cody docs](https://docs.sourcegraph.com/cody)
  - [Cursor documentation](https://docs.cursor.com/)
- **Copilot Agent, MCP, and extensions**
  - [Copilot Chat and Agents overview](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat)
  - [Copilot Extensions](https://docs.github.com/en/copilot/extensions)
  - [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
- **Backend/API and testing**
  - [FastAPI](https://fastapi.tiangolo.com/)
  - [pytest](https://docs.pytest.org/en/stable/)
  - [coverage.py](https://coverage.readthedocs.io/)
  - [pytest-cov](https://pytest-cov.readthedocs.io/)
- **Frontend**
  - [React (new docs)](https://react.dev/learn)
  - [Vite Guide](https://vitejs.dev/guide/)
  - [Next.js Docs](https://nextjs.org/docs)
- **Diagrams and design**
  - [Mermaid](https://mermaid.js.org/)
  - [Mermaid Live Editor](https://mermaid.live/)
  - [PlantUML](https://plantuml.com/)
- **CI/CD and DevOps**
  - [GitHub Actions](https://docs.github.com/en/actions)
- **Security**
  - [OWASP Top 10 (Web)](https://owasp.org/www-project-top-ten/)
  - [OWASP API Security Top 10 (2023)](https://owasp.org/API-Security/editions/2023/en/0x11-t10/)
  - [GitHub CodeQL](https://docs.github.com/en/code-security/codeql)
  - [Dependabot](https://docs.github.com/en/code-security/dependabot)
  - [Semgrep Assistant](https://semgrep.dev/products/semgrep-assistant)
- **SQL optimization**
  - [Use The Index, Luke!](https://use-the-index-luke.com/)
  - [PostgreSQL EXPLAIN](https://www.postgresql.org/docs/current/using-explain.html)
- **Incident management and ops**
  - [Google SRE: Postmortem culture](https://sre.google/sre-book/postmortem-culture/)
  - [Incident runbook templates](https://incident.io/templates)
- **Product and planning**
  - [Atlassian PRD template](https://www.atlassian.com/agile/product-management/product-requirements)

### AI Usage Policy
- **Allowed**: Using LLMs/Copilot/Cursor/Cody for ideation, code gen, refactoring, tests, docs.
- **Required**: Log prompts and context used; cite AI‑generated content in PR descriptions or README “AI Usage” section.
- **Prohibited**: Submitting generated code without review, security scanning, or failing to attribute AI involvement.

### Logistics
- Modality: Daily 60–90 min lecture + 3–4 hr lab.
- Collaboration: Pair programming encouraged; individual accountability via prompt logs and PR history.
- Submission: GitHub PRs with CI checks; demo on Day 15.

### What to Submit (by Day)
- **Week 0**: Daily deliverables (reflections, screenshots, code files, prompts) uploaded to GitHub repo Week0 folder; final readiness checklist and reflection on Day 0.7.
- Day 6: PRD + backlog.
- Day 7: Architecture doc + UML.
- Day 8: API scaffold + README.
- Day 9: Test suite + coverage.
- Day 10: CI workflow + runbook/postmortem template.
- Days 11–12: Refactors, generated components, agent setup, sample PR review.
- Day 15: Final repo, demo recording/slides, "AI Usage" log.

Would you like a printable PDF version or a one‑page checklist version for instructors?