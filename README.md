# 🏥 MediSiBridge – Smart Hospital Management System

MediSiBridge is a **comprehensive hospital management system** that bridges the gap between **patients** and **doctors** through a seamless, secure, and efficient digital platform.  
It simplifies appointment scheduling, doctor availability, prescription tracking, and patient management — all in one unified dashboard.

---

## 🚀 Project Overview

MediSiBridge was designed to digitize the hospital workflow — from patient registrations and appointments to doctor consultations and prescription management.

It provides two main interfaces:
- 👨‍⚕️ **Doctor Dashboard:** Manage appointments, set availability, update patient records, and issue prescriptions.
- 🧍‍♀️ **Patient Dashboard:** Book appointments, view available doctors, manage health history, and track prescriptions.

The system ensures **data integrity**, **security**, and **real-time synchronization** between patients and doctors.

---

## 🧩 Key Features

### 👨‍⚕️ Doctor Features
- **Secure Authentication** – JWT-based login and signup for doctors.  
- **Set Availability** – Doctors can define time slots for patient consultations.  
- **Manage Appointments** – View, confirm, cancel, or mark appointments as completed.  
- **View Patients** – Access patient profiles and medical histories.  
- **Issue Prescriptions** – Create, save, and manage digital prescriptions for patients.

### 🧍 Patient Features
- **Easy Signup & Login** – Patients can register securely and access their personal dashboard.  
- **Doctor Discovery** – Search doctors by specialization and availability.  
- **Book Appointments** – Schedule appointments in available time slots.  
- **View Prescription History** – Access all prescriptions issued by doctors.  
- **Health Record Management** – Maintain and update medical history (BMI, allergies, etc.).

### 🏥 Admin Features (optional enhancement)
- **Monitor Doctor and Patient Activities**  
- **Manage Hospital Database**  
- **Analyze Appointment Statistics**

---

## ⚙️ Tech Stack

| Layer | Technologies Used |
|-------|--------------------|
| **Frontend** | React.js / Next.js, TypeScript, Tailwind CSS, Shadcn UI |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (Mongoose ODM) |
| **Authentication** | JSON Web Token (JWT) |
| **State Management** | React Context API |
| **Deployment** | Vercel (Frontend) • Render / Railway (Backend) • MongoDB Atlas (Cloud DB) |

---

---

## 🔐 Authentication Flow

1. **Doctor or Patient** signs up → credentials stored securely (hashed password).  
2. On login → **JWT** token issued.  
3. Each request to protected routes (e.g., `/doctor/appointments`) includes a `Bearer <token>` header.  
4. Middleware verifies token and grants access.

---

## 📡 API Overview (Sample)

### 🔹 Doctor Routes
| Endpoint | Method | Description |
|-----------|---------|-------------|
| `/doctor/signup` | POST | Doctor registration |
| `/doctor/login` | POST | Doctor login |
| `/doctor/set-availability` | POST | Set consultation slots |
| `/doctor/appointments` | GET | Get doctor’s appointments |
| `/doctor/appointments/:id/status` | PUT | Update appointment status |
| `/doctor/patients` | GET | Get list of patients |
| `/doctor/getDoctorSlots/:doctorId` | GET | Get available slots for doctor |

### 🔹 Patient Routes
| Endpoint | Method | Description |
|-----------|---------|-------------|
| `/patient/signup` | POST | Register a new patient |
| `/patient/login` | POST | Patient login |
| `/patient/book-appointment` | POST | Book an appointment |
| `/patient/getAppointments` | GET | View appointments |
| `/patient/getPrescriptions` | GET | View prescriptions |

---

## 🧪 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/MediSiBridge.git
cd MediSiBridge
