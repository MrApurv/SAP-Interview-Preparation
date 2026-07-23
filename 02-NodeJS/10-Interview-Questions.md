# Node.js Interview Questions

---

# Beginner

## What is Node.js?

Node.js is an open-source JavaScript runtime built on Google's V8 engine that allows JavaScript to run outside the browser.

---

## Is Node.js a programming language?

No.

JavaScript is the language.

Node.js is the runtime.

---

## Is Node.js single-threaded?

JavaScript execution is single-threaded, but Node.js uses asynchronous APIs and the Event Loop to handle many operations concurrently.

---

## What is npm?

Node Package Manager.

---

## What is package.json?

Stores project metadata, dependencies, scripts, and configuration.

---

## What is package-lock.json?

Stores the exact installed dependency versions.

---

## What is node_modules?

Directory containing installed project dependencies.

---

## Difference between dependency and devDependency?

dependency

Production package

devDependency

Development package

---

# Intermediate

## Explain Event Loop.

The Event Loop checks the Call Stack and Callback Queue to execute asynchronous callbacks without blocking the main thread.

---

## Why is Node.js fast?

Because it uses:

- V8 Engine
- Non-blocking I/O
- Event Loop
- Event-driven architecture

---

## Difference between require and import?

require → CommonJS

import → ES Modules

---

## Why don't we upload node_modules to GitHub?

Because it is very large and can be regenerated using:

```
npm install
```

---

## Why commit package-lock.json?

To ensure every developer installs the exact same dependency versions.

---

# Advanced

## Explain package.json in detail.

Mention:

- name
- version
- scripts
- dependencies
- devDependencies
- main
- author
- license

---

## Explain Node.js architecture.

JavaScript

↓

V8 Engine

↓

Event Loop

↓

System APIs

↓

Execution

---

## What happens when npm install runs?

1. Reads package.json.
2. Downloads dependencies.
3. Creates node_modules.
4. Updates package-lock.json if required.

---

## Real-Time Scenario

Q. You cloned a Node.js project, but the application fails because `node_modules` is missing. What should you do?

Answer:

Run:

```bash
npm install
```

This command reads `package.json` and `package-lock.json`, downloads the required dependencies, and recreates the `node_modules` directory.

---

# Quick Revision

Node.js → Runtime

V8 → JavaScript Engine

npm → Package Manager

package.json → Metadata

package-lock.json → Exact Versions

node_modules → Installed Packages

Event Loop → Async Processing

CommonJS → require()

ES Modules → import