# CommonJS vs ES Modules

---

# What are Modules?

Modules allow code to be divided into reusable files.

Instead of writing everything in one file,

we split code into

- Authentication
- Database
- API
- Utilities

---

# CommonJS

Default module system in Node.js.

Export

```javascript
module.exports = add;
```

Import

```javascript
const add = require("./add");
```

---

# ES Modules

Modern JavaScript module system.

Export

```javascript
export default add;
```

Import

```javascript
import add from "./add.js";
```

---

# Comparison

| CommonJS | ES Modules |
|----------|------------|
| require() | import |
| module.exports | export |
| Default in older Node.js | Standard JavaScript |
| Synchronous | Static Imports |

---

# Which One Should We Learn?

Modern projects

↓

ES Modules

Legacy Node.js Projects

↓

CommonJS

---

# Real-Time Example

Project

```
controllers/

services/

routes/

models/

utils/
```

Every folder exports modules.

Main application imports them.

---

# Interview Questions

## What is a Module?

A module is a reusable JavaScript file.

---

## Difference between require and import?

require belongs to CommonJS.

import belongs to ES Modules.

---

## Which module system is newer?

ES Modules.

---

# Quick Revision

CommonJS

↓

require()

↓

module.exports

---

ES Modules

↓

import

↓

export