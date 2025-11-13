# GitHub Upload Instructions - Using Git Bash

## 📋 Prerequisites

Before you start, make sure you have:
- ✅ Git Bash installed (comes with Git for Windows)
- ✅ A GitHub account
- ✅ A repository created on GitHub (or create one at https://github.com/new)

## 🚀 Step-by-Step Guide: Push to GitHub using Git Bash

### Step 1: Open Git Bash

1. **Navigate to your project folder** in Windows Explorer:
   - Go to: `C:\Users\james\Desktop\AI-Enabled-Software-Engineering`

2. **Right-click** in the folder and select **"Git Bash Here"**
   - This opens Git Bash in your project directory
   - You should see a prompt like: `username@computer MINGW64 /c/Users/james/Desktop/AI-Enabled-Software-Engineering`

### Step 2: Check Current Status

First, let's see what files need to be committed:

```bash
git status
```

This shows you:
- Files that are already committed
- Files that are modified but not staged
- Files that are untracked (new files)

### Step 3: Add Files to Staging Area

Add all files you want to commit:

```bash
# Add all files (including new and modified)
git add .

# OR add specific files
git add filename.txt
```

**Verify what's staged:**
```bash
git status
```
Files in green are staged and ready to commit.

### Step 4: Commit Your Changes

Create a commit with a descriptive message:

```bash
git commit -m "Initial commit: AI-Enabled Software Engineering course materials"
```

**Good commit message examples:**
- `"Add Week 1 course materials"`
- `"Update README with setup instructions"`
- `"Fix typo in Week2 worksheet"`

### Step 5: Set Up Remote Repository (First Time Only)

If this is your first time pushing, you need to connect your local repository to GitHub:

```bash
# Replace with your actual GitHub username and repository name
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Verify the remote was added
git remote -v
```

**Example:**
```bash
git remote add origin https://github.com/WyrmSnack/AI-Enabled-Software-Engineering-Class.git
```

**If the remote already exists but points to wrong URL:**
```bash
git remote set-url origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

### Step 6: Create a Personal Access Token (Required for Authentication)

GitHub no longer accepts passwords for authentication. You need a Personal Access Token:

1. **Go to GitHub Settings:**
   - Visit: https://github.com/settings/tokens
   - Or: GitHub → Your Profile → Settings → Developer settings → Personal access tokens → Tokens (classic)

2. **Generate New Token:**
   - Click **"Generate new token"** → **"Generate new token (classic)"**
   - **Name:** `Git Bash Upload` (or any name you like)
   - **Expiration:** Choose your preference (90 days, 1 year, or no expiration)
   - **Select scopes:** Check the box for **`repo`** (this gives full repository access)
   - Click **"Generate token"** at the bottom

3. **⚠️ IMPORTANT:** Copy the token immediately!
   - It looks like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`
   - You won't be able to see it again!
   - Save it somewhere safe (password manager recommended)

### Step 7: Push to GitHub

Now push your code to GitHub:

```bash
# Push to main branch (first time)
git push -u origin main

# For subsequent pushes, you can just use:
git push
```

**When prompted:**
- **Username:** Enter your GitHub username (e.g., `WyrmSnack`)
- **Password:** Paste your Personal Access Token (NOT your GitHub password)

**Note:** Git Bash may not show characters as you type the token - this is normal for security.

### Step 8: Verify Success

After pushing, you should see:
```
Enumerating objects: X, done.
Counting objects: 100% (X/X), done.
Writing objects: 100% (X/X), done.
To https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

Visit your repository on GitHub to confirm all files are there!

## 🔄 Common Git Bash Commands Reference

### Daily Workflow

```bash
# Check status
git status

# Add files
git add .                    # Add all files
git add filename.txt         # Add specific file

# Commit changes
git commit -m "Your message"

# Push to GitHub
git push

# Pull latest changes
git pull
```

### Viewing Information

```bash
# View commit history
git log

# View changes in files
git diff

# View remote repository info
git remote -v
```

### Branch Management

```bash
# Create new branch
git checkout -b new-branch-name

# Switch branches
git checkout branch-name

# List all branches
git branch -a
```

## 🔐 Authentication Options

### Option 1: Personal Access Token (Recommended)
- Use the token as your password when pushing
- Works with HTTPS URLs
- Token expires based on your settings

### Option 2: SSH Keys (More Secure, One-Time Setup)
If you prefer SSH authentication:

1. **Generate SSH key in Git Bash:**
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   # Press Enter to accept default location
   # Enter a passphrase (optional but recommended)
   ```

2. **Copy your public key:**
   ```bash
   cat ~/.ssh/id_ed25519.pub
   # Copy the entire output
   ```

3. **Add to GitHub:**
   - Go to: https://github.com/settings/keys
   - Click "New SSH key"
   - Paste your public key
   - Save

4. **Change remote URL to SSH:**
   ```bash
   git remote set-url origin git@github.com:YOUR_USERNAME/YOUR_REPO_NAME.git
   ```

5. **Test connection:**
   ```bash
   ssh -T git@github.com
   ```

### Option 3: GitHub CLI
If you have GitHub CLI installed:
```bash
gh auth login
git push -u origin main
```

## ❓ Troubleshooting

### "Authentication failed" Error
- ✅ Make sure you're using a **Personal Access Token**, not your GitHub password
- ✅ Verify the token has `repo` scope checked
- ✅ Check that the token hasn't expired
- ✅ Try generating a new token

### "Permission denied" Error
- ✅ Verify you have write access to the repository
- ✅ Check that the repository URL is correct
- ✅ Make sure you're logged into the correct GitHub account
- ✅ If it's not your repository, you need to fork it first

### "Repository not found" Error
- ✅ Make sure the repository exists on GitHub
- ✅ Verify the repository name and username are correct
- ✅ Check that the repository isn't private and you don't have access (if it is)

### "Branch 'main' does not exist" Error
- ✅ Check your current branch: `git branch`
- ✅ If you're on a different branch, either:
  - Push that branch: `git push -u origin your-branch-name`
  - Or switch to main: `git checkout main`

### Files Not Showing Up
- ✅ Make sure you've added files: `git add .`
- ✅ Make sure you've committed: `git commit -m "message"`
- ✅ Make sure you've pushed: `git push`

## 📝 Current Status

- **Repository:** https://github.com/WyrmSnack/AI-Enabled-Software-Engineering-Class
- **Branch:** `main`
- **Status:** Ready to push (just needs authentication)

## 🎯 Quick Start Checklist

- [ ] Open Git Bash in project folder
- [ ] Run `git status` to see what needs to be committed
- [ ] Run `git add .` to stage all files
- [ ] Run `git commit -m "Your message"` to commit
- [ ] Create Personal Access Token on GitHub
- [ ] Run `git push -u origin main` to push
- [ ] Enter username and token when prompted
- [ ] Verify files appear on GitHub

---

**💡 Tip:** After your first push, you can use `git push` without the `-u origin main` part for future updates!

