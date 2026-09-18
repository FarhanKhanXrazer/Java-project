# Java-project
# Smart Campus Event & Resource Management System

## Project Overview

The Smart Campus Event & Resource Management System is a console-based Java application developed to simplify the management of campus events, student registrations, and resource bookings. The system provides a centralized platform for students and administrators to manage events efficiently while maintaining records using file handling.

This project demonstrates the practical implementation of Object-Oriented Programming (OOP) concepts, file handling, exception handling, collections, and modular software design in Java.

---

# Problem Statement

Many colleges and educational institutions manage events, registrations, and resource bookings manually. This often results in scheduling conflicts, poor record management, duplication of information, and inefficient communication.

The Smart Campus Event & Resource Management System provides a centralized solution to automate these tasks and improve efficiency.

---

# Objectives

* Simplify event management processes.
* Maintain participant records efficiently.
* Manage resource bookings and prevent scheduling conflicts.
* Generate useful reports.
* Demonstrate Java programming concepts in a real-world application.

---

# Scope of the Project

The system provides:

* User Registration and Login
* Event Creation and Management
* Event Registration
* Resource Booking
* Conflict Detection
* Report Generation
* File-Based Data Storage

Target Users:

* Students
* Faculty Members
* Administrators

---

# Features

## User Management

* User Registration
* User Login Authentication
* Role-based Access

## Event Management

* Create Events
* View Events
* Delete Events
* Manage Event Records

## Event Registration

* Register Students for Events
* Maintain Registration Records

## Resource Booking

* Book Resources
* Detect Booking Conflicts
* Store Booking Details

## Report Generation

* Generate Event Reports
* Display Registration Details
* Display Booking Information

## File Storage

* Persistent Storage using Text Files
* Read and Write Operations

---

# Functional Requirements

1. User Registration
2. User Login
3. Event Creation
4. Event Registration
5. Resource Booking
6. Booking Conflict Detection
7. Report Generation
8. Data Storage in Files

---

# Non-Functional Requirements

* Performance
* Reliability
* Security
* Maintainability
* Usability
* Error Handling

---

# Technologies Used

* Java
* Object-Oriented Programming
* Collections Framework
* File Handling
* Exception Handling
* VS Code

---

# System Architecture

```text
+----------------------+
|     Console UI       |
+----------+-----------+
           |
           v
+----------------------+
| Authentication Layer |
+----------------------+
           |
           v
+----------------------+
| Event Management     |
| Booking Management   |
| Registration Module  |
| Report Module        |
+----------+-----------+
           |
           v
+----------------------+
| File Storage Layer   |
| users.txt            |
| events.txt           |
| bookings.txt         |
+----------------------+
```

---

# Workflow

```text
Start
  |
Login/Register
  |
Select Role
  |
Choose Operation
  |
Perform Action
  |
Save Data
  |
Generate Reports
  |
Exit
```

---

# UML Design

## Use Case Diagram

Student:

* Register
* Login
* View Events
* Register for Events
* Book Resources

Admin:

* Login
* Create Events
* Delete Events
* Manage Resources
* Generate Reports

---

## Class Diagram

```text
                User
                  |
        -------------------
        |                 |
     Student          Admin

EventManager ----- Event
BookingManager --- Booking

AuthenticationManager
RegistrationManager
ReportGenerator
FileManager

Main
```

---

## Sequence Diagram

```text
Student -> Main : Login
Main -> AuthenticationManager : validateUser()
AuthenticationManager -> users.txt : readData()
AuthenticationManager -> Main : success

Student -> EventManager : viewEvents()
EventManager -> events.txt : readEvents()
EventManager -> Student : displayEvents()

Student -> RegistrationManager : registerEvent()
RegistrationManager -> events.txt : updateRecords()
RegistrationManager -> Student : confirmation
```

---

# Project Structure

```text
SmartCampusSystem/
│
├── src/
│   ├── Main.java
│   ├── User.java
│   ├── Student.java
│   ├── Admin.java
│   ├── Event.java
│   ├── EventManager.java
│   ├── Booking.java
│   ├── BookingManager.java
│   ├── RegistrationManager.java
│   ├── AuthenticationManager.java
│   ├── ReportGenerator.java
│   └── FileManager.java
│
├── data/
│   ├── users.txt
│   ├── events.txt
│   └── bookings.txt
│
├── README.md
└── statement.md
```

---

# Sample Data Files

## users.txt

```text
farhan,password123,STUDENT
admin,admin123,ADMIN
```

## events.txt

```text
E101,Java Workshop,20-10-2026,100
E102,Hackathon,25-10-2026,200
```

## bookings.txt

```text
B001,Lab1,20-10-2026,Farhan
```

---

# Testing

| Test Case         | Expected Result         |
| ----------------- | ----------------------- |
| Valid Login       | Login Successful        |
| Invalid Login     | Error Message           |
| Create Event      | Event Added             |
| Register Event    | Registration Successful |
| Duplicate Booking | Conflict Detected       |
| Generate Report   | Report Generated        |

---

# Challenges Faced

* Designing a modular architecture.
* Managing persistent storage using text files.
* Implementing booking conflict detection.
* Handling invalid user inputs.
* Maintaining code reusability.

---

# Learnings & Key Takeaways

* Object-Oriented Programming
* Inheritance and Polymorphism
* Exception Handling
* File Handling
* Collections Framework
* Modular Software Development

---

# Future Enhancements

* Java Swing GUI
* Database Integration
* Email Notifications
* QR-based Attendance
* Cloud Deployment
* Mobile Application

---

# Installation & Execution

1. Clone the repository.
2. Open the project in VS Code.
3. Compile all Java files.

```bash
javac *.java
```

4. Run the application.

```bash
java Main
```

---

# References

1. Oracle Java Documentation
2. Java SE API Documentation
3. VS Code Java Extension Pack
4. GeeksforGeeks Java Tutorials
5. Java Collections Framework Documentation

---

# Author

Individual Project Submission

Course: Programming in Java

Project Title: Smart Campus Event & Resource Management System
