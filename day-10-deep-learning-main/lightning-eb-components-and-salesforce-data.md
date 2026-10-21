# Lightning Web Components and Salesforce Data

## Overview

LWC can retrieve and update Salesforce data using Lightning Data Service, Wire Service, and Apex methods.

---

## Lightning Data Service

Provides record access without Apex.

```javascript
import { getRecord }
from 'lightning/uiRecordApi';
```

---

## Wire Service

Used for reactive data access.

```javascript
import { LightningElement, wire }
from 'lwc';

import getAccounts
from '@salesforce/apex/AccountController.getAccounts';

export default class AccountList
extends LightningElement {

    @wire(getAccounts)
    accounts;
}
```

---

## Imperative Apex Call

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

## Data Operations

### Create Records

```javascript
createRecord(recordInput);
```

### Update Records

```javascript
updateRecord(recordInput);
```

### Delete Records

```javascript
deleteRecord(recordId);
```

---

## Benefits

- Real-time data access
- Reduced server calls
- Better performance
- Simplified development

---

## Conclusion

LWC provides multiple approaches for interacting with Salesforce data efficiently.
