# Course Setup Guide

## Prerequisites Checklist

Before starting the course, ensure you have:

- [ ] Python 3.11+ installed
- [ ] Git installed
- [ ] GitHub account created
- [ ] IDE installed (VS Code or Cursor)
- [ ] Node.js installed (for frontend work)
- [ ] Database installed (PostgreSQL or SQLite)

---

## Step 1: Python Environment

### Install Python

**Windows**:
1. Download from [python.org](https://www.python.org/downloads/)
2. Run installer
3. Check "Add Python to PATH"
4. Verify: `python --version`

**Mac**:
```bash
brew install python3
python3 --version
```

**Linux**:
```bash
sudo apt-get update
sudo apt-get install python3.11
python3 --version
```

### Create Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Mac/Linux)
source venv/bin/activate
```

---

## Step 2: Install Required Packages

```bash
# Install core packages
pip install fastapi uvicorn sqlalchemy alembic pydantic

# Install testing
pip install pytest pytest-cov httpx

# Install code quality
pip install black flake8 mypy

# Install frontend dependencies (if needed)
npm install
```

---

## Step 3: Git and GitHub

### Install Git

**Windows**: Download from [git-scm.com](https://git-scm.com/)  
**Mac**: `brew install git`  
**Linux**: `sudo apt-get install git`

### Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Set Up GitHub

1. Create account at [github.com](https://github.com)
2. Generate SSH key (optional but recommended)
3. Clone course repository (when provided)

---

## Step 4: IDE Setup

### VS Code

1. Download from [code.visualstudio.com](https://code.visualstudio.com/)
2. Install Python extension
3. Install GitHub Copilot extension (if available)
4. Configure Python interpreter (Ctrl+Shift+P → "Python: Select Interpreter")

### Cursor

1. Download from [cursor.com](https://cursor.com/)
2. Install Python support
3. Enable AI features
4. Configure Python interpreter

---

## Step 5: Database Setup

### SQLite (Easiest for Development)

**No installation needed** - comes with Python!

**Test**:
```python
import sqlite3
conn = sqlite3.connect('test.db')
print("SQLite working!")
```

### PostgreSQL (For Production-like Environment)

**Windows**: Download from [postgresql.org](https://www.postgresql.org/download/windows/)  
**Mac**: `brew install postgresql`  
**Linux**: `sudo apt-get install postgresql`

**Create database**:
```bash
createdb myapp
psql myapp
```

---

## Step 6: Frontend Setup (Week 3)

### Install Node.js

Download from [nodejs.org](https://nodejs.org/)

**Verify**:
```bash
node --version
npm --version
```

### Create React App

```bash
# Using Vite
npm create vite@latest my-app -- --template react

# Or using Next.js
npx create-next-app@latest my-app
```

---

## Step 7: GitHub Copilot (If Available)

### Enable Copilot

1. Sign in to GitHub
2. Install Copilot extension in IDE
3. Authorize in IDE
4. Test with a comment: `# Create a hello world function`

---

## Step 8: Verify Setup

### Run This Checklist

```bash
# Python
python --version  # Should show 3.11+

# FastAPI
python -c "import fastapi; print('FastAPI OK')"

# pytest
python -c "import pytest; print('pytest OK')"

# Git
git --version

# Node (if doing frontend)
node --version
npm --version
```

**All checks passing?** [ ] Yes

---

## Troubleshooting

### Python Not Found
- **Windows**: Add Python to PATH
- **Mac/Linux**: Use `python3` instead of `python`

### Package Installation Fails
- Upgrade pip: `python -m pip install --upgrade pip`
- Use virtual environment
- Check internet connection

### Git Authentication Issues
- Set up SSH keys
- Or use HTTPS with personal access token

### IDE Not Recognizing Python
- Select correct interpreter
- Restart IDE
- Check Python extension installed

---

## Getting Help

1. Check worksheet troubleshooting sections
2. Review Resources/ folder
3. Ask in course forums
4. Contact instructor

---

## Next Steps

Once setup is complete:
1. Complete Week 0 worksheets
2. Verify all tools work
3. Start Week 1 assessments

**You're ready to go!** 🚀

