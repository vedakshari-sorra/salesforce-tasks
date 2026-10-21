# Aura Components Basics (Overview)

## Introduction

Aura Components are reusable building blocks used to create Salesforce applications.

Aura was the primary Lightning framework before Lightning Web Components.

---

## Aura Component Structure

```text
MyComponent
│
├── MyComponent.cmp
├── MyComponentController.js
├── MyComponentHelper.js
└── MyComponent.css
```

---

## Component Example

```html
<aura:component>

    <h1>Hello Aura</h1>

</aura:component>
```

---

## Controller Example

```javascript
({
    handleClick : function(
        component,
        event,
        helper
    ) {

        alert('Button Clicked');

    }
})
```

---

## Features

- Component-based architecture
- Event-driven communication
- Reusable UI elements
- Client-side rendering

---

## Aura vs LWC

| Aura | LWC |
|------|-----|
| Older framework | Modern framework |
| Custom programming model | Standard web standards |
| More complex | Simpler |
| Lower performance | Better performance |

---

## Benefits

- Reusable components
- Modular development
- Dynamic interfaces
- Salesforce integration

---

## Conclusion

Aura Components introduced component-based development and paved the way for Lightning Web Components.
