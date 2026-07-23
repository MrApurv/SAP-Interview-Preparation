# 04-Branching.md

# Git Branching

---

# What is a Branch?

A branch is an independent line of development.

It allows developers to work on new features without affecting the main codebase.

---

# Why Branches?

Without branches

```

Everyone edits main

↓

Conflicts

↓

Broken Project

```

With branches

```

main

├── feature/login

├── feature/dashboard

├── feature/profile

└── bugfix/navbar

```

Each developer works independently.

---

# Main Branch

The main branch contains stable production-ready code.

Never experiment directly on main.

---

# Feature Branch

Created for new features.

Example

```
feature/login

feature/dashboard

feature/payment

feature/profile
```

---

# Bug Fix Branch

Created for fixing issues.

Example

```
bugfix/login

bugfix/api

bugfix/header
```

---

# Hotfix Branch

Used to fix production issues immediately.

Example

```
hotfix/payment

hotfix/security
```

---

# Create Branch

```bash
git checkout -b feature/login
```

---

# View Branches

```bash
git branch
```

---

# Switch Branch

```bash
git checkout main
```

---

# Delete Branch

Local

```bash
git branch -d feature/login
```

Remote

```bash
git push origin --delete feature/login
```

---

# Real-Time Example

WorkSphere

```
main

↓

feature/initial-ui5-app

↓

feature/initial-ui5-setup

↓

Merge

↓

Delete Branch
```

---

# Best Practices

✔ One feature per branch

✔ Short-lived branches

✔ Merge frequently

✔ Delete merged branches

---

# Interview Questions

## What is a Git Branch?

A branch is an independent line of development.

---

## Why use feature branches?

To isolate changes and reduce conflicts.

---

## Difference between Main and Feature Branch?

Main contains stable code.

Feature branches contain ongoing development.

---

## Which branch should never be used for experiments?

main

---

# Quick Revision

Branch = Independent development

Main = Stable

Feature = New functionality

Bugfix = Error correction

Hotfix = Production issue