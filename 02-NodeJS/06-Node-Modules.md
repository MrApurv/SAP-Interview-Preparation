# node_modules

---

# What is node_modules?

node_modules is the directory where npm installs all project dependencies.

It contains every package required by the application.

---

# How is it Created?

When

```bash
npm install
```

is executed,

npm downloads all required packages into the node_modules folder.

---

# Why is node_modules Important?

Without node_modules,

the application cannot use installed libraries.

Example

```
express

axios

mongoose

dotenv
```

---

# Structure

```
Project

│

├── package.json

├── package-lock.json

├── node_modules

│

└── app.js
```

---

# Why is node_modules So Large?

Each package may depend on many other packages.

Example

```
Express

↓

Body Parser

↓

Debug

↓

Mime

↓

...

```

Thousands of files can be installed.

---

# Should We Push node_modules to GitHub?

NO.

Never commit node_modules.

Reason

- Very large
- Can be regenerated
- Makes repository huge

Instead,

commit

```
package.json

package-lock.json
```

---

# How to Recreate node_modules?

Delete

```
node_modules
```

Run

```bash
npm install
```

npm will recreate it automatically.

---

# Why is node_modules in .gitignore?

Because it can always be regenerated from package.json and package-lock.json.

---

# Real-Time Example

You cloned WorkSphere.

Initially

```
No node_modules
```

Run

```bash
npm install
```

↓

npm reads package.json

↓

Downloads packages

↓

Creates node_modules

↓

Project works

---

# Interview Questions

## What is node_modules?

It stores all installed project dependencies.

---

## Why don't we commit node_modules?

Because it is large and can be regenerated.

---

## Which files recreate node_modules?

package.json

package-lock.json

---

## What command recreates node_modules?

```bash
npm install
```

---

# Best Practices

✔ Ignore node_modules in Git

✔ Use npm install after cloning

✔ Commit package.json

✔ Commit package-lock.json

---

# Quick Revision

node_modules

↓

Installed Packages

↓

Generated Automatically

↓

Never Push to Git