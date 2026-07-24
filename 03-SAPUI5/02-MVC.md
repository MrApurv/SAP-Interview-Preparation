# MVC (Model-View-Controller)

---

# What is MVC?

MVC (Model-View-Controller) is a software architectural pattern used in SAPUI5 to separate an application's data, user interface, and business logic.

It makes applications easier to develop, test, maintain, and scale.

---

# Why is MVC Used?

Without MVC,

all the UI, business logic, and data would be written in a single file.

This makes applications difficult to understand and maintain.

MVC separates responsibilities into different components.

---

# MVC Components

## Model

The Model manages application data.

Responsibilities:

- Store data
- Retrieve data
- Update data
- Connect with backend
- Provide data to the View

---

## View

The View is responsible for the user interface.

Responsibilities:

- Display data
- Show controls
- Accept user input
- Bind data from Models

Views are commonly written in:

- XML
- HTML
- JavaScript
- JSON

Most SAPUI5 applications use XML Views.

---

## Controller

The Controller contains the business logic.

Responsibilities:

- Handle user actions
- Process data
- Update Models
- Navigate between pages
- Call backend services

---

# MVC Architecture

```
User

↓

View

↓

Controller

↓

Model

↓

Backend
```

---

# MVC Flow

```
User Clicks Button

↓

View

↓

Controller

↓

Model

↓

Backend

↓

Model

↓

View

↓

Updated Screen
```

---

# Example

Employee Details Screen

Model

```json
{
    "employeeId": "1001",
    "name": "Rahul Sharma",
    "department": "IT"
}
```

View

```xml
<Text text="{/name}" />

<Text text="{/department}" />
```

Controller

```javascript
onRefresh() {
    this.getView().getModel().refresh();
}
```

---

# Advantages of MVC

✔ Separation of Concerns

✔ Better Code Organization

✔ Easy Maintenance

✔ Reusable Components

✔ Easy Testing

✔ Scalable Architecture

✔ Better Team Collaboration

---

# Limitations

- More files to manage
- Slightly higher learning curve
- Small applications may feel over-structured

---

# Real-Time Example

WorkSphere

```
Employee Dashboard

↓

View

↓

Employee.controller.js

↓

EmployeeModel

↓

CAP / SAP Backend
```

---

# MVC in SAPUI5 Project

```
webapp

│

├── view

├── controller

├── model

├── Component.js

└── manifest.json
```

---

# Responsibilities

| Component | Responsibility |
|-----------|----------------|
| Model | Stores Data |
| View | Displays UI |
| Controller | Handles Logic |

---

# Best Practices

- Keep business logic inside Controllers.
- Store application data inside Models.
- Keep Views free from complex logic.
- Use Data Binding instead of manually updating UI controls.
- Keep Controllers lightweight by updating Models instead of UI elements.

---

# Common Mistakes

❌ Writing business logic inside the View.

❌ Updating UI controls directly instead of updating the Model.

❌ Storing application data inside Controllers.

❌ Mixing backend logic with UI code.

---

# Interview Questions

## What is MVC?

MVC is an architectural pattern that separates an application into Model, View, and Controller, improving maintainability and scalability.

---

## What is the role of the Model?

The Model stores and manages application data.

---

## What is the role of the View?

The View displays the user interface and binds data from the Model.

---

## What is the role of the Controller?

The Controller contains business logic, handles user interactions, updates Models, and manages navigation.

---

## Which View type is most commonly used in SAPUI5?

XML View.

---

## Can one Controller be used for multiple Views?

Generally, each View has its own Controller, but reusable logic can be shared using Base Controllers or utility classes.

---

## Can one Model be used by multiple Views?

Yes.

A single Model can be shared across multiple Views by assigning it at the Component level.

---

## Does the View communicate directly with the Backend?

No.

The View communicates with the Model through Data Binding, while the Controller manages interactions with the backend.

---

## Why is MVC important?

MVC separates responsibilities, making applications easier to maintain, test, and scale.

---

# Quick Revision

MVC

↓

Model → Stores Data

↓

View → Displays UI

↓

Controller → Handles Business Logic

↓

Better Maintainability

↓

Scalable Applications

↓

Core Architecture of SAPUI5