# Advanced SAPUI5

---

# What is Advanced SAPUI5?

Advanced SAPUI5 refers to concepts beyond the basics that help developers build enterprise-grade, scalable, reusable, and high-performance applications.

These concepts are commonly used in real-world SAP Fiori projects.

---

# Advanced Topics in SAPUI5

- Fragments
- Dialogs
- Formatter
- Expression Binding
- Custom Controls
- Custom Libraries
- MessageManager
- Reuse Components
- Lazy Loading
- Performance Optimization
- Error Handling
- Debugging
- Testing (QUnit & OPA5)

---

# Fragments

A Fragment is a reusable UI component that does not have its own Controller.

It is used to avoid duplicating UI code.

Common examples:

- Dialog
- Popover
- Value Help
- Filter Dialog

Example

```javascript
Fragment.load({
    name: "com.apurv.worksphere.view.fragments.EmployeeDialog",
    controller: this
});
```

---

# Dialog

A Dialog is a popup window used for user interaction.

Common uses:

- Confirmation
- Login
- Delete Confirmation
- Edit Form

---

# Formatter

A Formatter is a JavaScript function used to format data before displaying it.

Example

```javascript
formatStatus(status){
    return status ? "Active" : "Inactive";
}
```

---

# Expression Binding

Expression Binding allows simple logic directly in XML.

Example

```xml
<Text text="{= ${/salary} > 50000 ? 'High' : 'Low'}"/>
```

No formatter is required.

---

# MessageManager

MessageManager manages validation and application messages.

Examples

- Success
- Error
- Warning
- Information

Used extensively in enterprise SAP applications.

---

# Custom Controls

Custom Controls extend existing SAPUI5 controls to add new functionality.

Example

```javascript
sap.m.Button.extend(...)
```

Use when standard controls do not meet business requirements.

---

# Custom Libraries

A Custom Library is a collection of reusable controls, utilities, and components shared across multiple applications.

Benefits

- Reusability
- Consistency
- Easier Maintenance

---

# Reuse Components

Reuse Components allow developers to embed one SAPUI5 application inside another.

Used for:

- Shared Dashboards
- Common Modules
- Reusable Business Components

---

# Lazy Loading

Lazy Loading loads Views or Components only when they are needed.

Benefits

- Faster Startup
- Lower Memory Usage
- Better Performance

---

# Performance Optimization

Best practices:

- Load only required libraries.
- Use Lazy Loading.
- Use Batch Requests.
- Use $select to retrieve required fields.
- Avoid unnecessary Model refreshes.
- Reuse Fragments.
- Destroy unused controls.

---

# Error Handling

Handle backend and frontend errors gracefully.

Example

```javascript
MessageBox.error("Unable to fetch data.");
```

Never expose technical errors directly to end users.

---

# Debugging

Common debugging tools:

- Chrome Developer Tools
- SAPUI5 Diagnostics
- Network Tab
- Console
- Breakpoints

Useful methods

```javascript
console.log()

debugger;
```

---

# Testing

SAPUI5 supports:

## QUnit

Used for Unit Testing.

Tests individual JavaScript functions.

---

## OPA5

Used for Integration Testing.

Tests complete user workflows.

Example

- Login
- Navigation
- Form Submission

---

# Real-Time Example

WorkSphere

```
Dashboard

↓

Fragment

↓

Employee Dialog

↓

Formatter

↓

OData

↓

MessageManager

↓

Success Message
```

---

# Advantages

✔ Better Code Reusability

✔ Improved Performance

✔ Easier Maintenance

✔ Enterprise Architecture

✔ Better User Experience

---

# Common Mistakes

❌ Duplicating Dialog XML.

Use Fragments.

---

❌ Writing complex XML expressions.

Use Formatter.

---

❌ Loading all Views during startup.

Use Lazy Loading.

---

❌ Ignoring Error Handling.

Always display meaningful messages.

---

# Best Practices

- Create reusable Fragments.
- Use Formatter for complex formatting.
- Optimize OData requests.
- Load Views lazily.
- Use MessageManager for validation.
- Write Unit Tests.
- Keep Controllers lightweight.

---

# Interview Questions

## What is a Fragment?

A Fragment is a reusable UI component without its own Controller.

---

## Why are Fragments used?

To reuse UI elements and reduce duplicate code.

---

## Difference between Fragment and View?

View

- Has its own Controller.
- Represents a complete screen.

Fragment

- No Controller.
- Represents a reusable UI part.

---

## What is a Formatter?

A JavaScript function used to format Model data before displaying it.

---

## What is Expression Binding?

Expression Binding allows simple conditions and calculations directly in XML.

---

## Difference between Formatter and Expression Binding?

Expression Binding

- Simple conditions
- No JavaScript file

Formatter

- Complex formatting
- JavaScript function

---

## What is MessageManager?

A framework used to manage validation, success, warning, and error messages.

---

## What are Custom Controls?

Controls developed by extending existing SAPUI5 controls.

---

## What is a Reuse Component?

A reusable SAPUI5 component that can be embedded in multiple applications.

---

## What is Lazy Loading?

Loading Views or Components only when required.

---

## How can SAPUI5 application performance be improved?

- Lazy Loading
- Batch Requests
- Use $select
- Destroy unused controls
- Load required libraries only

---

## Which testing frameworks are used in SAPUI5?

QUnit and OPA5.

---

## What is QUnit?

A Unit Testing framework for JavaScript functions.

---

## What is OPA5?

An Integration Testing framework for testing complete application flows.

---

## Which tool is used for debugging SAPUI5 applications?

Chrome Developer Tools and SAPUI5 Diagnostics.

---

## What is the purpose of MessageBox?

To display success, error, warning, or confirmation messages to users.

---

# Quick Revision

Advanced SAPUI5

↓

Fragments

↓

Dialogs

↓

Formatter

↓

Expression Binding

↓

MessageManager

↓

Custom Controls

↓

Reuse Components

↓

Lazy Loading

↓

Performance Optimization

↓

Error Handling

↓

Debugging

↓

QUnit

↓

OPA5