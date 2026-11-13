# 🩸 Sweety – Blood Glucose Tracker

**A Smart and Simple Blood Glucose Monitoring Platform**

Sweety is a web-based blood glucose tracking application designed to help individuals record, monitor, and understand their blood glucose levels. It provides a patient dashboard for managing glucose readings and a doctor dashboard for viewing assigned patients.

The application helps users maintain their glucose history, track trends through visual analytics, and generate reports for better health monitoring.

---

## ✨ Key Features

### 👤 Patient Dashboard
- Patient registration and secure login.
- Record daily blood glucose readings.
- Add, edit, and delete glucose entries.
- View previous glucose readings in a history table.
- Track glucose trends using interactive charts.
- View 7-day and 30-day glucose analytics.
- Generate daily, month-to-date, and previous-month reports.
- Download reports as PDF files.

### 🩺 Doctor Dashboard
- Dedicated doctor login.
- Doctor registration with a secure setup key.
- View assigned patient lists.
- Access individual patient glucose readings.
- View patient reports and glucose history.

### 📊 Data Visualization and Reports
- Interactive glucose trend charts.
- Daily glucose statistics.
- Minimum, maximum, and average glucose values.
- Monthly glucose summaries.
- PDF report generation.

### 🔐 Security
- Password hashing using bcrypt.
- JWT-based authentication.
- Role-based access for patients and doctors.
- Protected API endpoints.
- Environment variables for sensitive configuration.

---

## 🛠️ Technologies Used

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite |
| Styling | CSS |
| Backend | Node.js, Express.js |
| Database | Neon PostgreSQL |
| API Communication | Axios, REST API |
| Authentication | JWT, bcrypt |
| Charts | Recharts |
| PDF Generation | jsPDF |
| Development Tools | VS Code, Thunder Client, Git, GitHub |

---

## 🏗️ Project Architecture

Sweety follows a client-server architecture.

```text
Sweety-Blood-Glucose-Tracker/
│
├── client/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── main.jsx
│   ├── package.json
│   └── index.html
│
├── server/
│   ├── src/
│   │   ├── app.js
│   │   ├── server.js
│   │   └── db.js
│   ├── package.json
│   └── .env
│
├── .gitignore
└── README.md
```

---

## ⚙️ Installation and Setup

### Prerequisites

Make sure you have installed:

- Node.js and npm
- Git
- A Neon PostgreSQL account
- Visual Studio Code (recommended)

### 1. Clone the Repository

```bash
git clone https://github.com/nishanth312005/Sweety-Blood-Glucose-Tracker
```

```bash
cd sweety-blood-glucose-tracker
```

### 2. Setup the Backend

```bash
cd server
npm install
```

Create a `.env` file inside the `server` folder:

```env
PORT=5000

DATABASE_URL=YOUR_NEON_DATABASE_URL

JWT_SECRET=YOUR_PRIVATE_JWT_SECRET

DOCTOR_SETUP_KEY=YOUR_PRIVATE_DOCTOR_SETUP_KEY

ADMIN_SETUP_KEY=YOUR_PRIVATE_ADMIN_SETUP_KEY
```

**Important:** Replace the placeholder values with your own credentials. Never upload your `.env` file or expose database passwords and secret keys on GitHub.

Start the backend:

```bash
npm run dev
```

Backend URL:

```text
http://localhost:5000
```

### 3. Setup the Frontend

Open another terminal:

```bash
cd client
npm install
```

Start the frontend:

```bash
npm run dev
```

Frontend URL:

```text
http://localhost:5173
```

---

## 🔗 API Endpoints

The backend provides REST APIs for authentication, glucose readings, reports, and doctor-patient management.

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a patient |
| POST | `/api/auth/login` | User login |
| POST | `/api/auth/register-doctor` | Register a doctor |
| GET | `/api/readings` | Retrieve patient readings |
| POST | `/api/readings` | Add a glucose reading |
| PUT | `/api/readings/:id` | Update a reading |
| DELETE | `/api/readings/:id` | Delete a reading |
| GET | `/api/reports` | Retrieve patient reports |
| GET | `/api/doctor/patients` | View assigned patients |
| GET | `/api/doctor/patients/:patientId/readings` | View patient readings |
| GET | `/api/doctor/patients/:patientId/reports` | View patient reports |
| POST | `/api/admin/assign-patient` | Assign a patient to a doctor |
| GET | `/api/health` | Check backend health |

Protected endpoints require a valid JWT authentication token.

---

## 🗄️ Database

Sweety uses **Neon PostgreSQL**, a cloud-hosted PostgreSQL database.

Main database tables:

- **users** – Stores patient and doctor account information.
- **readings** – Stores blood glucose readings, dates, and time slots.
- **doctor_patient_assignments** – Maintains relationships between doctors and their assigned patients.

---

## 📸 Application Modules

The application includes the following modules:

1. Patient Registration and Login
2. Patient Dashboard
3. Blood Glucose Entry Management
4. Glucose History
5. Analytics and Visualization
6. Daily and Monthly Reports
7. PDF Report Download
8. Doctor Registration and Login
9. Doctor Dashboard
10. Patient Assignment and Monitoring




---
<img width="1222" height="887" alt="Screenshot 2026-11-13 215035" src="https://github.com/user-attachments/assets/a6eca75b-cbfb-4a4e-b6ec-22ac1fc11780" />
<img width="1212" height="892" alt="Screenshot 2026-11-13 215141" src="https://github.com/user-attachments/assets/ff15e68b-f072-43b7-8a20-7e06681b9cc0" />
<img width="1201" height="893" alt="Screenshot 2026-11-13 215303" src="https://github.com/user-attachments/assets/bace7bfd-f170-4581-aac6-02fa3a4c1012" />
<img width="1217" height="861" alt="Screenshot 2026-11-13 215320" src="https://github.com/user-attachments/assets/b0112c92-8afb-4a38-b53d-65d17f8180f6" />

## 🎯 Project Objectives

- Simplify daily blood glucose recording.
- Help patients maintain an organized glucose history.
- Provide meaningful visual insights into glucose trends.
- Enable doctors to monitor their assigned patients.
- Make glucose reports easy to access and share.

---

## 🚀 Future Enhancements

- Automated glucose monitoring device integration.
- Email and SMS reminders.
- Personalized health insights.
- AI-powered glucose trend analysis.
- Medication and appointment reminders.
- Secure report sharing between patients and healthcare professionals.

---

## ⚠️ Disclaimer

Sweety is an educational and health-monitoring project. It is not intended to replace professional medical advice, diagnosis, or treatment. Users should consult qualified healthcare professionals for medical decisions.

---

## 👩‍💻 Developed By

**Nishanth M**

M.Sc. Software Systems  
KG College of Arts and Science
m.nishanthmanian@gmail.com

**Project:** Sweety – Blood Glucose Tracker

---

⭐ If you find this project interesting, consider giving the repository a star!
