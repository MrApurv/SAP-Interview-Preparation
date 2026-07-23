# 05-Merge.md

# Git Merge

---

# What is Merge?

Merge combines changes from one branch into another.

Example

```

feature/login

↓

main

```

---

# Why Merge?

After completing development, feature branches are merged into the main branch.

---

# Merge Process

```

Create Feature

↓

Commit

↓

Push

↓

Pull Request

↓

Review

↓

Merge

↓

Delete Branch

```

---

# Merge Command

Switch to main

```bash
git checkout main
```

Pull latest

```bash
git pull origin main
```

Merge

```bash
git merge feature/login
```

Push

```bash
git push origin main
```

---

# Merge Conflict

Occurs when two developers modify the same lines of code.

Example

Developer A

```
Button Color = Blue
```

Developer B

```
Button Color = Red
```

Git cannot decide which change to keep.

Developer must resolve it manually.

---

# Resolve Conflict

1. Open conflicted file

2. Edit manually

3. Save

4. Stage

```bash
git add .
```

5. Commit

```bash
git commit
```

6. Push

```bash
git push
```

---

# Fast Forward Merge

Occurs when no new commits exist on the target branch.

Git simply moves the branch pointer forward.

---

# Three-Way Merge

Occurs when both branches contain different commits.

Git combines histories into a new merge commit.

---

# Real-Time Example

WorkSphere

```
feature/initial-ui5-setup

↓

Pull Request

↓

Merge into main

↓

Delete Branch
```

This is the merge strategy followed during the project.

---

# Best Practices

✔ Pull latest changes before merging

✔ Resolve conflicts carefully

✔ Test after merge

✔ Delete merged branches

---

# Interview Questions

## What is Git Merge?

Git Merge combines changes from one branch into another.

---

## What is Merge Conflict?

A merge conflict occurs when Git cannot automatically combine changes.

---

## How do you resolve Merge Conflicts?

Edit conflicted files manually, stage the changes, commit, and push.

---

## Difference between Fast Forward Merge and Three-Way Merge?

Fast Forward moves the branch pointer directly.

Three-Way Merge creates a new merge commit.

---

# Quick Revision

Merge = Combine branches

Conflict = Same code changed

Fast Forward = No divergence

Three-Way = Diverged histories
