# Day 5 - Apex Introduction

## 1. What is Apex?

Apex is a programming language used in 
Salesforce to write custom business logic.
It is similar to Java and runs on the 
Salesforce platform.

Apex is used when:
- Flow and configuration are not enough
- Complex calculations are needed
- External system connections required
- Bulk data processing needed

---

## 2. Difference

### Flow vs Apex

| Flow | Apex |
|------|------|
| No code needed | Code is required |
| Point and click | Write Java-like code |
| Simple automation | Complex logic |
| Cannot call external APIs | Can call external APIs |
| Limited conditions | Unlimited conditions |
| Slower for bulk | Faster for bulk |

### Configuration vs Coding

| Configuration | Coding (Apex) |
|--------------|----------------|
| Use for simple tasks | Use for complex tasks |
| Anyone can do it | Developer needed |
| Examples: Fields, Flows | Examples: Apex Classes |
| No programming knowledge | Programming knowledge needed |

---

## 3. Real Examples Where Apex is Needed

### Example 1 - Complex Fee Calculation
Fee depends on course type, student 
category, scholarship, and late payment.
Flow cannot handle all these together.
Apex calculates everything at once!

### Example 2 - External Payment Integration
Connecting Salesforce to PayTM or 
Razorpay payment gateway needs Apex.
Flow cannot make external API calls.
Apex can send and receive data from
any external system!

### Example 3 - Advanced Eligibility Check
Student eligibility needs attendance,
marks, fee status all checked together.
Too complex for Flow.
Apex handles all conditions at once!

---

## 4. Integrated System Design

### College Management System

**CRM:**
Student admission pipeline tracking
from inquiry to enrollment

**Objects:**
- Student (stores student data)
- Course (stores course details)
- Faculty (stores teacher info)
- Department (stores dept info)

**Relationships:**
- Student looks up to Course
- Course looks up to Department
- Faculty looks up to Department

**Validation:**
- Email cannot be empty
- Age cannot be negative
- Seats cannot exceed limit

**Flow:**
- Auto email after registration
- Notify faculty when course full
- Send fee reminder automatically

**Apex:**
- Complex fee calculation
- External payment integration
- Bulk student record processing

---

## 5. Pseudocode Examples

### Logic 1 - Block Registration if Full
IF Course.Remaining_Seats = 0
THEN
  Show message "Course is Full"
  Block student registration
ELSE
  Allow registration
  Reduce seats by 1
END IF

### Logic 2 - Notify Low Attendance
IF Student.Attendance < 75%
THEN
  Send email to student
  Send alert to faculty
  Add warning to record
ELSE
  Attendance is fine
END IF

### Logic 3 - Auto Generate Student ID
WHEN new Student record created
DO
  Count existing students
  Generate ID = STU + Count + 1
  Save ID to Student record
END

### Logic 4 - Fee Reminder
IF Fee_Due_Date - TODAY = 7
THEN
  Send reminder email
  Create task for admin
ELSE IF Fee_Due_Date < TODAY
THEN
  Add late fee penalty
  Send urgent reminder
END IF

---

## 6. Reflection

### Why Enterprise Systems Eventually Need Programming?

1. Complexity
   Business rules become too complex
   for point and click tools

2. External Connections
   Cannot connect to banks or payment
   systems without code

3. Bulk Processing
   Flow handles one record at a time
   Apex handles thousands at once

4. Custom Algorithms
   Complex calculations need real
   programming logic

5. Performance
   Apex is faster for complex operations

6. Flexibility
   Every business has unique needs
   that configuration cannot handle

CONCLUSION:
Configuration is great for simple tasks.
Apex is needed when logic becomes
complex, external connections needed,
or bulk processing is required!

---

## Screenshots
![accountutils](accountutils.png)
![stringlisttest](stringlisttest.png)


**Date:** 15 May 2026
**Day:** Day 5 - Apex Introduction
