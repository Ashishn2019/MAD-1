# Placement Portal Application  
**MAD-1 Project – IIT Madras BS Degree Program**

---

## 📖 Project Overview

The **Placement Portal Application** is a role-based web application developed to simplify and manage campus recruitment processes.

It enables structured interaction between three main stakeholders:

- **Admin (Institute Placement Cell)**
- **Companies**
- **Students**

The system replaces traditional spreadsheet-based placement tracking with a **centralized database-driven platform**.

---

## 🎯 Objectives

- Manage company registration requests and approvals
- Handle creation and approval of placement drives
- Allow students to apply for approved drives
- Prevent duplicate student applications
- Maintain complete placement records
- Provide admin-level monitoring and management
- Enforce role-based access control

---

## 🛠️ Tech Stack (As Per MAD-1 Requirements)

| Component | Technology |
|-----------|------------|
| Backend | Flask |
| Frontend | Jinja2, HTML, CSS, Bootstrap |
| Database | SQLite (Programmatically created) |
| Authentication | Flask-Login |
| ORM | Flask-SQLAlchemy |

⚠️ No manual database creation used  
⚠️ No JavaScript used for core functionality

---

## 👥 User Roles & Functionalities

### 1️⃣ Admin (Institute Placement Cell)

- Pre-created superuser account
- Access dashboard statistics
- Approve / reject company registrations
- Approve / reject placement drives
- View all students, companies, drives, and applications
- Blacklist or reactivate accounts
- Search students and companies
- Monitor complete placement activity

---

### 2️⃣ Company

- Register and wait for admin approval
- Manage company profile
- Create placement drives (requires approval)
- View applicants for drives
- Shortlist, select, or reject candidates
- Close placement drives

---

### 3️⃣ Student

- Register and login
- Update profile and upload resume
- View approved placement drives
- Apply for placement drives
- Track application status
- View personal placement history

---

## 🔒 Core System Rules Implemented

- Only **approved companies** can create placement drives
- Only **approved drives** are visible to students
- Duplicate applications prevented using **database constraints**
- Application **deadline validation** enforced
- **Blacklisted users cannot access the system**
- Complete **application history maintained**
- **Role-based route protection** implemented

---

## 🗄️ Database Design

### Main Tables

- User
- Student
- Company
- PlacementDrive
- Application

### Relationships

- One **User → One Student / Company**
- One **Company → Many Placement Drives**
- One **Student → Many Applications**
- One **Drive → Many Applications**

### Unique Constraint

Prevents a student from applying **multiple times for the same drive**.

---

## ▶️ How to Run the Project Locally

### 1. Clone Repository

```bash
git clone <https://github.com/Ashishn2019/MAD-1>
cd MAD-1
```

### 2. Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Application

```bash
python app.py
```

Open in browser:

```
http://127.0.0.1:5000
```

---

## 🔑 Default Admin Credentials

**Username:** admin  
**Password:** admin123  

---

## 📊 Key Features Demonstrated

- Role-based authentication
- Dynamic dashboards
- Approval workflow
- Application lifecycle management
- Resume upload functionality
- Blacklist enforcement
- Clean Bootstrap-based UI

---

## 📹 Demo

Video demonstration link will be added in the **project report**.

---

## 📄 Academic Note

This project was developed strictly according to **MAD-1 project guidelines**:

- SQLite database only
- Programmatic database creation
- Local execution
- Role-based access control
- Bootstrap UI
- No JavaScript used for core logic