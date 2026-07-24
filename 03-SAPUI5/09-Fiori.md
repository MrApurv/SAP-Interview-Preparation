# SAP Fiori

---

# What is SAP Fiori?

SAP Fiori is SAP's modern User Experience (UX) design system used to build simple, responsive, and role-based business applications.

It provides a consistent look and feel across desktop, tablet, and mobile devices.

SAPUI5 is the primary technology used to develop SAP Fiori applications.

---

# Why was SAP Fiori Introduced?

Before SAP Fiori,

SAP applications mainly used SAP GUI, which had a traditional interface and was difficult for end users.

SAP Fiori was introduced to provide:

- Modern User Interface
- Better User Experience
- Responsive Applications
- Role-Based Screens
- Simplified Business Processes
- Consistent Design

---

# SAP Fiori Design Principles

SAP Fiori is based on five key design principles.

## Role-Based

Applications display only the information required for a user's role.

Example:

- HR Employee
- Sales Manager
- Purchase Manager

Each user sees different applications.

---

## Responsive

Applications automatically adapt to:

- Desktop
- Tablet
- Mobile

without changing the code.

---

## Simple

Business processes are simplified.

Users can complete tasks with fewer clicks.

---

## Coherent

All Fiori applications have a consistent layout and behavior.

Users don't need to relearn different interfaces.

---

## Delightful

Fiori focuses on a modern and intuitive user experience.

---

# SAP Fiori Architecture

```
User

↓

SAP Fiori Launchpad

↓

SAPUI5 Application

↓

OData Service

↓

SAP Gateway

↓

SAP Backend
```

---

# SAP Fiori Launchpad (FLP)

The Fiori Launchpad is the central entry point for SAP Fiori applications.

It provides:

- Home Page
- Tiles
- Search
- Navigation
- User Personalization

---

# Tiles

Tiles represent applications on the Launchpad.

Example

```
Employee Management

Project Dashboard

Asset Tracking

Leave Requests
```

Clicking a tile opens the application.

---

# Catalog

A Catalog contains all applications assigned to a particular business role.

Example

HR Catalog

```
Employee Details

Leave Approval

Payroll
```

---

# Group

A Group organizes frequently used applications on the Launchpad home page.

Example

Favorites

```
Employee App

Dashboard

Reports
```

---

# Spaces and Pages

Modern SAP Fiori Launchpad uses Spaces and Pages.

## Space

Represents a business area.

Example

```
Human Resources
```

---

## Page

Contains applications related to that business area.

Example

```
Employees

Payroll

Attendance
```

Spaces and Pages replace the older Group concept in newer SAP systems.

---

# Fiori Elements

Fiori Elements is a framework that generates SAP Fiori applications automatically using metadata and annotations.

Developers write very little frontend code.

Best suited for:

- CRUD Applications
- Standard Business Apps

---

# Freestyle SAPUI5

Freestyle SAPUI5 gives developers complete control over the application's UI and logic.

Used when:

- Custom Layouts
- Complex Business Logic
- Custom User Experience

are required.

---

# Fiori Elements vs Freestyle

| Fiori Elements | Freestyle SAPUI5 |
|----------------|------------------|
| Metadata Driven | Code Driven |
| Faster Development | More Flexible |
| Less Coding | Full Customization |
| Standard UI | Custom UI |
| Annotation Based | Manual Development |

---

# SAPUI5 vs SAP Fiori

| SAPUI5 | SAP Fiori |
|----------|-----------|
| JavaScript UI Framework | SAP Design System |
| Used for Development | Used for User Experience |
| Contains UI Controls | Defines Design Guidelines |
| Builds Applications | Standardizes Applications |

SAPUI5 is the technology.

SAP Fiori is the design language.

---

# Real-Time Example

WorkSphere

```
SAP Fiori Launchpad

↓

WorkSphere Tile

↓

SAPUI5 Application

↓

OData Service

↓

CAP Backend

↓

Database
```

---

# Advantages

✔ Modern User Experience

✔ Responsive Design

✔ Role-Based Access

✔ Enterprise Ready

✔ Consistent Design

✔ Easy Navigation

✔ Mobile Friendly

---

# Common Mistakes

❌ Thinking SAPUI5 and SAP Fiori are the same.

SAPUI5 is a framework.

SAP Fiori is a design system.

---

❌ Assuming every SAPUI5 application is a Fiori application.

Only SAPUI5 applications that follow Fiori design principles are considered SAP Fiori apps.

---

❌ Confusing Launchpad with SAPUI5.

Launchpad is a portal.

SAPUI5 is the frontend framework.

---

# Best Practices

- Follow SAP Fiori Design Guidelines.
- Build responsive applications.
- Use role-based navigation.
- Keep user interactions simple.
- Prefer Fiori Elements for standard CRUD applications.
- Use Freestyle SAPUI5 for highly customized applications.

---

# Interview Questions

## What is SAP Fiori?

SAP Fiori is SAP's design system that provides a modern, responsive, and role-based user experience for business applications.

---

## What is SAPUI5?

SAPUI5 is a JavaScript framework used to develop SAP Fiori applications.

---

## Is SAP Fiori a programming language?

No.

It is a design system and user experience concept.

---

## What is the SAP Fiori Launchpad?

It is the central entry point where users access SAP Fiori applications.

---

## What are Tiles?

Tiles are clickable icons on the Launchpad that open applications.

---

## What is a Catalog?

A Catalog is a collection of applications assigned to a business role.

---

## What is a Group?

A Group organizes frequently used applications on the Launchpad.

---

## What are Spaces and Pages?

Spaces organize applications by business area, while Pages contain related applications within that area.

---

## What is Fiori Elements?

A framework that generates SAP Fiori applications using metadata and annotations with minimal coding.

---

## What is Freestyle SAPUI5?

A development approach where developers manually build the UI and business logic for full customization.

---

## Difference between Fiori Elements and Freestyle SAPUI5?

Fiori Elements is metadata-driven with less coding.

Freestyle SAPUI5 is code-driven and offers complete flexibility.

---

## Difference between SAPUI5 and SAP Fiori?

SAPUI5 is the JavaScript framework used to build applications.

SAP Fiori is the design language and user experience standard followed by those applications.

---

## Can SAPUI5 applications run without Fiori?

Yes.

SAPUI5 applications can run independently without the Fiori Launchpad.

---

## Which approach is faster for developing standard business applications?

Fiori Elements.

---

## Which approach is preferred for highly customized applications?

Freestyle SAPUI5.

---

# Quick Revision

SAP Fiori

↓

SAP UX Design System

↓

Role-Based

↓

Responsive

↓

Simple

↓

Fiori Launchpad

↓

Tiles

↓

Catalog

↓

Spaces & Pages

↓

Fiori Elements

↓

Freestyle SAPUI5

↓

Built Using SAPUI5