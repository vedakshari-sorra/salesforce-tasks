# Visualforce Basics

## Overview

Visualforce is a framework used to build custom Salesforce user interfaces.

---

## Features

- Tag-based markup language
- Apex controller integration
- Custom page development
- Server-side rendering

---

## Basic Visualforce Page

```html
<apex:page>
    <h1>Hello Salesforce</h1>
</apex:page>
```

---

## Visualforce with Apex Controller

### Apex Controller

```apex
public class HelloController {

    public String message {
        get {
            return 'Hello Salesforce';
        }
    }
}
```

### Visualforce Page

```html
<apex:page controller="HelloController">

    <h2>{!message}</h2>

</apex:page>
```

---

## Common Components

### Input Field

```html
<apex:inputText />
```

### Command Button

```html
<apex:commandButton
    value="Submit" />
```

### Page Block

```html
<apex:pageBlock
    title="Account Information">
</apex:pageBlock>
```

---

## Advantages

- Easy UI development
- Apex integration
- Custom layouts
- Salesforce security support

---

## Conclusion

Visualforce remains an important Salesforce technology for building custom interfaces and integrating with Apex controllers.
