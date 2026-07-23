# Pull Request (PR)

---

# What is a Pull Request?

A Pull Request (PR) is a request to merge changes from one branch into another.

It allows team members to review, discuss, test, and approve code before it becomes part of the main codebase.

---

# Why Use Pull Requests?

- Code Review
- Maintain Code Quality
- Team Collaboration
- Early Bug Detection
- Knowledge Sharing

---

# Pull Request Workflow

```
Feature Branch
      │
      ▼
Commit Changes
      │
      ▼
Push to GitHub
      │
      ▼
Create Pull Request
      │
      ▼
Code Review
      │
      ▼
Approve
      │
      ▼
Merge into Main
      │
      ▼
Delete Feature Branch
```

---

# Creating a Pull Request

1. Push your feature branch.

```bash
git push origin feature/login
```

2. Open GitHub.

3. Click **Compare & Pull Request**.

4. Add:

- Title
- Description
- Reviewer

5. Submit PR.

---

# PR Title Example

```
feat(login): add login page
```

---

# PR Description Example

## Changes

- Created Login View
- Added Controller
- Connected Routing

## Testing

- Tested on Chrome
- Tested Login Validation

---

# Code Review

Reviewer checks:

- Code Quality
- Naming Convention
- Performance
- Security
- Best Practices

---

# Merge Options

### Create Merge Commit

Keeps complete history.

### Squash Merge

Combines all commits into one.

Useful when many small commits exist.

### Rebase Merge

Maintains linear history.

---

# Best Practices

✔ Small PRs

✔ Clear Description

✔ Meaningful Title

✔ Self Review

✔ Resolve Conflicts

✔ Delete Branch After Merge

---

# Interview Questions

## What is a Pull Request?

A Pull Request is a request to merge one branch into another after code review.

---

## Why use Pull Requests?

To review code before merging.

---

## What should a PR contain?

- Clear title
- Description
- Screenshots (if UI)
- Testing Details

---

## Why shouldn't developers merge directly into main?

Direct merges bypass code review and increase the risk of introducing bugs.

---

# Quick Revision

PR = Code Review

Reviewer = Checks Quality

Merge = Approved Code

Delete Branch = Cleanup