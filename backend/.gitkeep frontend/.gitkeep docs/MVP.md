# 🏥 Medical History App — MVP Specification

## 📌 Project Overview

A web-based application that allows patients to securely store and manage their medical history, track appointments, upload medical documents, and communicate with doctors for basic check-ins.


---

## 🎯 MVP Goal

Enable a patient to:

* Create an account and log in securely
* Store and view medical records
* Track appointments
* Upload medical documents
* Send messages to a doctor and receive replies

---

## 👥 User Roles

### 1. Patient

* Register and log in
* Manage personal medical data
* Upload files
* Book/view appointments
* Send messages to doctor

### 2. Doctor

* Log in
* View assigned patient messages
* Reply to messages

---

## ✅ MVP Features

### 🔐 Authentication

* Register (email + password)
* Login
* JWT-based authentication
* Password hashing (bcrypt)

---

### 👤 User Profile

* Basic profile info (name, email)
* Role-based access (Patient / Doctor)

---

### 📋 Medical Records

Patients can:

* Create a medical record
* View all records
* Update records
* Delete records

#### Record Fields:

* Title (e.g. Blood Test)
* Description
* Date

---

### 📅 Appointments

Patients can:

* Create an appointment
* View upcoming appointments

#### Appointment Fields:

* Date
* Doctor (optional for MVP)
* Notes

---

### 📎 File Upload

Patients can:

* Upload medical files (images or PDFs)
* View uploaded files

#### File Types:

* Test results
* Hospital membership card

---

### 💬 Messaging (Basic)

* Patient sends message to doctor
* Doctor replies
* No real-time chat (refresh-based)

#### Message Fields:

* Sender ID
* Receiver ID
* Message content
* Timestamp

---

## ❌ Out of Scope (NOT in MVP)

* AI/ML diagnosis or recommendations
* Real-time chat (WebSockets)
* Notifications (SMS/Push)
* Payment system
* Advanced analytics or charts
* Multi-hospital integrations

---

## 🧱 Core Modules (Backend)

* Auth Module
* Users Module
* Medical Records Module
* Appointments Module
* File Upload Module
* Messaging Module

---

## 📡 API Endpoints (Initial Draft)

### Auth

* POST /auth/register
* POST /auth/login

---

### Users

* GET /users/profile

---

### Medical Records

* GET /records
* POST /records
* PUT /records/:id
* DELETE /records/:id

---

### Appointments

* GET /appointments
* POST /appointments

---

### Files

* POST /files/upload
* GET /files

---

### Messages

* POST /messages
* GET /messages/:userId

---

## 🗄️ Data Models (Simplified)

### User

* id
* email
* password
* role
* created_at

---

### MedicalRecord

* id
* user_id
* title
* description
* date

---

### Appointment

* id
* user_id
* doctor_id
* date
* notes

---

### File

* id
* user_id
* file_url
* type

---

### Message

* id
* sender_id
* receiver_id
* message
* created_at

---

## 🔐 Security Requirements

* Password hashing (bcrypt)
* JWT authentication
* Protected routes
* Input validation (DTOs)

---

## 🛠️ Suggested Tech Stack

### Backend

* Node.js + NestJS
* PostgreSQL or MongoDB
* JWT + bcrypt

### Frontend

* HTML/CSS/JavaScript (or React)

### File Storage

* Cloudinary or AWS S3

### Email (optional)

* Nodemailer

---

## 📂 Project Structure

/project-root
 /backend
 /frontend
 /docs

---

## 📅 Development Plan (MVP)

### Week 1

* Auth system
* Project setup

### Week 2

* Medical records CRUD

### Week 3

* Appointments

### Week 4

* File uploads

### Week 5

* Messaging

---

## 🧪 Testing Strategy

* Backend testing with Postman
* Frontend integration testing
* Weekly team testing sessions

---

## 👥 Team Responsibilities

### Backend

* API development
* Database design
* Authentication & security

### Frontend

* UI implementation
* API integration

### UI/UX

* Figma designs
* User experience flow

---

## 🚀 Success Criteria

The MVP is complete when:

* A user can register and log in
* A patient can create and view medical records
* A patient can upload files
* A patient can create and view appointments
* Messaging between patient and doctor works (basic)

---

## 🔮 Future Enhancements (Post-MVP)

* Real-time chat (WebSockets)
* AI assistant (non-diagnostic)
* Email/SMS reminders
* Data visualization (charts)
* Mobile app version

---

## 📌 Final Note

Focus on building a **simple, secure, and functional system**.
Avoid adding extra features until the MVP is fully complete and stable.

---

]
