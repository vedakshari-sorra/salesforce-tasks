# Day 3 - Data Modeling in Salesforce

## 1. Difference Between App, Object, Record and Field

### App
A collection of tabs and tools for a 
specific business purpose.
Example: College Management App

### Object
A table that stores specific type of data.
Example: Student, Course, Department

### Record
A single row of data inside an object.
Example: One student's information

### Field
A column inside an object.
Example: Student Name, Email, Age

---

## 2. Standard vs Custom Objects

### Standard Objects
Already built inside Salesforce.
Examples:
- Account
- Contact
- Opportunity
- Lead

### Custom Objects
Objects YOU create for your business.
Examples:
- Student
- Course
- Faculty
- Department

---

## 3. My College Data Model

### Objects Created:
- Student
- Course
- Faculty
- Department

### Relationships:
- Course → Department (Lookup)
- Faculty → Department (Lookup)
- Student → Course (Lookup)

### Diagram:

                +------------------+
                |   Department     |
                +------------------+
                | Department Name  |
                | HOD Name         |
                +------------------+
                    ↑          ↑
                    |          |
         Lookup     |          | Lookup
                    |          |
        +----------------+   +----------------+
        |    Course      |   |    Faculty     |
        +----------------+   +----------------+
        | Course Name    |   | Faculty Name   |
        | Duration       |   | Subject        |
        +----------------+   +----------------+

                    ↑
                    |
                Lookup
                    |
            +----------------+
            |    Student     |
            +----------------+
            | Student Name   |
            | Email          |
            | Age            |
            +----------------+

## Screenshots

![Course Object](course.png)

![Department Object](department.png)

![Faculty Object](faculty.png)

![Student Object](student.png)
