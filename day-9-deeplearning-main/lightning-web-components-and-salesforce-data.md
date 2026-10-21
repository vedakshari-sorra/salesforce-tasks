# Lightning Web Components and Salesforce Data

## Overview

Lightning Web Components (LWC) can access Salesforce data using Lightning Data Service, Apex methods, and the Wire Service.

---

## Lightning Data Service

Lightning Data Service provides easy access to Salesforce records without writing Apex code.

### Example

```javascript
import { getRecord } from 'lightning/uiRecordApi';
```

---

## Wire Service

The Wire Service connects a component to Salesforce data.

### Example

```javascript
import { LightningElement, wire } from 'lwc';
import getAccounts from '@salesforce/apex/AccountController.getAccounts';

export default class AccountList extends LightningElement {

    @wire(getAccounts)
    accounts;
}
```

---

## Imperative Apex Calls

Used when data retrieval needs to happen on demand.

```javascript
getAccounts()
    .then(result => {
        this.accounts = result;
    })
    .catch(error => {
        console.error(error);
    });
```

---

## Benefits

- Faster development
- Real-time data access
- Reduced server calls
- Better performance

---

## Conclusion

LWC provides multiple ways to access Salesforce data, making applications more dynamic and efficient.
