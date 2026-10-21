# Visualforce + Aura

## Visualforce

### Overview

Visualforce is a Salesforce framework used to build custom user interfaces.

### Example

```html
<apex:page>
    <h1>Hello Salesforce</h1>
</apex:page>
```

### Features

- Tag-based markup
- Apex controller integration
- Custom page creation
- Server-side rendering

---

## Aura Components

### Overview

Aura is a component-based framework for building dynamic Salesforce applications.

### Component Example

```html
<aura:component>
    <h1>Hello Aura Component</h1>
</aura:component>
```

### Controller Example

```javascript
({
    handleClick : function(component, event, helper) {
        alert('Button Clicked');
    }
})
```

### Features

- Component-based architecture
- Event-driven design
- Reusable components
- Client-side rendering

---

## Visualforce vs Aura

| Visualforce | Aura |
|------------|------|
| Page-based | Component-based |
| Older framework | Modern framework |
| Server rendering | Client rendering |
| Limited interactivity | Highly interactive |

---

## Conclusion

Visualforce and Aura are important Salesforce UI technologies that laid the foundation for modern Lightning Web Components.
