# Git Basics

---

# What is Git?

Git is a Distributed Version Control System (DVCS) used to track changes in source code during software development.

It allows multiple developers to work on the same project simultaneously while maintaining a complete history of every change.

Git was created by **Linus Torvalds** in 2005.

---

# Why Git?

Without Git:

- Code can be lost.
- No history of changes.
- Difficult team collaboration.
- Difficult to restore previous versions.

Git solves these problems by maintaining complete version history.

---

# Key Features

- Distributed Version Control
- Fast Performance
- Lightweight
- Branching Support
- Merge Support
- Collaboration
- Open Source
- Secure
- Version History

---

# What is Version Control?

Version Control is the process of managing changes made to source code over time.

It records:

- Who made the change
- What changed
- When it changed
- Why it changed

---

# Types of Version Control

## Local Version Control

```

Developer

↓

Local Folder

```

No collaboration.

---

## Centralized Version Control

```

Developer

↓

Central Server

```

Example

SVN

Problem

Server failure affects everyone.

---

## Distributed Version Control

```

Developer

↓

Local Repository

↓

Remote Repository

```

Example

Git

Every developer has a complete copy of the repository.

---

# Git Architecture

```

Working Directory

↓

Staging Area

↓

Local Repository

↓

Remote Repository

```

---

## Working Directory

Contains the current project files.

Example

```

index.html

App.js

README.md

```

---

## Staging Area

Temporary area where changes are prepared before committing.

Command

```bash
git add .
```

---

## Local Repository

Stores commits on the local machine.

Command

```bash
git commit -m "Initial Commit"
```

---

## Remote Repository

Stores the project on GitHub, GitLab, or Bitbucket.

Command

```bash
git push
```

---

# Basic Git Workflow

```

Create File

↓

git add

↓

git commit

↓

git push

```

---

# Important Git Commands

Initialize Repository

```bash
git init
```

Clone Repository

```bash
git clone <repository-url>
```

Check Status

```bash
git status
```

Stage Files

```bash
git add .
```

Commit

```bash
git commit -m "Commit Message"
```

Push

```bash
git push
```

Pull

```bash
git pull
```

View History

```bash
git log
```

---

# Real-Time Example

Suppose you are working on an Employee Management System.

Day 1

```
Create Login Page
```

Commit

```
git commit -m "Add login page"
```

Day 2

```
Fix Login Validation
```

Commit

```
git commit -m "Fix login validation"
```

If the latest changes introduce a bug, Git allows you to return to the previous working version.

---

# Interview Questions

## What is Git?

Git is a distributed version control system used to track changes in source code and enable team collaboration.

---

## Why Git?

Git helps manage code versions, maintain history, support collaboration, and recover previous versions when needed.

---

## Difference between Git and GitHub?

Git is a version control system.

GitHub is a cloud platform that hosts Git repositories.

---

## What is a Repository?

A repository is a storage location that contains project files and their complete version history.

---

## What is Commit?

A commit is a snapshot of project changes stored in Git history.

---

## What is the Staging Area?

The staging area is an intermediate area where selected changes are prepared before committing.

---

## Difference between Git and SVN?

| Git | SVN |
|------|-----|
| Distributed | Centralized |
| Offline support | Requires server |
| Faster | Slower |
| Branching is lightweight | Branching is expensive |

---

# Common Mistakes

- Committing without checking `git status`
- Using unclear commit messages like "update"
- Forgetting to push commits
- Working directly on `main` for every change

---

# Quick Revision

- Git = Version Control System
- GitHub = Repository Hosting Platform
- Repository = Project storage
- Commit = Snapshot
- Push = Upload changes
- Pull = Download changes
- Clone = Copy repository
- Branch = Parallel line of development

---

# Difficulty

⭐☆☆☆☆
