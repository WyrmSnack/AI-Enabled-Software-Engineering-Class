# Git Cheat Sheet

Quick reference for Git commands.

## Basic
```bash
git status
git add <file>
git add .
git commit -m "message"
git push
git pull
```

## Branching
```bash
git branch
git branch <name>
git checkout <branch>
git checkout -b <branch>
git merge <branch>
```

## History
```bash
git log
git log --oneline
git log --graph
git show <commit>
```

## Undoing
```bash
git reset <file>
git reset --soft HEAD~1
git reset --hard HEAD~1
git revert <commit>
```

## Remote
```bash
git remote -v
git remote add origin <url>
git push -u origin <branch>
git fetch
git pull origin <branch>
```

## Stashing
```bash
git stash
git stash list
git stash apply
git stash drop
```

