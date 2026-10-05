# 🎓 VIT MITRA CLUB — Attendance Management & Analytics Platform

<p align="center">

### 📊 Smart • Secure • Centralized Attendance Management

**A web-based attendance management and analytics platform for VIT MITRA Club at Vishnu Institute of Technology.**

<p align="center">
  <a href="https://vit-mitra-attendance.vercel.app/">
    <strong>🚀 Live Website</strong>
  </a>
  •
  <a href="https://github.com/rekhaannapurna/VIT-MITRA-Attendance-Portal">
    <strong>💻 Source Code</strong>
  </a>
</p>

</p>

---

## 🌐 Live Application

### 🚀 [Open VIT MITRA Attendance Portal](https://vit-mitra-attendance.vercel.app/)

The application provides separate access paths for:

* 👨‍🎓 **Students**
* 🛡️ **Club Administrators**
* 📝 **Student Account Registration**
* 📊 **Attendance Dashboard**
* 👥 **Team Management**
* 📈 **Attendance Analytics**
* 📅 **Attendance History**

> **Live URL:** https://vit-mitra-attendance.vercel.app/

---

## 📌 About the Project

**VIT MITRA Club — Attendance Management & Analytics Platform** is a centralized web application designed to digitize and simplify attendance management for VIT MITRA Club.

The platform replaces manual attendance tracking with a structured digital system where administrators can manage students and attendance while students can securely access their own attendance information.

The application is designed around two primary roles:

| Role              | Access                                                         |
| ----------------- | -------------------------------------------------------------- |
| 👨‍🎓 Student     | Personal attendance, history, profile and account              |
| 🛡️ Administrator | Student management, attendance management, teams and analytics |

---

## 🎯 Project Objectives

The main objectives of VIT MITRA are:

* Replace manual attendance maintenance with a centralized digital platform.
* Provide secure role-based access for students and administrators.
* Maintain student and team information in an organized system.
* Allow administrators to record and manage daily attendance.
* Provide students with transparent access to their attendance.
* Calculate attendance percentages automatically.
* Provide attendance history and analytics.
* Support team-wise attendance monitoring.
* Identify students who fall below the required attendance threshold.
* Improve accuracy, accessibility and efficiency of club attendance management.

---

# ✨ Key Features

## 👨‍🎓 Student Portal

Students can access their personal attendance information through a dedicated student portal.

### Student features include:

* 🔐 Secure student login
* 📝 Student account creation
* 👤 Student profile
* 📊 Personal attendance percentage
* 📅 Attendance history
* ✅ Present-session tracking
* ❌ Absent-session tracking
* 📈 Attendance status monitoring
* 🏷️ Team information

The live application provides a dedicated Student Portal Login and account creation workflow.

---

## 🛡️ Administrator Portal

Administrators have centralized control over club attendance operations.

### Administrator capabilities include:

* 🔐 Administrator authentication
* 📊 Administrative dashboard
* 👥 Student management
* ➕ Add students
* 🔎 Search students
* 🏷️ Manage teams
* 📅 Create attendance sessions
* ✅ Mark students present
* ❌ Mark students absent
* 💾 Save attendance records
* 📈 Attendance analytics
* 🎯 Attendance threshold monitoring

The deployed interface includes dashboard statistics, student roster management, team management, attendance marking and attendance-threshold controls.

---

# 📊 Attendance Management

The platform provides a structured attendance workflow.

### Attendance workflow

```text
Administrator
      │
      ▼
Select Session Date
      │
      ▼
Enter Session Description
      │
      ▼
Select Team
      │
      ▼
Mark Attendance
      │
      ├── Present
      │
      └── Absent
      │
      ▼
Save Attendance
      │
      ▼
Attendance Records
      │
      ▼
Student Dashboard & Analytics
```

The application supports session date, session description, team filtering, bulk present/absent actions and attendance saving.

---

# 📈 Attendance Analytics

VIT MITRA provides attendance monitoring at both individual and administrative levels.

### Key metrics

* Total students
* Total teams
* Total sessions
* Present sessions
* Absent sessions
* Attendance percentage
* Students below attendance threshold
* Team-wise attendance
* Individual attendance history

The deployed dashboard includes total students, total teams, overall attendance, total sessions and below-threshold monitoring.

---

# 🎯 Attendance Threshold

The system provides an attendance threshold mechanism to identify students who require attention.

The deployed application currently displays a **75% minimum attendance requirement** and identifies students requiring attendance intervention based on their calculated attendance rate.

### Attendance calculation

```text
Attendance Percentage
        =
(Present Sessions / Total Recorded Sessions) × 100
```

---

# 👥 VIT MITRA Teams

The platform supports multiple club tracks/teams.

The current application interface provides **four active tracks** and a dedicated teams directory.

The platform can organize students according to their assigned team and monitor attendance across different tracks.

---

# 🏗️ System Architecture

The application follows a client-server architecture with cloud-based data management.

```text
┌───────────────────────────────────────────┐
│              USER INTERFACE               │
│                                           │
│       React / TypeScript / Vite           │
│                                           │
│  Student Portal     Administrator Portal  │
└───────────────────┬───────────────────────┘
                    │
                    │ HTTPS / API
                    ▼
┌───────────────────────────────────────────┐
│              BACKEND API                  │
│                                           │
│             Python / FastAPI              │
│                                           │
│ Authentication • Attendance • Users      │
│ Teams • Analytics • Notifications        │
└───────────────────┬───────────────────────┘
                    │
                    │ Firebase Admin SDK
                    ▼
┌───────────────────────────────────────────┐
│             CLOUD FIRESTORE               │
│                                           │
│ Students • Attendance • Teams             │
│ Issues • Notifications • Records          │
└───────────────────────────────────────────┘
```

---

# 🧰 Technology Stack

## Frontend

* **React**
* **TypeScript**
* **Vite**
* **Tailwind CSS**
* **React Router**
* **Lucide Icons**

## Backend

* **Python**
* **FastAPI**
* **Uvicorn**
* **REST API**
* **JWT-based authentication**
* **Role-based access control**

## Database & Cloud

* **Firebase**
* **Cloud Firestore**
* **Firebase Admin SDK**

## Development & Deployment

* **Git**
* **GitHub**
* **Antigravity / VS Code**
* **Vercel**
* **Render**

---

# 📁 Project Structure

```text
VIT-MITRA-Attendance-Portal/
│
├── backend/
│   ├── app/
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── firebase.py
│   │   │   └── security.py
│   │   │
│   │   ├── dependencies/
│   │   │   └── auth.py
│   │   │
│   │   ├── routes/
│   │   │   ├── attendance.py
│   │   │   ├── auth.py
│   │   │   ├── dashboard.py
│   │   │   ├── issues.py
│   │   │   ├── notifications.py
│   │   │   └── users.py
│   │   │
│   │   ├── schemas/
│   │   ├── services/
│   │   └── main.py
│   │
│   ├── scripts/
│   ├── requirements.txt
│   └── .env.example
│
├── public/
│   ├── favicon.svg
│   ├── icons.svg
│   └── mitra-logo-circle.svg
│
├── src/
│   ├── assets/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── App.tsx
│   ├── App.css
│   ├── index.css
│   └── main.tsx
│
├── package.json
├── package-lock.json
├── vite.config.ts
├── tailwind.config.js
├── tsconfig.json
├── .gitignore
└── README.md
```

---

# 🔐 Security & Access Control

The application separates access according to user roles.

### Student

```text
Student
   ↓
Student Authentication
   ↓
Student Dashboard
   ↓
Personal Attendance & History
```

### Administrator

```text
Administrator
   ↓
Admin Authentication
   ↓
Admin Dashboard
   ↓
Students • Teams • Attendance • Analytics
```

Sensitive credentials and environment variables should be stored securely through environment configuration and should **never be committed to GitHub**.

---

# 📋 Student Information

The system is designed to maintain structured student information such as:

* Registration Number
* Full Name
* College Email
* Branch
* Year
* Section
* Team
* Phone Number
* Account Status

The deployed application includes an administrator workflow for adding student information using these fields.

---

# 📅 Attendance History

Students can view their recorded attendance history.

The student portal provides:

* Session date
* Session description
* Team context
* Attendance status

This gives students a transparent view of their recorded participation.

---

# ☁️ Cloud Data Management

The application uses **Cloud Firestore** for persistent application data.

The deployed interface includes Firestore status information, allowing the application to indicate its cloud data connection state.

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/rekhaannapurna/VIT-MITRA-Attendance-Portal.git
```

```bash
cd VIT-MITRA-Attendance-Portal
```

---

## 2. Install frontend dependencies

```bash
npm install
```

---

## 3. Configure environment variables

Create the required environment configuration based on:

```text
backend/.env.example
```

Do not commit private credentials, Firebase service-account keys or production secrets to GitHub.

---

## 4. Install backend dependencies

```bash
cd backend
```

```bash
pip install -r requirements.txt
```

---

## 5. Run the backend

```bash
uvicorn app.main:app --reload
```

---

## 6. Run the frontend

From the project root:

```bash
npm run dev
```

Then open the local development URL provided by Vite.

---

# 🌍 Deployment

The project can be deployed using:

### Frontend

**Vercel**

```text
https://vit-mitra-attendance.vercel.app/
```

### Backend

**Render**

The backend can be deployed as a Python/FastAPI web service.

### Database

**Firebase Cloud Firestore**

---

# 🧪 Testing Checklist

Before production use, verify:

* [ ] Student registration
* [ ] Student login
* [ ] Administrator login
* [ ] Authentication and authorization
* [ ] Student profile
* [ ] Student attendance
* [ ] Attendance history
* [ ] Mark Present
* [ ] Mark Absent
* [ ] Save attendance
* [ ] Attendance percentage
* [ ] Team filtering
* [ ] Student search
* [ ] Attendance threshold
* [ ] Dashboard statistics
* [ ] Firestore data persistence
* [ ] Logout
* [ ] Protected routes
* [ ] Production API connection

---

# 🔮 Future Enhancements

Potential future improvements include:

* 📱 Progressive Web App / mobile support
* 📷 QR-based attendance
* 🤖 Face-recognition-based attendance with appropriate institutional and privacy approval
* 📄 Excel/PDF attendance reports
* 📧 Low-attendance notifications
* 📱 WhatsApp/email notifications
* 📝 Multiple attendance sessions per day
* 📊 Advanced analytics
* 🕵️ Audit logs
* ☁️ Automated cloud backups
* 🔔 Real-time notifications

---

# 🎓 Academic Context

**Project:** VIT MITRA Club — Attendance Management & Analytics Platform

**Institution:** Vishnu Institute of Technology, Bhimavaram

**Domain:** Web Application Development • Attendance Management • Analytics • Cloud Computing

**Primary Goal:** Digitize and centralize attendance management for VIT MITRA Club while providing students with transparent access to their attendance information.

---

# 👩‍💻 Project Repository

### GitHub

**[VIT-MITRA-Attendance-Portal](https://github.com/rekhaannapurna/VIT-MITRA-Attendance-Portal)**

### Live Application

**[🚀 VIT MITRA Attendance Portal](https://vit-mitra-attendance.vercel.app/)**

---

# ⭐ Project Highlights

```text
✔ Role-based Student & Admin Access
✔ Centralized Attendance Management
✔ Student Account Registration
✔ Attendance History
✔ Attendance Percentage Calculation
✔ Team-wise Organization
✔ Attendance Threshold Monitoring
✔ Dashboard Analytics
✔ Cloud Firestore Integration
✔ Responsive Web Interface
✔ Production Deployment
```

---

## 📜 License

This project is developed for academic and institutional project purposes.

---

<p align="center">

### 🎓 VIT MITRA CLUB

**Vishnu Institute of Technology**

**Detect • Record • Analyze • Improve**

⭐ If you find this project useful, consider giving the repository a star.

</p>

