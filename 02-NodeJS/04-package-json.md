# package.json

---

# What is package.json?

package.json is the heart of every Node.js project.

It stores metadata about the project, project information, dependencies, scripts, and configuration.

Every Node.js project should contain a package.json file.

---

# Why is package.json Needed?

Without package.json:

- No project information
- No dependency management
- No npm scripts
- Difficult collaboration

package.json solves all these problems.

---

# How to Create?

Interactive

```bash
npm init
```

Quick

```bash
npm init -y
```

---

# Example

```json
{
  "name": "worksphere",
  "version": "1.0.0",
  "description": "Enterprise Asset Management Platform",
  "main": "index.js",
  "scripts": {
    "start": "node app.js",
    "dev": "nodemon app.js"
  },
  "author": "Apurv Nipane",
  "license": "MIT",
  "dependencies": {
    "express": "^5.1.0"
  },
  "devDependencies": {
    "nodemon": "^3.1.0"
  }
}
```

---

# Important Fields

## name

Project name.

```
"worksphere"
```

---

## version

Current application version.

Example

```
1.0.0
```

Semantic Versioning

```
Major.Minor.Patch

1.0.0
```

Major

Breaking Changes

Minor

New Features

Patch

Bug Fixes

---

## description

Short description of the project.

---

## main

Entry point of application.

Example

```
index.js
```

---

## scripts

Defines commands that can be executed using npm.

Example

```json
"scripts": {
  "start": "node app.js",
  "dev": "nodemon app.js"
}
```

Run

```bash
npm start

npm run dev
```

---

## dependencies

Packages required in production.

Example

```json
"dependencies": {
  "express": "^5.1.0"
}
```

---

## devDependencies

Packages required only during development.

Example

```json
"devDependencies": {
  "nodemon": "^3.1.0"
}
```

---

## author

Developer information.

---

## license

Project license.

---

# Real-Time Example

WorkSphere

```
package.json

↓

Stores

Project Name

↓

Scripts

↓

Dependencies

↓

Version

↓

Author
```

---

# Interview Questions

## What is package.json?

package.json stores project metadata, dependencies, scripts, and configuration.

---

## Why is package.json important?

It helps manage the project and its dependencies.

---

## Difference between dependencies and devDependencies?

dependencies

Required in production.

devDependencies

Required only during development.

---

## What are npm scripts?

Commands defined inside package.json that simplify common development tasks.

---

# Best Practices

✔ Keep scripts organized

✔ Remove unused dependencies

✔ Use meaningful version numbers

✔ Commit package.json to Git

---

# Quick Revision

package.json

↓

Project Information

↓

Dependencies

↓

Scripts

↓

Metadata