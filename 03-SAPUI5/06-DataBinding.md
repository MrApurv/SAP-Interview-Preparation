# Data Binding in SAPUI5

---

# What is Data Binding?

Data Binding is the process of connecting the UI (View) with the application's data (Model).

It automatically synchronizes data between the Model and the View without writing manual JavaScript code.

---

# Why is Data Binding Needed?

Without Data Binding,

developers would have to manually update every UI control whenever data changes.

Data Binding automatically keeps the UI and Model synchronized.

---

# How Data Binding Works?

```
Backend / Data

↓

Model

↓

Data Binding

↓

View

↓

User Interface
```

Whenever the Model changes, the View updates automatically based on the binding mode.

---

# Types of Data Binding

SAPUI5 provides three main types of Data Binding.

- Property Binding
- Aggregation Binding
- Element Binding

---

# Property Binding

Property Binding binds a single property of a control to a Model value.

Example:

```xml
<Text text="{/name}" />

<Input value="{/email}" />

<ObjectNumber number="{/salary}" />
```

Used for displaying a single value.

---

# Aggregation Binding

Aggregation Binding binds a collection of data to controls such as List, Table, ComboBox, or Select.

Example:

```xml
<List items="{/employees}">
    <StandardListItem title="{name}" />
</List>
```

Each item in the collection creates a new control automatically.

---

# Element Binding

Element Binding binds an entire object to a View or Container.

Example:

```xml
<Panel binding="{/employee}">
    <Text text="{name}" />
    <Text text="{department}" />
</Panel>
```

All child controls use the bound object.

---

# Binding Modes

SAPUI5 supports three Binding Modes.

- One-Way Binding
- Two-Way Binding
- One-Time Binding

---

# One-Way Binding

```
Model

↓

View
```

When the Model changes, the View updates.

Changes in the View do not update the Model.

Example:

```xml
<Text text="{/employeeName}" />
```

Used for:

- Labels
- KPIs
- Reports
- Dashboard Cards

---

# Two-Way Binding

```
Model

▲ ▼

View
```

Changes in either the Model or the View are synchronized automatically.

Example:

```xml
<Input value="{/employeeName}" />
```

Used for:

- Forms
- User Input
- Edit Screens

---

# One-Time Binding

```
Model

↓

View

(No Further Updates)
```

The value is read only once during initialization.

Example:

```xml
<Text text="{:= ${/appVersion}}" />
```

Used for:

- Version Number
- Company Name
- Static Information

---

# Absolute Binding

Starts with "/"

Example:

```xml
<Text text="{/employee/name}" />
```

The path starts from the root of the Model.

---

# Relative Binding

Does not start with "/"

Example:

```xml
<Text text="{name}" />
```

Used inside Element Binding or Aggregation Binding.

---

# Expression Binding

Expression Binding performs simple calculations directly in XML.

Example:

```xml
<Text text="{= ${/salary} > 50000 ? 'High' : 'Low'}" />
```

No formatter function is required.

---

# Formatter

A Formatter is a JavaScript function used to format data before displaying it.

Example:

Controller

```javascript
formatStatus(status) {
    return status ? "Active" : "Inactive";
}
```

View

```xml
<ObjectStatus text="{
    path: '/status',
    formatter: '.formatStatus'
}" />
```

---

# Composite Binding

Combines multiple properties into one control.

Example:

```xml
<Text text="{
    parts: [
        {path:'firstName'},
        {path:'lastName'}
    ],
    formatter: '.formatFullName'
}" />
```

---

# Real-Time Example

WorkSphere Dashboard

```
Employee Data

↓

JSONModel

↓

Data Binding

↓

Dashboard Cards

↓

Automatic UI Update
```

---

# Advantages

✔ Less JavaScript Code

✔ Automatic UI Updates

✔ Cleaner Architecture

✔ Better Performance

✔ Easy Maintenance

✔ Improved Readability

---

# Common Mistakes

❌ Updating UI controls directly.

Incorrect:

```javascript
this.byId("txtName").setText("Rahul");
```

Correct:

```javascript
oModel.setProperty("/name", "Rahul");
```

---

❌ Using One-Time Binding for dynamic data.

---

❌ Using Two-Way Binding for read-only controls.

---

❌ Incorrect binding path.

Example:

```xml
{/employeeName}
```

Model should contain the same property.

---

# Best Practices

- Use One-Way Binding for display-only data.
- Use Two-Way Binding for editable forms.
- Use One-Time Binding for static values.
- Use Expression Binding for simple conditions.
- Use Formatter for complex formatting.
- Prefer updating the Model instead of UI controls.

---

# Interview Questions

## What is Data Binding?

Data Binding is the process of connecting the View with the Model so that data is synchronized automatically.

---

## Why is Data Binding used?

It reduces manual UI updates and keeps the View synchronized with the Model.

---

## What are the types of Data Binding?

- Property Binding
- Aggregation Binding
- Element Binding

---

## What are the Binding Modes?

- One-Way
- Two-Way
- One-Time

---

## What is Property Binding?

It binds a single control property to a Model value.

---

## What is Aggregation Binding?

It binds a collection of data to controls like List or Table.

---

## What is Element Binding?

It binds an entire object to a container or View.

---

## What is the default Binding Mode for JSONModel?

Two-Way Binding.

---

## What is Expression Binding?

It allows simple calculations or conditions directly in XML.

---

## What is a Formatter?

A JavaScript function used to format Model data before displaying it.

---

## Difference between Absolute and Relative Binding?

Absolute Binding starts from the root using "/".

Relative Binding depends on the current binding context.

---

## Which Binding Mode is best for Input controls?

Two-Way Binding.

---

## Which Binding Mode is best for dashboard KPIs?

One-Way Binding.

---

## Can multiple controls bind to the same Model property?

Yes.

All bound controls update automatically when the Model changes.

---

# Quick Revision

Data Binding

↓

Model ↔ View

↓

Property Binding

↓

Aggregation Binding

↓

Element Binding

↓

One-Way

↓

Two-Way

↓

One-Time

↓

Expression Binding

↓

Formatter

↓

Automatic UI Synchronization