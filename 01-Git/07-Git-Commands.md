# Git Commands

---

# Repository Commands

Initialize Repository

```bash
git init
```

Clone Repository

```bash
git clone <url>
```

---

# Status Commands

```bash
git status
```

```bash
git log
```

```bash
git log --oneline
```

```bash
git diff
```

---

# Staging Commands

Stage All

```bash
git add .
```

Stage Specific File

```bash
git add filename
```

Unstage

```bash
git restore --staged filename
```

---

# Commit Commands

```bash
git commit -m "message"
```

Amend Last Commit

```bash
git commit --amend
```

---

# Branch Commands

List Branches

```bash
git branch
```

Create Branch

```bash
git branch feature/login
```

Switch Branch

```bash
git checkout feature/login
```

Create & Switch

```bash
git checkout -b feature/login
```

Delete Branch

```bash
git branch -d feature/login
```

---

# Remote Commands

View Remote

```bash
git remote -v
```

Add Remote

```bash
git remote add origin URL
```

---

# Push Commands

```bash
git push
```

```bash
git push origin main
```

Delete Remote Branch

```bash
git push origin --delete feature/login
```

---

# Pull Commands

```bash
git pull
```

```bash
git fetch
```

Difference

git fetch → Downloads only

git pull → Downloads + Merges

---

# Merge Commands

```bash
git merge feature/login
```

Abort Merge

```bash
git merge --abort
```

---

# Restore Commands

Restore File

```bash
git restore filename
```

Restore All

```bash
git restore .
```

---

# Reset Commands

Soft Reset

```bash
git reset --soft HEAD~1
```

Mixed Reset

```bash
git reset HEAD~1
```

Hard Reset

```bash
git reset --hard HEAD~1
```

---

# Stash Commands

```bash
git stash
```

```bash
git stash list
```

```bash
git stash apply
```

---

# Helpful Commands

```bash
git config --global user.name
```

```bash
git config --global user.email
```

```bash
git config --list
```

---

# Interview Tip

Know the difference between:

- fetch vs pull
- restore vs reset
- merge vs rebase
- clone vs fork
- add vs commit