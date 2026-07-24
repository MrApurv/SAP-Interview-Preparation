# Component.js

---

# What is Component.js?

Component.js is the entry point of a SAPUI5 application.

It initializes the application, loads the manifest.json file, sets up Models, initializes Routing, and prepares the application before the first View is displayed.

---

# Why is Component.js Needed?

Without Component.js,

every View would need to initialize Models, Routing, and application settings separately.

Component.js provides a centralized place for application initialization.

---

# Responsibilities of Component.js

- Starts the application
- Loads manifest.json
- Initializes Routing
- Creates Global Models
- Loads Device Model
- Initializes Services
- Configures Application Metadata

---

# Application Startup Flow

```
User Opens Application

↓

index.html

↓

Component.js

↓

manifest.json

↓

Models

↓

Routing

↓

Root View

↓

Application Ready
```

---

# Basic Structure

```javascript
sap.ui.define([
    "sap/ui/core/UIComponent"
], function (UIComponent) {
    "use strict";

    return UIComponent.extend("demo.Component", {

        metadata: {
            manifest: "json"
        },

        init: function () {

            UIComponent.prototype.init.apply(this, arguments);

            this.getRouter().initialize();

        }

    });

});
```

---

# UIComponent

Component.js extends the UIComponent class.

```javascript
return UIComponent.extend("demo.Component", {});
```

UIComponent provides built-in functionality such as:

- Routing
- Model Management
- Lifecycle Methods
- Manifest Loading
- Resource Management

---

# metadata

The metadata object contains application configuration.

Example:

```javascript
metadata: {
    manifest: "json"
}
```

This instructs SAPUI5 to load configuration from the manifest.json file.

---

# manifest : "json"

Instead of configuring everything in Component.js, SAPUI5 reads the application settings from manifest.json.

This includes:

- Routing
- Models
- Libraries
- Dependencies
- Root View
- Application Information

---

# init()

init() is the first lifecycle method executed when the application starts.

Typical tasks performed inside init():

- Call parent init()
- Create Models
- Set Device Model
- Initialize Routing
- Load User Settings
- Initialize Services

---

# Parent Initialization

```javascript
UIComponent.prototype.init.apply(this, arguments);
```

This calls the init() method of UIComponent.

It ensures that SAPUI5 performs its internal initialization before executing custom code.

---

# Routing Initialization

```javascript
this.getRouter().initialize();
```

This starts the routing mechanism.

Without this line:

- URL navigation will not work.
- navTo() will fail.
- Views will not load automatically.

---

# Device Model

Most SAPUI5 applications create a Device Model.

```javascript
this.setModel(models.createDeviceModel(), "device");
```

It stores information about:

- Desktop
- Tablet
- Phone
- Orientation
- Touch Support

Used for responsive applications.

---

# Global Models

Component.js is the ideal place to create global Models.

Example:

```javascript
this.setModel(oEmployeeModel, "employee");

this.setModel(oDashboardModel, "dashboard");
```

All Views can access these Models.

---

# Real-Time Example

WorkSphere

```
User Opens WorkSphere

↓

Component.js

↓

Load manifest.json

↓

Load Device Model

↓

Create Employee Model

↓

Initialize Routing

↓

Display Dashboard
```

---

# Advantages

✔ Centralized Application Initialization

✔ Global Model Management

✔ Routing Configuration

✔ Better Maintainability

✔ Enterprise Architecture

---

# Common Mistakes

❌ Forgetting to call:

```javascript
UIComponent.prototype.init.apply(this, arguments);
```

This may prevent proper framework initialization.

---

❌ Forgetting:

```javascript
this.getRouter().initialize();
```

Navigation will not work.

---

❌ Creating Models in every Controller.

Instead, create shared Models in Component.js whenever appropriate.

---

# Best Practices

- Keep initialization code inside Component.js.
- Load global Models only once.
- Use manifest.json for configuration.
- Initialize Routing inside init().
- Keep Component.js clean and lightweight.

---

# Interview Questions

## What is Component.js?

Component.js is the entry point of a SAPUI5 application. It initializes the application, loads the manifest.json file, creates Models, and initializes Routing.

---

## Why is Component.js important?

It centralizes application initialization and configuration, reducing code duplication and improving maintainability.

---

## Which class does Component.js extend?

UIComponent.

---

## What is the purpose of metadata?

It provides application configuration such as loading the manifest.json file.

---

## Why do we write?

```javascript
manifest: "json"
```

It instructs SAPUI5 to load application configuration from the manifest.json file.

---

## What is init()?

init() is the first lifecycle method executed when the application starts.

---

## Why is this line important?

```javascript
UIComponent.prototype.init.apply(this, arguments);
```

It calls the parent UIComponent initialization, ensuring the SAPUI5 framework is initialized correctly.

---

## What is the purpose of this line?

```javascript
this.getRouter().initialize();
```

It starts the routing mechanism and enables URL-based navigation.

---

## Where should global Models be created?

Inside Component.js.

---

## Where should DeviceModel be created?

Inside Component.js.

---

## Can multiple Views use the same Model?

Yes.

Models created in Component.js can be shared across all Views.

---

## Can we navigate without initializing the Router?

No.

Routing must be initialized before navigation can occur.

---

# Quick Revision

Component.js

↓

Application Entry Point

↓

Extends UIComponent

↓

Loads manifest.json

↓

Creates Global Models

↓

Loads Device Model

↓

Initializes Routing

↓

Starts Application