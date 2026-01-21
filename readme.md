# 🏥 Hospital Management System

A full-stack web application for managing hospital operations including patient registration, doctor appointments, and administrative functions. Built with React.js frontend and Spring Boot backend.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)5
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Contributing](#contributing)

## 🎯 Overview

This Hospital Management System is a web-based application designed to digitize and streamline hospital operations. The system provides separate interfaces for patients, doctors, and administrators to manage appointments, medical records, and hospital resources efficiently.

## ✨ Features

### Patient Module
- **User Registration & Login** - Secure authentication system for patients
- **Book Appointments** - Schedule appointments with available doctors
- **View Appointments** - Check appointment history and status
- **Profile Management** - Update personal and medical information

### Doctor Module
- **Doctor Login** - Secure access for medical staff
- **View Appointments** - See scheduled patient appointments
- **Patient Records** - Access patient medical history
- **Appointment Management** - Approve or reschedule appointments

### Admin Module
- **Admin Dashboard** - Overview of hospital operations
- **Manage Doctors** - Add, update, or remove doctor profiles
- **Manage Patients** - View and manage patient records
- **Appointment Oversight** - Monitor all hospital appointments
- **Department Management** - Organize hospital departments

## 🛠️ Tech Stack

### Frontend
- **React.js** - UI library for building user interfaces
- **JavaScript** - Programming language
- **CSS3** - Styling and layout
- **Axios** - HTTP client for API requests
- **React Router** - Client-side routing

### Backend
- **Spring Boot** - Java framework for backend
- **Spring Data JPA** - Database operations
- **MySQL** - Relational database
- **Maven** - Dependency management
- **JWT** - Authentication and authorization

## 📥 Installation

### Prerequisites
- Node.js (v14 or higher)
- Java JDK 11 or higher
- Maven
- MySQL Server

### Backend Setup

1. **Clone the repository**
```bash
git clone https://github.com/gurmetejas-collab/Hospital-Management-System.git
cd Hospital-Management-System/hospital-management-system
```

2. **Configure MySQL Database**

Create a database in MySQL:
```sql
CREATE DATABASE hospital_db;
```

3. **Update application.properties**

Edit `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/hospital_db
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

4. **Run the backend**
```bash
mvn clean install
mvn spring-boot:run
```

Backend will start on `http://localhost:8080`

### Frontend Setup

1. **Navigate to frontend directory**
```bash
cd ../hms-frontend
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure API URL**

Create `.env` file:
```env
REACT_APP_API_URL=http://localhost:8080
```

4. **Start the frontend**
```bash
npm start
```

Frontend will open on `http://localhost:3000`

## 🚀 Usage

### For Patients
1. Register a new account from the registration page
2. Login with your credentials
3. Book an appointment by selecting a doctor
4. View your appointment history and status

### For Doctors
1. Login with doctor credentials
2. View scheduled appointments
3. Check patient details and medical history
4. Update appointment status

### For Admin
1. Login with admin credentials
2. Manage doctors and patients
3. Monitor all appointments
4. Manage hospital departments

## 📁 Project Structure

```
Hospital-Management-System/
│
├── hms-frontend/                 # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/          # React components
│   │   ├── pages/               # Page components
│   │   ├── services/            # API services
│   │   └── App.js
│   └── package.json
│
├── hospital-management-system/   # Spring Boot Backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/hospital/
│   │   │   │       ├── controller/    # REST Controllers
│   │   │   │       ├── service/       # Business Logic
│   │   │   │       ├── repository/    # Database Layer
│   │   │   │       └── model/         # Entity Classes
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/
│   └── pom.xml
│
└── README.md
```

## 📸 Screenshots

> Add screenshots of your application here when available

### Login Page
![Login Page](screenshots/login.png)

### Dashboard
![Dashboard](screenshots/dashboard.png)

### Appointment Booking
![Appointments](screenshots/appointments.png)

## 🔐 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

### Appointments
- `POST /api/appointments` - Book appointment
- `GET /api/appointments` - Get all appointments
- `GET /api/appointments/{id}` - Get appointment by ID
- `PUT /api/appointments/{id}` - Update appointment

### Doctors
- `GET /api/doctors` - Get all doctors
- `POST /api/doctors` - Add new doctor (Admin)
- `GET /api/doctors/{id}` - Get doctor details

### Patients
- `GET /api/patients` - Get all patients
- `GET /api/patients/{id}` - Get patient details
- `PUT /api/patients/{id}` - Update patient info

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

**Gurme Tejas**

- GitHub: [@gurmetejas-collab](https://github.com/gurmetejas)
- Repository: [Hospital-Management-System](https://github.com/gurmetejas-collab/Hospital-Management-System)

## 🙏 Acknowledgments

- Spring Boot Documentation
- React.js Community
- MySQL Database

---

⭐ If you found this project helpful, please give it a star!

**Made with ❤️ by Gurme Tejas**