# 03-Git-Workflow.md

# Git Workflow

---

# What is Git Workflow?

Git Workflow is the standard process developers follow to track, commit, review, and merge changes in a project.

A proper workflow ensures:

- Better collaboration
- Code quality
- Easy rollback
- Organized development
- Fewer merge conflicts

---

# Standard Git Workflow

```

Create Feature

↓

git status

↓

git add .

↓

git commit

↓

git push

↓

Create Pull Request

↓

Code Review

↓

Merge

↓

git pull

```

---

# Step 1 - Clone Repository

Clone the project from GitHub.

```bash
git clone git@github.com:username/project.git
```

---

# Step 2 - Create a Feature Branch

Never work directly on the main branch.

```bash
git checkout -b feature/login
```

---

# Step 3 - Make Changes

Examples

- Create new page
- Fix bug
- Add feature
- Update documentation

---

# Step 4 - Check Status

```bash
git status
```

Always check modified files before committing.

---

# Step 5 - Stage Changes

```bash
git add .
```

Or

```bash
git add filename
```

---

# Step 6 - Commit

```bash
git commit -m "feat(login): create login page"
```

A commit should represent one logical change.

---

# Step 7 - Push Changes

```bash
git push origin feature/login
```

---

# Step 8 - Create Pull Request

Create a Pull Request on GitHub.

Purpose:

- Code Review
- Team Discussion
- Approval

---

# Step 9 - Merge

After approval:

```
feature/login

↓

main
```

---

# Step 10 - Pull Latest Changes

```bash
git checkout main

git pull origin main
```

Always update your local main branch.

---

# Real-Time Example (WorkSphere)

```
main

↓

feature/initial-ui5-app

↓

feature/initial-ui5-setup

↓

Create Pull Request

↓

Merge

↓

Delete Branch
```

This is exactly the workflow followed during the WorkSphere project.

---

# Best Practices

✅ Small commits

✅ Meaningful commit messages

✅ Pull before pushing

✅ Never commit unnecessary files

✅ Keep branches short-lived

---

# Interview Questions

## What is Git Workflow?

Git Workflow is a structured process that developers follow to develop, review, and merge code efficiently.

---

## Why create a feature branch?

Feature branches isolate development, reduce conflicts, and allow safe code reviews.

---

## Why create Pull Requests?

To review code before merging into the main branch.

---

## What should you do before pushing?

- Check status
- Review changes
- Pull latest changes
- Resolve conflicts if any

---

# Quick Revision

Feature → Commit → Push → Pull Request → Review → Merge