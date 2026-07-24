# Models in SAPUI5

---

# What is a Model?

A Model is an object that stores and manages application data.

It acts as the bridge between the View and the Backend, providing data to the UI through Data Binding.

---

# Why are Models Needed?

Without Models,

developers would have to manually update UI controls whenever data changes.

Models provide automatic synchronization between the application data and the user interface.

---

# SAPUI5 Model Architecture

```
Backend

↓

Model

↓

Data Binding

↓

View
```

The View never communicates directly with the backend.

Instead, it retrieves data from the Model.

---

# Types of Models in SAPUI5

SAPUI5 provides multiple Model types.

The most commonly used are:

- JSONModel
- ResourceModel
- ODataModel
- DeviceModel

---

# JSONModel

JSONModel stores application data in JSON format.

It is mainly used for:

- Forms
- Temporary Data
- Local Application Data
- Small Datasets

Example

```javascript
const oModel = new sap.ui.model.json.JSONModel({
    name: "Apurv",
    department: "SAP"
});

this.getView().setModel(oModel);
```

---

# ResourceModel

ResourceModel is used for Internationalization (i18n).

Instead of writing:

```xml
<Button text="Save"/>
```

We write:

```xml
<Button text="{i18n>save}"/>
```

Text is stored inside:

```
i18n.properties
```

Example

```
save=Save
cancel=Cancel
```

---

# ODataModel

ODataModel is used to communicate with SAP Backend services.

It supports:

- Read
- Create
- Update
- Delete

Example

```javascript
const oModel = new sap.ui.model.odata.v2.ODataModel(
    "/sap/opu/odata/sap/ZEMPLOYEE_SRV/"
);
```

Enterprise SAP applications mostly use ODataModel.

---

# DeviceModel

DeviceModel stores information about the user's device.

Example

```javascript
this.setModel(models.createDeviceModel(), "device");
```

Information available:

- Desktop
- Tablet
- Phone
- Orientation
- Touch Support

---

# Default Model

A Default Model is assigned without a name.

Example

```javascript
this.getView().setModel(oModel);
```

Accessed as:

```xml
<Text text="{/name}"/>
```

---

# Named Model

A Named Model is assigned with a name.

Example

```javascript
this.getView().setModel(oModel, "employee");
```

Accessed as:

```xml
<Text text="{employee>/name}"/>
```

Named Models improve readability and organization.

---

# setModel()

Used to assign a Model.

Example

```javascript
this.getView().setModel(oModel);
```

---

# getModel()

Used to retrieve a Model.

Example

```javascript
const oModel = this.getView().getModel();
```

Named Model

```javascript
const oModel = this.getView().getModel("employee");
```

---

# setProperty()

Updates data inside a Model.

Example

```javascript
oModel.setProperty("/name", "Apurv");
```

The UI updates automatically.

---

# getProperty()

Reads data from a Model.

Example

```javascript
const sName = oModel.getProperty("/name");
```

---

# Model Hierarchy

Models can be assigned at different levels.

```
Core

↓

Component

↓

View

↓

Control
```

SAPUI5 searches for the nearest available Model.

---

# Global Models

Models created inside Component.js are available throughout the application.

Example

```javascript
this.setModel(oEmployeeModel, "employee");
```

All Views can access this Model.

---

# Real-Time Example

WorkSphere

```
Employee Data

↓

JSONModel

↓

Employee View

↓

User Updates Data

↓

Model Updated

↓

UI Refreshes Automatically
```

---

# Advantages

✔ Automatic Data Synchronization

✔ Clean MVC Architecture

✔ Reusable Data

✔ Easy Maintenance

✔ Better Performance

✔ Enterprise Ready

---

# Common Mistakes

❌ Creating the same Model in multiple Controllers.

Instead, create shared Models inside Component.js.

---

❌ Updating UI controls manually.

Instead, update the Model.

---

❌ Using JSONModel for enterprise backend data.

Use ODataModel for SAP backend communication.

---

❌ Hardcoding application text.

Use ResourceModel.

---

# Best Practices

- Use JSONModel for local data.
- Use ODataModel for backend communication.
- Use ResourceModel for translations.
- Use DeviceModel for responsive design.
- Prefer Named Models in large applications.
- Create global Models inside Component.js.

---

# Interview Questions

## What is a Model in SAPUI5?

A Model stores and manages application data and provides it to the View through Data Binding.

---

## What are the different Model types?

- JSONModel
- ResourceModel
- ODataModel
- DeviceModel

---

## Which Model is used for local data?

JSONModel.

---

## Which Model is used for internationalization?

ResourceModel.

---

## Which Model is used for SAP backend communication?

ODataModel.

---

## Which Model is used for responsive applications?

DeviceModel.

---

## What is the difference between Default Model and Named Model?

Default Model

```javascript
this.getView().setModel(oModel);
```

Binding

```xml
{/name}
```

Named Model

```javascript
this.getView().setModel(oModel, "employee");
```

Binding

```xml
{employee>/name}
```

---

## What does setModel() do?

It assigns a Model to the View or Component.

---

## What does getModel() do?

It retrieves an existing Model.

---

## What does setProperty() do?

It updates data inside a Model.

---

## What does getProperty() do?

It retrieves data from a Model.

---

## Where should global Models be created?

Inside Component.js.

---

## Can multiple Views share the same Model?

Yes.

If the Model is created at the Component level, all Views can access it.

---

## Why is ODataModel preferred in enterprise applications?

Because it communicates directly with SAP backend systems and supports CRUD operations.

---

# Quick Revision

Models

↓

Store Application Data

↓

JSONModel

↓

ResourceModel

↓

ODataModel

↓

DeviceModel

↓

setModel()

↓

getModel()

↓

setProperty()

↓

getProperty()

↓

Automatic Data Binding

↓

Enterprise Applications