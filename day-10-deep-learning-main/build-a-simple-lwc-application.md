# Build a Simple LWC Application

## Overview

Lightning Web Components (LWC) are reusable UI components built using modern web standards.

---

## LWC Structure

A basic component contains:

```text
helloWorld
│
├── helloWorld.html
├── helloWorld.js
└── helloWorld.js-meta.xml
```

---

## HTML File

```html
<template>
    <h1>Hello Salesforce!</h1>
</template>
```

---

## JavaScript File

```javascript
import { LightningElement } from 'lwc';

export default class HelloWorld
extends LightningElement {
}
```

---

## Meta XML File

```xml
<?xml version="1.0" encoding="UTF-8"?>

<LightningComponentBundle
    xmlns="http://soap.sforce.com/2006/04/metadata">

    <apiVersion>60.0</apiVersion>

    <isExposed>true</isExposed>

    <targets>
        <target>
            lightning__AppPage
        </target>
    </targets>

</LightningComponentBundle>
```

---

## Steps to Build

1. Create LWC Component
2. Write HTML Markup
3. Add JavaScript Logic
4. Configure Meta XML
5. Deploy Component
6. Add to Lightning Page

---

## Benefits

- Reusable
- Fast
- Easy to maintain
- Modern development approach

---

## Conclusion

LWC provides a modern and efficient way to build Salesforce user interfaces.
