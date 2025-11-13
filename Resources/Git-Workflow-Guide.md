# Git Workflow Guide

Best practices for using Git and GitHub in this course.

## Basic Git Concepts

### Repository (Repo)
A folder containing your project and its version history.

### Commit
A snapshot of your code at a specific point in time.

### Branch
A parallel version of your code where you can make changes.

### Pull Request (PR)
A request to merge changes from one branch into another.

---

## Branch Naming Conventions

### Format
`<type>/<description>`

### Types
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation
- `test/` - Tests
- `refactor/` - Code refactoring
- `chore/` - Maintenance tasks

### Examples
- `feature/user-authentication`
- `fix/login-error`
- `docs/api-documentation`
- `test/user-endpoints`

---

## Commit Message Standards

### Format
```
<type>: <subject>

<body>

<footer>
```

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting
- `refactor`: Code refactoring
- `test`: Tests
- `chore`: Maintenance

### Examples

**Good**:
```
feat: add user authentication endpoint

- Implement JWT token generation
- Add password hashing
- Create login and register endpoints

Closes #123
```

**Bad**:
```
fixed stuff
```

### Guidelines
- Use imperative mood ("add" not "added")
- Keep subject line under 50 characters
- Capitalize first letter
- No period at end
- Reference issues/PRs in footer

---

## Workflow Steps

### 1. Create a Branch
```bash
git checkout -b feature/new-feature
# or
git switch -c feature/new-feature
```

### 2. Make Changes
- Edit files
- Test your changes
- Commit frequently

### 3. Commit Changes
```bash
git add .
git commit -m "feat: add new feature"
```

### 4. Push to GitHub
```bash
git push origin feature/new-feature
```

### 5. Create Pull Request
- Go to GitHub
- Click "New Pull Request"
- Fill out PR template
- Request review

### 6. Address Feedback
- Make requested changes
- Push updates
- PR updates automatically

### 7. Merge
- After approval, merge PR
- Delete branch (optional)
- Update local main branch

---

## Pull Request Template

Use this template for all PRs:

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation
- [ ] Refactoring
- [ ] Other

## Changes Made
- Change 1
- Change 2
- Change 3

## Testing
- [ ] Tests added/updated
- [ ] Manual testing completed
- [ ] All tests passing

## AI Usage
- [ ] AI tools used
- [ ] Prompts documented
- [ ] Code reviewed

## Screenshots (if applicable)
[Add screenshots]

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] No new warnings
```

---

## Code Review Checklist

### For Reviewers
- [ ] Code works as intended
- [ ] Code is readable
- [ ] Tests are present
- [ ] Documentation updated
- [ ] No security issues
- [ ] AI usage documented
- [ ] Follows best practices

### For Authors
- [ ] Self-reviewed code
- [ ] Tests written
- [ ] Documentation updated
- [ ] PR description complete
- [ ] Ready for review

---

## Common Git Commands

### Basic
```bash
# Check status
git status

# Add files
git add <file>
git add .

# Commit
git commit -m "message"

# Push
git push origin <branch>

# Pull
git pull origin <branch>
```

### Branching
```bash
# Create branch
git checkout -b <branch-name>

# Switch branch
git checkout <branch-name>
git switch <branch-name>

# List branches
git branch

# Delete branch
git branch -d <branch-name>
```

### Merging
```bash
# Merge branch into current
git merge <branch-name>

# Rebase (advanced)
git rebase <branch-name>
```

### Undoing
```bash
# Unstage files
git reset <file>

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes)
git reset --hard HEAD~1

# Revert a commit
git revert <commit-hash>
```

---

## Best Practices

### Do's
✅ Commit frequently with clear messages
✅ Create branches for features
✅ Test before committing
✅ Write meaningful commit messages
✅ Keep branches up to date
✅ Review your own code before PR
✅ Use PRs for all changes

### Don'ts
❌ Commit directly to main/master
❌ Commit broken code
❌ Write vague commit messages
❌ Commit large files
❌ Force push to shared branches
❌ Skip code review
❌ Commit secrets/credentials

---

## Troubleshooting

### Merge Conflicts
1. Pull latest changes: `git pull origin main`
2. Resolve conflicts in files
3. Stage resolved files: `git add .`
4. Complete merge: `git commit`

### Undo Last Commit
```bash
# Keep changes
git reset --soft HEAD~1

# Discard changes
git reset --hard HEAD~1
```

### Recover Deleted Branch
```bash
git reflog
git checkout -b <branch-name> <commit-hash>
```

---

## Collaboration Patterns

### Pair Programming with Git
1. One person creates branch
2. Both work on same branch
3. Commit frequently
4. Push and pull regularly
5. Communicate changes

### Feature Branch Workflow
1. Create feature branch from main
2. Develop feature
3. Create PR when ready
4. Get review and approval
5. Merge to main
6. Deploy from main

---

## AI-Assisted Git Workflow

### Using AI for Commit Messages
```
Generate a commit message for these changes:
[Paste git diff]
```

### Using AI for PR Descriptions
```
Create a PR description for this branch:
[Describe changes]
```

### Using AI for Code Review
```
Review this code for:
- Security issues
- Best practices
- Potential bugs
[Paste code]
```

---

## Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)

---

## Remember

- Git is a tool for collaboration
- Good commits tell a story
- PRs are for discussion, not just merging
- Review is a learning opportunity
- Use AI to help, but understand what you're committing

