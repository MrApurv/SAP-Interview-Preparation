# GitHub

---

# What is GitHub?

GitHub is a cloud-based platform that hosts Git repositories and enables developers to collaborate on software projects.

It provides features like version control, pull requests, code reviews, issue tracking, and CI/CD integration.

---

# Why GitHub?

Git alone manages version control locally.

GitHub adds:

- Remote repository hosting
- Team collaboration
- Pull Requests
- Code Reviews
- Issue Tracking
- Project Management
- GitHub Actions (CI/CD)

---

# Git vs GitHub

| Git | GitHub |
|------|---------|
| Version Control System | Cloud Hosting Platform |
| Works locally | Works online |
| Tracks code history | Stores Git repositories |
| Command-line tool | Web platform |

---

# Repository

A repository contains:

- Source Code
- Commit History
- Branches
- Pull Requests
- Documentation
- Releases

---

# Public Repository

Visible to everyone.

Used for:

- Open Source
- Portfolio Projects
- Learning

---

# Private Repository

Accessible only to authorized collaborators.

Used for:

- Company projects
- Confidential code
- Personal work

---

# Branches

Branches allow developers to work independently without affecting the main codebase.

Example

```
main

↓

feature/login

↓

feature/dashboard
```

---

# Pull Request

A Pull Request is a request to merge changes from one branch into another.

It allows team members to:

- Review code
- Suggest improvements
- Discuss changes
- Approve before merging

---

# Fork

A fork creates your own copy of someone else's repository under your GitHub account.

Useful for contributing to open-source projects.

---

# Clone

Copies a remote repository to your local machine.

Command

```bash
git clone <repository-url>
```

---

# SSH Authentication

SSH provides secure communication between your local machine and GitHub without entering your password every time.

Common steps:

1. Generate SSH key.
2. Add the public key to GitHub.
3. Test the connection using:

```bash
ssh -T git@github.com
```

---

# Real-Time Example

WorkSphere Repository

```
main

↓

feature/initial-ui5-setup

↓

Pull Request

↓

Code Review

↓

Merge

↓

main
```

This is the same workflow used in professional software teams.

---

# Interview Questions

## What is GitHub?

GitHub is a cloud-based platform used to host Git repositories and enable collaboration among developers.

---

## Difference between Git and GitHub?

Git is a version control system.

GitHub is a hosting platform built around Git.

---

## What is a Pull Request?

A Pull Request is a request to merge code from one branch into another after review.

---

## What is Fork?

A fork creates a personal copy of another user's repository.

---

## What is Clone?

Clone downloads a copy of a remote repository to the local machine.

---

## Why use SSH instead of HTTPS?

SSH provides secure authentication without requiring credentials for every push or pull operation.

---

# Quick Revision

- GitHub = Cloud platform
- Repository = Project storage
- Branch = Independent development
- Pull Request = Merge request
- Fork = Copy repository
- Clone = Download repository
- SSH = Secure authentication

---

# Difficulty

⭐☆☆☆☆
