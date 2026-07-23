# NPM (Node Package Manager)

---

# What is NPM?

NPM stands for Node Package Manager.

It is the default package manager for Node.js.

It helps developers install, update, remove, and manage project dependencies.

---

# Why NPM?

Without NPM:

- Manual library downloads
- Version conflicts
- Difficult dependency management

NPM automates these tasks.

---

# Types of Dependencies

### Production Dependency

Required to run the application.

Example:

```
express
axios
```

Install:

```bash
npm install express
```

---

### Development Dependency

Required only during development.

Example:

```
nodemon
eslint
prettier
```

Install:

```bash
npm install --save-dev nodemon
```

---

# Useful Commands

Initialize Project

```bash
npm init
```

Quick Initialization

```bash
npm init -y
```

Install Package

```bash
npm install express
```

Install All Dependencies

```bash
npm install
```

Remove Package

```bash
npm uninstall express
```

Update Packages

```bash
npm update
```

---

# Real-Time Example

WorkSphere Backend

```
npm init -y

↓

package.json

↓

npm install express

↓

npm install mongoose

↓

npm install dotenv
```

---

# Interview Questions

## What is NPM?

NPM is the default package manager for Node.js.

---

## Difference between dependency and devDependency?

dependency → Required in production.

devDependency → Required only during development.

---

## What command initializes a Node project?

```
npm init
```

---

# Quick Revision

npm = Package Manager

npm init

npm install

npm uninstall

npm update