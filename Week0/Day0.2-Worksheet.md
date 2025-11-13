# Day 0.2 Worksheet: GitHub & Project Workflow

**Estimated Time**: 1–2 hours  
**Focus**: Understanding GitHub, version control, and collaboration basics

---

## Learning Objectives

By the end of this session, you will be able to:
- Understand what GitHub is and why teams use it
- Learn key terms: repository, commit, branch, pull request
- Create your first repository and make a commit
- Practice contributing to code without fear

---

## Pre-Activity: Understanding Version Control

**Question**: Why do developers use version control systems like Git?

Think about this scenario: You're writing a document, and you want to:
- Save different versions
- See what changed between versions
- Work on multiple versions at once
- Collaborate with others without overwriting each other's work

**Your thoughts**:
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 1: Create a GitHub Account

**Steps**:
1. Go to [github.com](https://github.com)
2. Click "Sign up"
3. Choose a username (this will be part of your profile URL)
4. Enter your email and create a password
5. Verify your email address

**After creating your account, fill in**:
- GitHub username: _________________________
- Profile URL: https://github.com/_________________________

---

## Activity 2: Complete GitHub Skills Tutorial

**Resource**: [GitHub Skills – Introduction to GitHub](https://github.com/skills/introduction-to-github)

**Instructions**: 
1. Click "Start course" on the GitHub Skills page
2. Complete all lessons in the tutorial
3. Take notes on key concepts as you go

**Key Terms to Learn** (define each as you encounter them):

| Term | Definition | Example/Use Case |
|------|------------|------------------|
| Repository (repo) | | |
| Commit | | |
| Branch | | |
| Pull Request (PR) | | |
| Fork | | |
| Clone | | |

**Notes from the tutorial**:
_______________________________________________________________________
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 3: Create Your First Repository

**Steps**:
1. On GitHub, click the "+" icon in the top right → "New repository"
2. Name it: `week0-practice` (or similar)
3. Add a description: "Practice repository for Week 0"
4. Make it **Public** (for now, so you can share it easily)
5. **Do NOT** initialize with README, .gitignore, or license (we'll add files manually)
6. Click "Create repository"

**Repository URL**: https://github.com/_________________________/_________________________

---

## Activity 4: Make Your First Commit

**Option A: Using GitHub Web Interface**
1. In your new repository, click "creating a new file"
2. Name the file: `hello.txt`
3. Add some content, for example:
   ```
   Hello, GitHub!
   This is my first file in this repository.
   Created on [today's date]
   ```
4. Scroll down and click "Commit new file"
5. Write a commit message: "Add hello.txt file"
6. Click "Commit new file"

**Option B: Using Command Line (if you're comfortable)**
```bash
# Navigate to a folder on your computer
cd ~/Desktop  # or wherever you want to work

# Clone your repository (replace with your username and repo name)
git clone https://github.com/YOUR_USERNAME/week0-practice.git
cd week0-practice

# Create and edit the file
echo "Hello, GitHub!" > hello.txt
echo "This is my first file in this repository." >> hello.txt

# Stage the file
git add hello.txt

# Commit the file
git commit -m "Add hello.txt file"

# Push to GitHub
git push origin main
```

**Which method did you use?** [ ] Web Interface [ ] Command Line

---

## Activity 5: Explore Your Repository

After making your commit, explore your repository page:

1. **Find your commit**:
   - Look for the commit message you wrote
   - Click on it to see what changed

2. **Check the file**:
   - Click on `hello.txt` to view it
   - Notice the file viewer interface

3. **Take a screenshot**:
   - Capture your repository page showing:
     - The repository name
     - Your `hello.txt` file
     - At least one commit visible
   - Save it as `Day0.2-Repository-Screenshot.png`

**Screenshot saved?** [ ] Yes

---

## Activity 6: Understanding Collaboration Workflow

**Scenario**: You're working on a team project. Someone else wants to add a feature.

**Match the workflow steps** (draw lines or number them):

1. **Fork/Clone** → Get a copy of the project
2. **Create Branch** → Work on changes without affecting main code
3. **Make Changes** → Edit files, add features
4. **Commit** → Save your changes with a message
5. **Push** → Upload your changes to GitHub
6. **Pull Request** → Ask to merge your changes into the main project
7. **Review** → Team members review your code
8. **Merge** → Approved changes are combined into main

**Why use branches instead of editing main directly?**
_______________________________________________________________________
_______________________________________________________________________

---

## Activity 7: Practice Exercise

**Task**: Add another file to your repository

1. Create a file called `about-me.txt`
2. Write 3–4 sentences about:
   - Your background
   - Why you're taking this course
   - What you hope to learn
3. Commit this file with a descriptive commit message

**Example commit message**: "Add about-me.txt with introduction"

**Your commit message**: _________________________________________________

---

## Deliverable Checklist

- [ ] Created GitHub account
- [ ] Completed GitHub Skills tutorial
- [ ] Created first repository
- [ ] Made first commit (hello.txt)
- [ ] Took screenshot of repository page
- [ ] Added about-me.txt file
- [ ] Committed about-me.txt
- [ ] Saved screenshot as `Day0.2-Repository-Screenshot.png` in Week0 folder

---

## Reflection Questions

1. **What was the most confusing part of using GitHub?**
   _______________________________________________________________________

2. **What questions do you still have about version control?**
   _______________________________________________________________________

3. **How do you think GitHub will help you in this course?**
   _______________________________________________________________________

---

## Additional Resources (Optional)

- [GitHub Docs: Getting Started](https://docs.github.com/en/get-started)
- [GitHub Guides: Understanding the GitHub Flow](https://guides.github.com/introduction/flow/)
- [Visual Git Guide](https://marklodato.github.io/visual-git-guide/index-en.html)

---

## Troubleshooting

**Common Issues**:

- **"Repository not found"**: Make sure you're logged into the correct GitHub account
- **"Permission denied"**: Check that you have write access to the repository
- **Can't see commits**: Refresh the page or check you're on the correct branch

**Need help?** Note your issue here:
_______________________________________________________________________
_______________________________________________________________________

---

## Next Steps

Tomorrow (Day 0.3), you'll learn Python fundamentals. Make sure you have:
- Python 3.11+ installed (check with `python --version` or `python3 --version`)
- VS Code or Cursor installed (or ready to install)

