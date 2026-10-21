# Day 6 - Apex Introduction

## 1. What is Apex?
Apex is Salesforce programming language
used for complex business logic that
configuration cannot handle.

## 2. Difference: Flow vs Apex

| Flow | Apex |
|------|------|
| No code | Requires code |
| Simple tasks | Complex tasks |
| Cannot call APIs | Can call APIs |
| One record | Bulk processing |

## 3. Real Examples Where Apex Needed

### Example 1 - Complex Fee Calculation
Multiple conditions like course type,
scholarship, penalty cannot be handled
by Flow. Apex calculates everything!

### Example 2 - Payment Integration
Connecting to PayTM or Razorpay needs
HTTP callouts only possible in Apex!

### Example 3 - Eligibility Check
Checking attendance, marks, fees all
together is too complex for Flow!

## 4. Integrated System Design

CRM: Student admission pipeline
Objects: Student, Course, Faculty, Department
Relationships: Student → Course → Department
Validation: Email required, Age positive
Formula: Remaining seats auto calculated
Flow: Auto email on registration
Apex: Complex fee calculation logic

## 5. Pseudocode Examples

IF seats = 0
THEN block registration

IF attendance < 75%
THEN notify student and faculty

IF fee_due - today = 7
THEN send reminder email

## 6. Reflection

Enterprise systems need programming because:
- Business logic becomes too complex
- External connections required
- Bulk processing needed
- Custom algorithms necessary
- Better performance with code
- Maximum flexibility with Apex

screenshot
<img width="769" height="1012" alt="accountaccounttrigger" src="https://github.com/user-attachments/assets/1d05db88-aa6c-4158-b26b-4d2f48e2de19" />
<img width="1898" height="913" alt="aat" src="https://github.com/user-attachments/assets/22a79502-be22-4f2e-ab1a-6bc5b2dd6ff2" />


**Day:** Day 6 - Apex Introduction
