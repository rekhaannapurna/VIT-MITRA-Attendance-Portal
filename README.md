# VIT MITRA Club – Attendance Management & Analytics

A secure, role-based web application designed to centralize and simplify attendance management for the **VIT MITRA Club**.

The system replaces manual attendance maintenance with a centralized platform for managing students, teams, daily attendance, attendance history, analytics, and low-attendance identification.

---

## 📌 Project Overview

The **VIT MITRA Club – Attendance Management & Analytics Web Application** is designed for two primary users:

* **Admin**
* **Student**

Administrators can manage students, teams, attendance, and analytics, while students have view-only access to their own attendance information.

The system supports the four initial VIT MITRA teams:

* Vibe Coding
* AI
* Industrial Connect
* Marketing

The application is designed to maintain accurate attendance records while providing individual, weekly, monthly, team-wise, and overall attendance analytics.

---

## 🎯 Objectives

The main objectives of the system are to:

* Replace manual attendance maintenance.
* Centralize student and team information.
* Simplify daily attendance marking.
* Prevent duplicate attendance records.
* Provide accurate attendance percentage calculations.
* Provide weekly and monthly attendance analysis.
* Provide team-wise attendance analytics.
* Provide overall club attendance analytics.
* Identify students with low attendance.
* Maintain secure role-based access.
* Protect attendance data from unauthorized modification.

---

## 👥 User Roles

### 👨‍💼 Admin

Administrators have full management access to:

* Student records
* Team records
* Student-team assignments
* Daily attendance
* Attendance history
* Attendance corrections
* Attendance analytics
* Search and filtering
* Low-attendance identification

### 👨‍🎓 Student

Students have view-only access to:

* Their profile information
* Their team information
* Personal attendance history
* Attendance percentage
* Weekly attendance
* Monthly attendance

Students cannot modify attendance, team membership, or administrative data.

---

# ✨ Core Features

## 🔐 Authentication & Authorization

The system provides secure authentication and role-based authorization.

### Features

* User login
* Admin and Student roles
* Role-based access control
* Protected application pages
* Backend authorization
* Secure password handling
* Logout functionality
* Unauthorized-access protection

Only authenticated and authorized users can access protected functionality.

---

## 👨‍🎓 Student Management

Administrators can manage student records.

### Student Information

Each student record contains:

* Student ID
* Name
* Email
* Branch
* Year
* Section
* Team
* Phone
* Account Status

### Admin Operations

Administrators can:

* Create student records
* View student records
* Update student details
* Deactivate student records
* Search students
* Filter students
* Assign students to teams
* Change student team assignments

Each Student ID must remain unique.

---

## 👥 Team Management

The system supports team management for VIT MITRA.

### Initial Teams

1. Vibe Coding
2. AI
3. Industrial Connect
4. Marketing

Administrators can:

* Create teams
* Edit teams
* Deactivate teams
* Assign students to teams
* Change student team assignments

Historical attendance must remain logically accurate when a student's current team changes.

---

# 📝 Daily Attendance Management

Administrators can manage daily attendance for club members.

### Attendance Operations

The system allows administrators to:

* Select an attendance date
* View students grouped by team
* Mark students as **Present**
* Mark students as **Absent**
* Mark attendance for a team
* Mark attendance for the entire club
* Correct existing attendance records

### Attendance Rules

* Attendance status must be either **Present** or **Absent**.
* A student must have a valid student record.
* Duplicate attendance for the same student and date/session must be prevented.
* Attendance changes must update relevant analytics.
* Historical attendance must remain logically consistent.

---

# 📚 Attendance History

The system maintains attendance history for administrators and students.

### Admin Access

Administrators can:

* View attendance history
* Search attendance records
* Filter by student
* Filter by team
* Filter by date
* Filter by date range
* Filter by attendance status

### Student Access

Students can:

* View their own attendance history
* View attendance dates
* View attendance status
* View attendance percentage

Students cannot edit or delete attendance history.

---

# 📊 Attendance Analytics

The application provides multiple levels of attendance analysis.

## 👤 Individual Analytics

For each student, the system provides:

* Total recorded sessions
* Present sessions
* Absent sessions
* Attendance percentage
* Weekly attendance
* Monthly attendance
* Low-attendance identification

### Attendance Percentage

The attendance percentage is calculated as:

```text
Attendance Percentage =
(Present Sessions / Total Recorded Sessions) × 100
```

The low-attendance threshold is configurable.

---

## 👥 Team-wise Analytics

The system provides separate attendance analytics for each active team.

Team analytics include:

* Total students
* Present count
* Absent count
* Attendance percentage
* Weekly attendance analysis
* Monthly attendance analysis

The system allows administrators to compare attendance statistics across teams without modifying the underlying attendance data.

---

## 🏫 Overall Club Analytics

The Admin Dashboard provides overall club attendance statistics.

### Overall Metrics

* Total students
* Present count
* Absent count
* Overall attendance percentage
* Weekly attendance trends
* Monthly attendance trends

Changes to attendance records must be reflected in overall analytics.

---

# 📈 Dashboard & Visualization

The Admin Dashboard provides an overview of attendance activity.

Dashboard components include:

* Attendance summary cards
* Weekly attendance trends
* Monthly attendance trends
* Team-wise comparison charts
* Present vs. Absent visualization

Charts should clearly display:

* Dates
* Teams
* Values
* Legends where applicable

---

# 🔎 Search & Filtering

The application provides search and filtering functionality for efficient attendance management.

Administrators can search students using:

* Student ID
* Student Name

Attendance records can be filtered by:

* Team
* Date
* Date range
* Attendance status
* Student

---

# ⚠️ Low Attendance Identification

The system can identify students whose attendance falls below the configured attendance threshold.

This allows administrators to review students who require attendance monitoring.

---

# 🔒 Security Requirements

Security is a major requirement of the system.

The application is designed to ensure:

* Protected operations require authentication.
* Authorization is enforced on the backend.
* Passwords are securely hashed.
* Input validation is implemented.
* Sensitive authentication information is not exposed.
* Students cannot access administrative operations.
* Unauthorized API requests are rejected.
* Invalid student, team, date, and attendance information is rejected.

Attendance data must be protected from unauthorized access or modification.

---

# 🧩 Business Rules

The system follows the following core business rules:

1. Only authorized administrators can create, update, or delete student, team, and attendance records.
2. Students can only view their own attendance information.
3. Every attendance record must reference a valid student.
4. A student can have at most one attendance record for a particular attendance date/session.
5. Attendance percentage is calculated from recorded attendance sessions.
6. Changing a student's current team must not incorrectly rewrite historical attendance context.
7. Analytics must be refreshed or recalculated after attendance changes.
8. The low-attendance threshold must be configurable.
9. Duplicate Student IDs are not allowed.
10. Invalid attendance statuses are not allowed.
11. Historical attendance data must remain logically consistent when students or teams are deactivated.

---

# 🏗️ System Architecture

The SRS defines the following logical architecture:

```text
┌─────────────────────────────┐
│      Student / Admin        │
│          Browser            │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│       React Frontend        │
│ HTML / JSX / CSS / Tailwind │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│          REST API           │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ Spring Boot Backend         │
│ Spring Security             │
│ JPA / Hibernate             │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│       MySQL Database        │
└─────────────────────────────┘
```

The frontend is responsible for presentation and user interaction.

The backend is responsible for:

* Authentication
* Authorization
* Business logic
* Attendance processing
* Analytics
* Database access

The database stores and maintains student, team, and attendance information.

---

# 🛠️ Technology Stack

| Layer             | Technology                                 |
| ----------------- | ------------------------------------------ |
| Frontend          | React.js                                   |
| Markup            | HTML5 / JSX                                |
| Styling           | CSS / Tailwind CSS                         |
| Charts            | Recharts                                   |
| Backend           | Java                                       |
| Backend Framework | Spring Boot                                |
| Security          | Spring Security                            |
| Authentication    | JWT or secure session-based authentication |
| ORM               | Spring Data JPA / Hibernate                |
| Database          | MySQL                                      |
| API               | REST API                                   |
| API Testing       | Postman                                    |
| Version Control   | Git & GitHub                               |
| Development       | VS Code / IntelliJ IDEA                    |
| Browser           | Chrome / Edge / Firefox                    |

The technology stack above follows the SRS specification.

---

# 🔄 Attendance Workflow

```text
Admin Login
     │
     ▼
Admin Dashboard
     │
     ▼
Select Attendance Date
     │
     ▼
Select Team / Club
     │
     ▼
View Students
     │
     ▼
Mark Present / Absent
     │
     ▼
Validate Attendance
     │
     ▼
Save Attendance
     │
     ▼
Update Analytics
     │
     ▼
Student Views Personal Attendance
```

---

# 🧪 Testing Requirements

The system should be tested at multiple levels.

### Unit Testing

Test:

* Attendance percentage calculation
* Analytics calculations
* Attendance-related business logic

### API Testing

Test:

* Authentication
* Student APIs
* Team APIs
* Attendance APIs
* Analytics APIs

### Role-Based Access Testing

Verify that:

* Admins can perform administrative operations.
* Students cannot perform admin operations.
* Students can access only their own attendance information.

### Database Testing

Verify:

* Student relationships
* Team relationships
* Attendance relationships
* Duplicate attendance prevention
* Data integrity

### UI Testing

Test:

* Login
* Attendance marking
* Attendance filtering
* Dashboard
* Analytics
* Responsive layouts

### Security Testing

Test:

* Unauthorized access
* Invalid credentials
* Invalid input
* Protected API operations

### End-to-End Testing

The complete workflow should be tested:

```text
Login
  ↓
Attendance Marking
  ↓
Attendance Storage
  ↓
Analytics Calculation
  ↓
Student Attendance Viewing
```

---

# ✅ Acceptance Criteria

The system is expected to satisfy the following:

* Admin can securely log in.
* Student can log in.
* Admin can create, edit, search, and deactivate students.
* Admin can manage the four initial teams.
* Admin can assign students to teams.
* Admin can mark daily attendance.
* Admin can correct attendance.
* Duplicate attendance is prevented.
* Individual attendance percentage is calculated correctly.
* Weekly analytics are available.
* Monthly analytics are available.
* Team-wise analytics are available.
* Overall club analytics are available.
* Students cannot modify attendance.
* Students cannot modify team membership.
* Low-attendance students can be identified using the configured threshold.

---

# 🚀 Future Enhancements

The SRS identifies the following possible future enhancements:

* QR-code-based attendance
* Face-recognition-based attendance
* Excel/PDF attendance export
* Automated low-attendance notifications
* Email notifications
* WhatsApp notifications
* Multiple attendance sessions per day
* Multiple academic years
* Multiple club batches
* Administrative audit logs
* Progressive Web App / mobile application
* Cloud backup and deployment

Face recognition would require appropriate institutional approval and privacy considerations.

---

# 📁 Project Scope

The system covers the complete attendance-management lifecycle:

```text
Authentication
      ↓
Student Management
      ↓
Team Management
      ↓
Attendance Management
      ↓
Attendance History
      ↓
Individual Analytics
      ↓
Team Analytics
      ↓
Overall Club Analytics
      ↓
Low Attendance Review
```

---

# 📖 Documentation

The project requirements are defined in:

**Software Requirements Specification (SRS)**

**Document:** VIT MITRA Club – Attendance Management & Analytics
**Version:** 1.0

The SRS defines the functional requirements, non-functional requirements, architecture, use cases, business rules, testing requirements, acceptance criteria, and future enhancements for the system.

---

# 🎓 Project Purpose

The VIT MITRA Attendance Management & Analytics system is intended to provide a centralized and secure approach to managing club attendance.

It simplifies attendance marking for administrators, provides students with transparent access to their own attendance information, and enables meaningful attendance analysis at individual, team, and club levels.

---

# 👩‍💻 Development Team

**VIT MITRA Club**

Developed as a web-based attendance management and analytics solution for VIT MITRA Club.

---

## 📄 License

This project is developed for academic and institutional purposes.

---

## ⭐ Project Highlights

* Role-based authentication
* Student and Admin access
* Student management
* Team management
* Daily attendance
* Attendance history
* Individual analytics
* Weekly analytics
* Monthly analytics
* Team-wise analytics
* Overall club analytics
* Search and filtering
* Low-attendance identification
* Duplicate attendance prevention
* Secure backend authorization
* Responsive web interface

---

## 📌 Conclusion

The VIT MITRA Club Attendance Management & Analytics application provides a centralized solution for managing attendance, students, teams, and attendance analytics.

By replacing manual attendance maintenance with a structured web-based system, the application aims to improve data consistency, simplify attendance operations, and provide transparent attendance insights for both administrators and students.
