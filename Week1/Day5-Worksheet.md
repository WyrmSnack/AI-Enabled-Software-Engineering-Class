# Week 1, Day 5 Worksheet: Vendor Kickoff

**Estimated Time**: 2–3 hours (including kickoff session)  
**Focus**: Align expectations, confirm access, establish project logistics and conventions

---

## Learning Objectives

By the end of Day 5, you will be able to:
- Confirm access to all required platforms and tools
- Understand course project structure and conventions
- Know repository, branching, and CI/CD conventions
- Identify any blockers and get them resolved
- Be ready to start hands-on work in Week 2

---

## Pre-Kickoff: Preparation Checklist

**Before the kickoff session, ensure**:

- [ ] All Week 1 assessments completed
- [ ] Career manager approval obtained
- [ ] GitHub account active and accessible
- [ ] IDE (VS Code/Cursor) installed and configured
- [ ] Python 3.11+ installed and verified
- [ ] FastAPI and pytest installed
- [ ] Questions prepared (see below)

**Questions to ask during kickoff**:
1. _______________________________________________________________________
2. _______________________________________________________________________
3. _______________________________________________________________________

---

## Activity 1: Kickoff Session Participation

### During the Kickoff

**Key topics to listen for and take notes**:

#### Platform Access
- **GitHub**: 
  - Repository structure: _______________________________________________________________________
  - Access method: _______________________________________________________________________
  - Organization/team: _______________________________________________________________________

- **Learning Platform**:
  - URL: _______________________________________________________________________
  - Login credentials: _______________________________________________________________________
  - Where to find materials: _______________________________________________________________________

- **Vendor Sites**:
  - Required sites: _______________________________________________________________________
  - Access methods: _______________________________________________________________________
  - Any special setup: _______________________________________________________________________

#### Project Logistics

**Repository Conventions**:
- Naming conventions: _______________________________________________________________________
- Branch naming: _______________________________________________________________________
- Commit message format: _______________________________________________________________________
- PR process: _______________________________________________________________________

**Branching Strategy**:
- Main/master branch: _______________________________________________________________________
- Feature branches: _______________________________________________________________________
- How to create branches: _______________________________________________________________________
- Merge process: _______________________________________________________________________

**CI/CD Conventions**:
- What CI checks are required: _______________________________________________________________________
- How to set up GitHub Actions: _______________________________________________________________________
- Testing requirements: _______________________________________________________________________

**Communication Channels**:
- Primary communication: _______________________________________________________________________
- Office hours/support: _______________________________________________________________________
- Emergency contacts: _______________________________________________________________________

**Submission Process**:
- How to submit deliverables: _______________________________________________________________________
- PR requirements: _______________________________________________________________________
- Due dates/timing: _______________________________________________________________________

**Notes from kickoff**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 2: Access Validation

### Validate All Platform Access

#### GitHub Access

**Test 1: Login and Navigation**
- [ ] Can log into GitHub
- [ ] Can see course organization/team
- [ ] Can access course repository

**Test 2: Repository Operations**
- [ ] Can clone repository: `git clone [repo-url]`
- [ ] Can create a new branch: `git checkout -b test-branch`
- [ ] Can make a commit
- [ ] Can push to repository: `git push origin test-branch`

**Test 3: Pull Requests**
- [ ] Understand how to create a PR
- [ ] Know what information to include in PR description
- [ ] Understand review process

**GitHub Issues Encountered**:
_______________________________________________________________________
_______________________________________________________________________

#### Learning Platform Access

**Test 1: Login**
- [ ] Can log into learning platform
- [ ] Can see course dashboard
- [ ] Can access course materials

**Test 2: Navigation**
- [ ] Can find Week 2 materials
- [ ] Can access worksheets
- [ ] Can see assignment instructions

**Learning Platform Issues**:
_______________________________________________________________________
_______________________________________________________________________

#### Development Environment

**Test 1: IDE Setup**
- [ ] VS Code or Cursor opens without errors
- [ ] Python extension works
- [ ] GitHub Copilot enabled (if available)
- [ ] Can open course repository in IDE

**Test 2: Python Environment**
```bash
python --version  # Should show 3.11+
python -c "import fastapi; print('FastAPI OK')"
python -c "import pytest; print('pytest OK')"
```

**Results**:
- Python version: _________________________
- FastAPI: [ ] Working [ ] Not working
- pytest: [ ] Working [ ] Not working

**Test 3: Git Integration**
- [ ] Git is accessible from terminal/command line
- [ ] Can run `git status` in repository
- [ ] IDE shows Git status correctly

**Development Environment Issues**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 3: Repository Setup

### Clone and Explore Course Repository

**Step 1: Clone Repository**
```bash
# Navigate to where you want the repo
cd ~/Desktop  # or your preferred location

# Clone the repository (use URL from kickoff)
git clone [repository-url]
cd [repository-name]
```

**Repository cloned?** [ ] Yes  
**Location**: _______________________________________________________________________

**Step 2: Explore Repository Structure**

**What's in the repository?**
- [ ] README.md
- [ ] .gitignore
- [ ] Project folders
- [ ] Configuration files
- [ ] Other: _______________________________________________________________________

**Repository structure** (draw or describe):
```
[repository-name]/
├── 
├── 
├── 
└── 
```

**Step 3: Create Your First Branch**

```bash
# Create a branch for your work
git checkout -b week1-setup

# Make a small change (create a file)
echo "# Week 1 Setup" > week1-setup.md

# Commit the change
git add week1-setup.md
git commit -m "Add week1-setup.md"

# Push to GitHub
git push origin week1-setup
```

**Branch created?** [ ] Yes  
**Branch name**: _________________________

**Step 4: Create Your First PR (Practice)**

- [ ] Go to GitHub web interface
- [ ] Create a pull request from your branch
- [ ] Add a description
- [ ] Submit (or just practice, then close)

**PR created?** [ ] Yes [ ] Practiced only

---

## Activity 4: Understand Project Conventions

### Document Conventions from Kickoff

**Branch Naming**:
- Format: _______________________________________________________________________
- Examples: _______________________________________________________________________

**Commit Messages**:
- Format: _______________________________________________________________________
- Examples: _______________________________________________________________________

**PR Descriptions**:
- Required sections: _______________________________________________________________________
- Template: _______________________________________________________________________

**File Structure**:
- Where to put deliverables: _______________________________________________________________________
- Naming conventions: _______________________________________________________________________

**Code Standards**:
- Python style guide: _______________________________________________________________________
- Documentation requirements: _______________________________________________________________________
- Testing requirements: _______________________________________________________________________

**AI Usage Documentation**:
- How to document AI assistance: _______________________________________________________________________
- Where to log prompts: _______________________________________________________________________
- Attribution requirements: _______________________________________________________________________

---

## Activity 5: Identify and Resolve Blockers

### Blocker Identification

**Access Blockers**:
- [ ] GitHub access issues
- [ ] Learning platform access issues
- [ ] Development environment issues
- [ ] Other: _______________________________________________________________________

**Knowledge Blockers**:
- [ ] Unclear about project structure
- [ ] Unclear about submission process
- [ ] Unclear about expectations
- [ ] Other: _______________________________________________________________________

**Technical Blockers**:
- [ ] Can't install required tools
- [ ] Environment setup problems
- [ ] Configuration issues
- [ ] Other: _______________________________________________________________________

### Resolution Plan

**For each blocker, create a resolution plan**:

**Blocker 1**: _______________________________________________________________________
**Resolution**: _______________________________________________________________________
**Who to contact**: _______________________________________________________________________
**Timeline**: _______________________________________________________________________

**Blocker 2**: _______________________________________________________________________
**Resolution**: _______________________________________________________________________
**Who to contact**: _______________________________________________________________________
**Timeline**: _______________________________________________________________________

**Blocker 3**: _______________________________________________________________________
**Resolution**: _______________________________________________________________________
**Who to contact**: _______________________________________________________________________
**Timeline**: _______________________________________________________________________

---

## Activity 6: Week 2 Preparation

### Review Week 2 Expectations

**What's coming in Week 2**:
- **Day 6**: Planning & Requirements (PRD, user stories)
- **Day 7**: Design & Architecture (UML diagrams)
- **Day 8**: Development & Coding (FastAPI scaffold)
- **Day 9**: Testing & QA (pytest, coverage)
- **Day 10**: Deployment & Maintenance (CI/CD, runbooks)

**What you need**:
- [ ] All access confirmed
- [ ] Repository cloned and ready
- [ ] Development environment working
- [ ] Understanding of project conventions
- [ ] No unresolved blockers

**Questions before Week 2**:
_______________________________________________________________________
_______________________________________________________________________

### Set Up Your Workspace

**Create project structure** (if not provided):
```bash
# In your repository
mkdir -p week2/day6-requirements
mkdir -p week2/day7-architecture
mkdir -p week2/day8-development
mkdir -p week2/day9-testing
mkdir -p week2/day10-deployment
```

**Workspace ready?** [ ] Yes

---

## Deliverable Checklist

- [ ] Attended vendor kickoff session
- [ ] Took notes on all key topics
- [ ] Validated GitHub access and can clone repository
- [ ] Validated learning platform access
- [ ] Development environment verified (Python, FastAPI, pytest)
- [ ] Created first branch and made test commit
- [ ] Understood repository conventions
- [ ] Understood branching strategy
- [ ] Understood CI/CD requirements
- [ ] Identified and documented any blockers
- [ ] Created resolution plans for blockers
- [ ] Ready for Week 2

---

## Reflection Questions

1. **What was the most valuable information from the kickoff?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What questions do you still have?**
   _______________________________________________________________________
   _______________________________________________________________________

3. **What are you most excited about for Week 2?**
   _______________________________________________________________________

4. **What concerns do you have?**
   _______________________________________________________________________

---

## Troubleshooting

**Common Issues**:

- **Can't clone repository**: Check access permissions, verify URL, contact administrator
- **Git authentication errors**: Set up SSH keys or use HTTPS with personal access token
- **Python/FastAPI import errors**: Verify virtual environment, reinstall packages
- **IDE not recognizing Git**: Check Git installation, restart IDE

**Issues encountered and resolved**:
_______________________________________________________________________
_______________________________________________________________________

---

## Additional Resources

- [GitHub Getting Started](https://docs.github.com/en/get-started)
- [GitHub Actions Overview](https://docs.github.com/en/actions)
- [Git Branching Basics](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows)
- [FastAPI Tutorial](https://fastapi.tiangolo.com/)

---

## Next Steps

**You're ready for Week 2!** 

Tomorrow (Day 6), you'll start with Planning & Requirements. Make sure you:
- Have all access confirmed
- Repository is ready
- Development environment is working
- No unresolved blockers

**Let's build something amazing!** 🚀

