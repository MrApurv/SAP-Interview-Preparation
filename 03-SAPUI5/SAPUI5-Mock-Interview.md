# SAPUI5 Mock Interview

---

# SAPUI5 Technical Mock Interview

This document simulates a real SAPUI5 interview.

Questions progress from Beginner → Intermediate → Advanced.

Try answering each question before reading the answer.

---

# Round 1 — Introduction

## Q1. Tell me about yourself.

Focus on:

- SAP ABAP Background
- SAPUI5
- OData
- Fiori
- Current Project
- Strengths

---

## Q2. What is SAPUI5?

SAPUI5 is SAP's JavaScript framework used to build responsive enterprise web applications.

---

## Q3. Is SAPUI5 a Framework or Library?

Framework.

---

## Q4. Which Architecture does SAPUI5 follow?

MVC Architecture.

---

## Q5. What technologies are used in SAPUI5?

- HTML5
- CSS3
- JavaScript
- XML
- JSON
- OData

---

# Round 2 — Project Structure

## Q6. Explain SAPUI5 project structure.

Expected answer:

- webapp
- Component.js
- manifest.json
- controller
- view
- model
- css
- i18n

---

## Q7. Why is Component.js needed?

Application entry point.

---

## Q8. Why is manifest.json called the Application Descriptor?

Because it contains the complete application configuration.

---

## Q9. What is Root View?

First View loaded by the application.

---

## Q10. What is metadata?

Configuration object of Component.js.

---

# Round 3 — MVC

## Q11. Explain MVC.

Model

↓

View

↓

Controller

---

## Q12. What is the Model?

Stores application data.

---

## Q13. What is the View?

Displays UI.

---

## Q14. What is the Controller?

Handles business logic.

---

## Q15. Why MVC?

Better maintainability.

---

# Round 4 — Routing

## Q16. What is Routing?

Navigation between Views.

---

## Q17. What is Router?

Handles navigation.

---

## Q18. Difference between Route and Target?

Route

URL Pattern

Target

View

---

## Q19. What is navTo()?

Navigates between Routes.

---

## Q20. What happens if Router is not initialized?

Navigation will not work.

---

# Round 5 — Data Binding

## Q21. What is Data Binding?

Connecting Model with View.

---

## Q22. Types of Binding?

- Property
- Aggregation
- Element

---

## Q23. Binding Modes?

- One Way
- Two Way
- One Time

---

## Q24. Difference between Absolute and Relative Binding?

Absolute

Starts with "/"

Relative

Uses current context.

---

## Q25. What is Expression Binding?

Simple calculations inside XML.

---

# Round 6 — Models

## Q26. Which Models have you used?

- JSONModel
- ResourceModel
- DeviceModel
- ODataModel

---

## Q27. Difference between Default and Named Model?

Default

```
{/name}
```

Named

```
{employee>/name}
```

---

## Q28. What is DeviceModel?

Stores device information.

---

## Q29. What is ResourceModel?

Used for i18n.

---

## Q30. Why ODataModel?

Backend communication.

---

# Round 7 — OData

## Q31. What is OData?

REST protocol.

---

## Q32. CRUD Operations?

Create

Read

Update

Delete

---

## Q33. HTTP Methods?

GET

POST

PUT

PATCH

DELETE

---

## Q34. What is Entity?

Single object.

---

## Q35. What is Entity Set?

Collection of Entities.

---

## Q36. What is Metadata?

Service definition.

---

## Q37. Difference between PUT and PATCH?

PUT

Entire record.

PATCH

Selected fields.

---

## Q38. What is $filter?

Filters records.

---

## Q39. What is $expand?

Fetches related entities.

---

## Q40. What is Batch Processing?

Multiple requests in one HTTP request.

---

# Round 8 — SAP Fiori

## Q41. What is SAP Fiori?

SAP UX Design System.

---

## Q42. Difference between SAPUI5 and Fiori?

SAPUI5

Framework.

Fiori

Design System.

---

## Q43. What is Launchpad?

Entry point of applications.

---

## Q44. What are Tiles?

Application shortcuts.

---

## Q45. Fiori Elements vs Freestyle?

Metadata Driven

vs

Code Driven.

---

# Round 9 — Advanced

## Q46. What are Fragments?

Reusable UI Components.

---

## Q47. Why use Fragments?

Avoid duplicate UI.

---

## Q48. Formatter vs Expression Binding?

Formatter

Complex logic.

Expression

Simple logic.

---

## Q49. What is MessageManager?

Handles validation messages.

---

## Q50. What is Lazy Loading?

Load Views only when required.

---

## Q51. How do you improve performance?

- Lazy Loading
- Batch Requests
- $select
- Destroy controls
- Reuse Fragments

---

## Q52. Which testing framework have you used?

QUnit

OPA5

---

## Q53. Difference between View and Fragment?

View

Independent.

Fragment

Reusable.

---

## Q54. Which lifecycle methods have you used?

- onInit()
- onBeforeRendering()
- onAfterRendering()
- onExit()

---

## Q55. Difference between onInit() and Constructor?

onInit()

Controller lifecycle.

Constructor

JavaScript object creation.

---

# Scenario-Based Questions

## Q56.

A button click is not navigating.

How will you debug?

Expected points:

- Check Route Name
- Router Initialized
- manifest.json
- Browser Console
- Network

---

## Q57.

Data is not appearing in Table.

Possible reasons?

- Wrong Model
- Wrong Path
- Service Error
- Binding Error

---

## Q58.

Application is slow.

What will you do?

- Batch Requests
- Lazy Loading
- Reduce OData Calls
- Destroy Controls

---

## Q59.

User reports a blank screen.

How do you troubleshoot?

- Console Errors
- Network Tab
- manifest.json
- Component.js
- Browser Logs

---

## Q60.

How would you structure a large SAPUI5 project?

- MVC
- Named Models
- Base Controller
- Reusable Fragments
- Utility Classes
- Modular Components

---

# Rapid Fire

- What is UIComponent?
- What is Core?
- What is XML View?
- What is JSONModel?
- What is OData?
- What is Fragment?
- What is Formatter?
- What is Router?
- What is Target?
- What is Route?
- What is DeviceModel?
- What is ResourceModel?
- What is Component.js?
- What is manifest.json?
- What is i18n?
- What is navTo()?
- What is getRouter()?
- What is setModel()?
- What is getModel()?
- What is setProperty()?
- What is getProperty()?

---

# Final Interview Tips

✔ Explain concepts with real project examples.

✔ Mention your WorkSphere project while answering architecture questions.

✔ Draw MVC and Routing diagrams on paper if allowed.

✔ Focus on "why" as well as "what".

✔ If you don't know an answer, explain your thought process instead of guessing.

✔ Be confident with Component.js, manifest.json, Routing, Data Binding, and OData—these are the most frequently asked topics.

---

# Final Revision

SAPUI5

↓

MVC

↓

Component.js

↓

manifest.json

↓

Routing

↓

Data Binding

↓

Models

↓

OData

↓

SAP Fiori

↓

Advanced SAPUI5

↓

Mock Interview Ready