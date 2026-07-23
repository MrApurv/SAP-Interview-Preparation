# Git Interview Questions

---

# Beginner Level

## What is Git?

Git is a Distributed Version Control System used to track source code changes.

---

## What is GitHub?

GitHub is a cloud platform that hosts Git repositories.

---

## Difference between Git and GitHub?

Git = Version Control System

GitHub = Git Hosting Platform

---

## What is a Repository?

A storage location containing project files and Git history.

---

## What is Commit?

A snapshot of project changes.

---

## What is Branch?

An independent line of development.

---

## What is Merge?

Combining one branch into another.

---

## What is Pull Request?

A request to merge changes after review.

---

## What is Clone?

Creates a local copy of a remote repository.

---

## What is Fork?

Creates your own copy of another repository on GitHub.

---

# Intermediate Level

## Difference between Pull and Fetch?

Fetch downloads changes only.

Pull downloads and merges changes.

---

## Difference between Restore and Reset?

Restore affects working files.

Reset affects Git history.

---

## Difference between Merge and Rebase?

Merge preserves history with a merge commit.

Rebase creates a linear history by replaying commits.

---

## What is Staging Area?

An intermediate area where selected changes are prepared before committing.

---

## What is HEAD?

HEAD points to the current commit that you are working on.

---

## What happens if two developers edit the same file?

Git may produce a merge conflict, which must be resolved manually.

---

# Advanced Level

## Explain Git Workflow in your current project.

Example Answer:

> In our WorkSphere project, we created feature branches for new work, committed changes with meaningful messages, pushed them to GitHub, opened Pull Requests, completed code reviews, merged into the main branch, and deleted the feature branch after successful integration.

---

## Have you resolved merge conflicts?

Example Answer:

> Yes. While merging feature branches, Git reported conflicts. I manually reviewed the conflicting sections, selected the correct changes, staged the resolved files, committed the merge, and pushed the updated branch.

---

## Why shouldn't developers work directly on main?

Working directly on the main branch increases the risk of introducing bugs into the stable codebase. Feature branches allow isolated development and proper code reviews.

---

## Best Practices

✔ Commit frequently

✔ Use meaningful commit messages

✔ Pull before pushing

✔ Create feature branches

✔ Review code before merging

✔ Delete merged branches

---

# Quick Revision

Git → Version Control

GitHub → Hosting Platform

Branch → Independent Development

Commit → Snapshot

Push → Upload Changes

Pull → Download + Merge

Fetch → Download Only

Merge → Combine Branches

Rebase → Linear History

PR → Code Review

Conflict → Manual Resolution