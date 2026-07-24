# manifest.json

---

# What is manifest.json?

manifest.json is the Application Descriptor File of a SAPUI5 application.

It contains the application's configuration such as routing, models, dependencies, libraries, root view, application information, and startup settings.

Instead of hardcoding configurations inside Component.js, SAPUI5 reads them from manifest.json.

---

# Why is manifest.json Needed?

Before manifest.json,

developers configured routing, models, dependencies, and other settings manually in JavaScript.

With manifest.json,

all application configuration is centralized in a single file.

This makes applications easier to maintain and extend.

---

# Why is it called the Application Descriptor?

Because it describes the entire application.

It contains:

- Application Information
- Libraries
- Dependencies
- Models
- Routing
- Root View
- Resources
- Services

Everything required to start the application.

---

# Location

```
webapp/

└── manifest.json
```

---

# Main Sections of manifest.json

```
manifest.json

│

├── sap.app

├── sap.ui

├── sap.ui5
```

---

# sap.app

Contains basic application information.

Example:

```json
"sap.app": {
    "id": "com.apurv.worksphere",
    "type": "application",
    "title": "{{appTitle}}",
    "description": "{{appDescription}}"
}
```

Common properties:

- id
- type
- title
- description
- applicationVersion
- dataSources

---

# sap.ui

Contains UI-related configuration.

Example:

```json
"sap.ui": {
    "technology": "UI5",
    "icons": {},
    "deviceTypes": {}
}
```

It defines how the application behaves on different devices.

---

# sap.ui5

This is the largest and most important section.

It contains:

- Root View
- Models
- Routing
- Dependencies
- Content Densities
- Resources

---

# Root View

Defines the first View loaded when the application starts.

Example:

```json
"rootView": {
    "viewName": "com.apurv.worksphere.view.App",
    "type": "XML",
    "async": true,
    "id": "App"
}
```

---

# Dependencies

Defines the libraries required by the application.

Example:

```json
"dependencies": {
    "libs": {
        "sap.m": {},
        "sap.ui.core": {},
        "sap.f": {}
    }
}
```

SAPUI5 loads these libraries automatically.

---

# Models

Defines application Models.

Example:

```json
"models": {
    "i18n": {
        "type": "sap.ui.model.resource.ResourceModel",
        "settings": {
            "bundleName": "com.apurv.worksphere.i18n.i18n"
        }
    }
}
```

Models can also include:

- JSONModel
- ODataModel
- ResourceModel

---

# Routing

Defines navigation between Views.

Example:

```json
"routing": {

}
```

Routing contains:

- config
- routes
- targets

---

# Content Densities

Determines the UI density.

Examples:

```
Compact

Cozy
```

Compact

- Desktop Applications

Cozy

- Tablet
- Mobile

---

# Resources

Used for loading CSS and JavaScript files.

Example:

```json
"resources": {
    "css": [
        {
            "uri": "css/style.css"
        }
    ]
}
```

---

# Data Sources

Defines backend services.

Example:

```json
"dataSources": {
    "mainService": {
        "uri": "/sap/opu/odata/sap/ZEMPLOYEE_SRV/",
        "type": "OData"
    }
}
```

Usually used with ODataModel.

---

# Real-Time Example

WorkSphere

```
manifest.json

↓

Application Information

↓

Libraries

↓

Models

↓

Routing

↓

Dashboard View

↓

Employee Module

↓

Settings Module
```

---

# Advantages

✔ Centralized Configuration

✔ Easy Maintenance

✔ Automatic Library Loading

✔ Cleaner Component.js

✔ Better Project Structure

✔ Enterprise Standard

---

# Common Mistakes

❌ Hardcoding configuration inside Component.js.

Use manifest.json whenever possible.

---

❌ Forgetting to declare required libraries.

The application may fail to load controls.

---

❌ Incorrect Model names.

Bindings will not work if model names do not match.

---

❌ Incorrect Routing configuration.

Navigation between Views will fail.

---

# Best Practices

- Keep application configuration inside manifest.json.
- Load libraries only when required.
- Define Models in manifest.json.
- Configure Routing centrally.
- Keep Component.js lightweight.

---

# Interview Questions

## What is manifest.json?

manifest.json is the Application Descriptor File that stores the application's configuration.

---

## Why is manifest.json called the Application Descriptor?

Because it describes the complete application including routing, models, libraries, dependencies, and startup configuration.

---

## Where is manifest.json located?

```
webapp/manifest.json
```

---

## Which file loads manifest.json?

Component.js.

---

## Which section contains application information?

sap.app

---

## Which section contains UI configuration?

sap.ui

---

## Which section contains Models and Routing?

sap.ui5

---

## What is Root View?

The first View loaded when the application starts.

---

## Why are dependencies declared?

To load the required SAPUI5 libraries automatically.

---

## Where are Models defined?

Inside the `sap.ui5` section.

---

## Where is Routing configured?

Inside the `sap.ui5.routing` section.

---

## What are Content Densities?

They define whether the application uses Compact or Cozy mode based on the device.

---

## Can OData services be configured in manifest.json?

Yes.

They are typically configured under `sap.app.dataSources`.

---

# Quick Revision

manifest.json

↓

Application Descriptor

↓

sap.app

↓

sap.ui

↓

sap.ui5

↓

Root View

↓

Models

↓

Routing

↓

Dependencies

↓

Enterprise Configuration