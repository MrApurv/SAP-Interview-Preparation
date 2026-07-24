# Routing in SAPUI5

---

# What is Routing?

Routing is the mechanism used to navigate between different Views in a SAPUI5 application without reloading the entire application.

It enables Single Page Application (SPA) behavior where only the content changes while the application remains loaded.

---

# Why is Routing Needed?

Without Routing,

developers would have to manually destroy and recreate Views every time a user navigates.

Routing automates navigation and manages browser URLs efficiently.

---

# How Routing Works

```
User Clicks Button

↓

Controller

↓

Router

↓

Route

↓

Target

↓

View

↓

Screen Displayed
```

---

# Routing Components

SAPUI5 Routing mainly consists of:

- Router
- Route
- Target
- Pattern
- Navigation

---

# Router

The Router is responsible for handling navigation between Views.

It reads the URL and determines which View should be displayed.

---

# Route

A Route defines the URL pattern.

Example:

```json
{
    "name": "employee",
    "pattern": "employee",
    "target": "employee"
}
```

---

# Target

A Target specifies which View should be loaded.

Example:

```json
{
    "employee": {
        "viewName": "Employee"
    }
}
```

---

# Pattern

A Pattern represents the URL.

Examples:

```
dashboard

employee

employee/1001

settings
```

The Router compares the browser URL with the configured pattern.

---

# Navigation Flow

```
Controller

↓

navTo()

↓

Router

↓

Route

↓

Target

↓

View Loaded
```

---

# navTo()

The navTo() method is used to navigate to another Route.

Example:

```javascript
this.getRouter().navTo("employee");
```

---

# getRouter()

Returns the Router instance.

Example:

```javascript
this.getOwnerComponent().getRouter();
```

or

```javascript
this.getRouter();
```

(when using BaseController)

---

# Browser URL Example

```
https://worksphere.com/#/dashboard

↓

Dashboard View
```

```
https://worksphere.com/#/employee

↓

Employee View
```

The URL changes, but the application is not reloaded.

---

# Routing Configuration

Routing is configured inside:

```
manifest.json

↓

sap.ui5

↓

routing
```

---

# Real-Time Example

WorkSphere

```
Login

↓

Dashboard

↓

Employees

↓

Projects

↓

Assets

↓

Settings
```

Each page represents a Route.

---

# Advantages

✔ Single Page Application

✔ Faster Navigation

✔ Bookmark Support

✔ Browser History Support

✔ Clean URL Structure

✔ Better User Experience

---

# Common Mistakes

❌ Forgetting to initialize the Router.

```javascript
this.getRouter().initialize();
```

---

❌ Incorrect Route Name.

```javascript
this.getRouter().navTo("Employee");
```

Route names are case-sensitive.

---

❌ Pattern mismatch.

The URL must match the configured Route pattern.

---

❌ Missing Target.

Every Route should point to a valid Target.

---

# Best Practices

- Define all Routes inside manifest.json.
- Use meaningful Route names.
- Keep Route names lowercase.
- Avoid duplicate Route patterns.
- Initialize Routing inside Component.js.
- Use navTo() instead of manually creating Views.

---

# Interview Questions

## What is Routing?

Routing is the mechanism used to navigate between different Views in a SAPUI5 application without reloading the application.

---

## Why is Routing required?

Routing enables navigation, browser history support, bookmarkable URLs, and Single Page Application behavior.

---

## Where is Routing configured?

Inside:

```
manifest.json

↓

sap.ui5

↓

routing
```

---

## What is a Router?

The Router manages navigation based on URL patterns.

---

## What is a Route?

A Route maps a URL pattern to a Target.

---

## What is a Target?

A Target defines which View should be displayed.

---

## What is navTo()?

navTo() is used to navigate from one Route to another.

Example:

```javascript
this.getRouter().navTo("dashboard");
```

---

## What is getRouter()?

getRouter() returns the Router instance used for navigation.

---

## Can Routing work without manifest.json?

No.

In modern SAPUI5 applications, Routing is configured in manifest.json.

---

## Does Routing reload the application?

No.

Only the required View is loaded.

---

## What is SPA?

SPA (Single Page Application) loads the application only once. Subsequent navigation updates only the displayed View without refreshing the browser.

---

## Which file initializes Routing?

Component.js

```javascript
this.getRouter().initialize();
```

---

## Can users use the browser Back button?

Yes.

SAPUI5 Routing integrates with browser history.

---

# Quick Revision

Routing

↓

SPA Navigation

↓

Router

↓

Route

↓

Target

↓

Pattern

↓

navTo()

↓

Browser History

↓

No Page Reload