# Communicate Between Lightning Web Components

## Overview

Lightning Web Components can communicate with each other using parent-child relationships and events.

---

## Parent to Child Communication

Uses public properties decorated with @api.

### Child Component

```javascript
import { LightningElement, api } from 'lwc';

export default class ChildComponent extends LightningElement {

    @api message;
}
```

### Parent Component

```html
<c-child-component
    message="Hello Child">
</c-child-component>
```

---

## Parent Calling Child Methods

### Child Component

```javascript
@api
showMessage() {
    alert('Hello from Child');
}
```

### Parent Component

```javascript
const child =
this.template.querySelector(
    'c-child-component'
);

child.showMessage();
```

---

## Child to Parent Communication

Uses custom events.

### Child Component

```javascript
handleClick() {
    const event =
    new CustomEvent('notify');

    this.dispatchEvent(event);
}
```

### Parent Component

```html
<c-child-component
    onnotify={handleNotification}>
</c-child-component>
```

---

## Benefits

- Component reusability
- Loose coupling
- Better maintainability
- Improved scalability

---

## Conclusion

Component communication is essential for building interactive and reusable Lightning Web Components.
