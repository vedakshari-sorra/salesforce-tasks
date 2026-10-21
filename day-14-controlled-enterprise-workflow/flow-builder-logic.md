# Flow Builder Logic

## Overview

Flow Builder is Salesforce's primary automation tool used to create workflows and automate business processes without writing code.

---

## What is Flow Builder?

Flow Builder allows users to:

- Automate tasks
- Guide users through screens
- Update records automatically
- Create business logic
- Integrate with Salesforce data

---

## Common Flow Types

### Screen Flow

Provides user interaction through screens.

### Record-Triggered Flow

Runs automatically when records are created, updated, or deleted.

### Scheduled Flow

Runs automatically at specified times.

### Autolaunched Flow

Runs in the background without user interaction.

---

## Important Flow Elements

### Get Records

Retrieves records from Salesforce.

### Create Records

Creates new records.

### Update Records

Updates existing records.

### Delete Records

Deletes records.

### Assignment

Assigns values to variables.

### Decision

Evaluates conditions and determines flow paths.

Example:

```text
If Amount > 10000
    Manager Approval Required
Else
    Auto Approve
```

### Loop

Iterates through a collection of records.

---

## Example Flow Logic

```text
Start
   ↓
Get Opportunity
   ↓
Decision
   ↓
Amount > 50000 ?
   ↓
Yes → Notify Manager
No → Update Record
```

---

## Benefits

- Low-code automation
- Easy maintenance
- Reusable logic
- Improved productivity

---

## Conclusion

Flow Builder is a powerful automation tool that enables organizations to automate complex business processes efficiently.
