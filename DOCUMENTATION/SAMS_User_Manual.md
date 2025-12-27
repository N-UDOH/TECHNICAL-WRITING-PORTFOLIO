# 📘 Technical Documentation: Smart Attendance Management System

**Author:** N.A Udoh
**Date:** December 2025
**System Version:** 1.0.2 (PWA Enabled)

---

## 1. Executive Summary
The **Smart Attendance Management System (SAMS)** is a web-based mobile solution designed to digitize and secure the academic attendance process. By integrating **Geolocation (GPS)** and **Artificial Intelligence (Facial Recognition)**, the system mitigates common academic integrity issues such as proxy attendance. This document serves as the official user manual and technical reference for administrators and end-users.

## 2. System Architecture
The application operates on a **Client-Server Architecture**:
* **The Client (Frontend):** A Progressive Web App (PWA) that leverages the device's native hardware (Camera & GPS) via the browser.
* **The Server (Backend):** A Python FastAPI engine that processes biometric data and validates geolocation coordinates against active session parameters.

## 3. Core Features & Capabilities

### 3.1. The "Invisible Wall" (Geofencing)
The system employs dynamic geofencing. When a lecturer initiates a class, the system captures their precise coordinates. A "valid zone" (radius of 50 meters) is established instantly. Any attendance request originating outside this zone is automatically rejected by the server, regardless of biometric validity.

### 3.2. AI-Driven Verification
Instead of a binary (Pass/Fail) check, the system utilizes a confidence scoring algorithm. It compares the live image input against the student's stored biometric profile to generate a **Confidence Score**.
* **>80% Score:** Marked as "High Confidence" (Green).
* **<50% Score:** Flagged for review.

### 3.3. Offline-First Mobile Experience
Built as a PWA, the application offers an "App-like" experience:
* Full-screen immersive mode (No browser URL bars).
* Home Screen installation support for Android and iOS.
* Low-bandwidth optimization for campus networks.

---

## 4. User Guide

### 🧑‍🏫 4.1. For Lecturers
**Objective:** Create a secure class session.
1.  **Log In:** Access the portal using valid staff credentials.
2.  **Initiate Session:** Navigate to the dashboard. Enter the *Course Code* (e.g., CSC 201) and *Topic*.
3.  **GPS Lock:** Click **"Get GPS & Start"**. *Note: You must be physically present in the classroom.*
4.  **Broadcast Code:** The system generates a unique 4-digit token (e.g., `4829`). Display this code to students.
5.  **Reports:** At the end of the semester, click **"View & Download PDF Reports"** to archive records.

### 🧑‍🎓 4.2. For Students
**Objective:** Mark attendance verified by location and face.
1.  **Log In:** Access the portal using Matric Number.
2.  **Input Token:** Enter the 4-digit code provided by the lecturer.
3.  **Biometric Scan:** Allow camera permissions. Align face within the frame and tap **"Snap & Mark Present"**.
4.  **Verification:** Wait for the "Success" confirmation message.

### 🛡️ 4.3. For Administrators
**Objective:** Manage users and system integrity.
1.  **User Management:** Create official accounts for Lecturers to prevent unauthorized session creation.
2.  **System Reset:** Assist students with password resets via the "Create User" panel.
3.  **Global Reporting:** Access university-wide attendance data for auditing purposes.

---

## 5. Troubleshooting

| Error Message | Cause | Resolution |
| :--- | :--- | :--- |
| **"GPS Not Supported"** | Device location is off. | Enable GPS in phone settings and allow browser permissions. |
| **"You are too far!"** | Student is outside the 50m radius. | Move inside the lecture hall and retry. |
| **"Face Not Match"** | Poor lighting or wrong person. | Move to a well-lit area and remove face coverings. |

---

---
---
### 👨‍💻 Developed By
**N.A Udoh**<br>
Lead AI Developer<br>
Aifiok Business & Tech Solutions. RC:8097734<br>
Nigeria<br>
© 2025 All Rights Reserved.