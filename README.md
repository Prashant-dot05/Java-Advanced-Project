🏥 Healthcare Patient Monitoring & Management System:

📌 Project Overview:

This project is a JavaFX-based Healthcare Patient Monitoring Dashboard integrated with a MySQL database.
It provides a complete solution for managing patient records, monitoring data, and generating OPD slips in a hospital environment.
The system supports Doctor and Patient roles, enabling secure login, patient data handling, and visualization of patient information.

---

🚀 Features:

🔐 Authentication System
User Registration (Doctor / Patient)
Login validation using MySQL database
Role-based access control

👨‍⚕️ Doctor Dashboard
Add patient details (Name, Age, Disease, Medicine)
Delete patient records
Auto-fill form on row selection
Search patient by name
Patient data visualization (Chart)
Generate OPD Slip automatically

👤 Patient Dashboard
View patient details (Read-only access)
Simple and clean interface

📊 Monitoring & Visualization
Table view of all patients
Bar chart for patient data analysis
Dynamic UI updates

🧾 OPD Slip Generation
Automatically generated after adding patient
Includes:
Patient details
Disease & Medicine
Doctor name
Cabin number

---

🛠️ Technologies Used
Language: Java
UI Framework: JavaFX
Database: MySQL
IDE: IntelliJ IDEA
JDBC: MySQL Connector
---
🗂️ Project Structure
```
src/
│
├── Main.java
├── LoginPage.java
├── RegisterPage.java
├── DoctorDashboard.java
├── PatientDashboard.java
├── OPDSlip.java
│
├── DBConnection.java
├── User.java
├── UserDAO.java
├── Session.java
│
├── Patient.java
├── PatientDAO.java
```

---

🗄️ Database Setup
1️⃣ Create Database
```sql
CREATE DATABASE testdb;
USE testdb;
```
2️⃣ Users Table
```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50),
    password VARCHAR(50),
    role VARCHAR(20),
    cabin VARCHAR(10)
);
```
3️⃣ Patients Table
```sql
CREATE TABLE patients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    disease VARCHAR(100),
    medicine VARCHAR(200)
);
```
---

⚙️ Setup Instructions
Clone or download the project
Open in IntelliJ IDEA
Add JavaFX SDK
Add MySQL Connector JAR
Configure VM options:
```
--module-path "path_to_javafx_lib" --add-modules javafx.controls,javafx.fxml
```
Update database credentials in `DBConnection.java`
Run `Main.java`
---
🧪 Usage Flow
Register as Doctor or Patient
Login using credentials
Doctor can:
Add patient
Generate OPD Slip
View chart & search
Patient can:
View records

---

🎯 Future Enhancements
Real-time health monitoring (BP, Heart Rate)
PDF export for OPD slip
Advanced analytics dashboard
Password encryption (security)
Multi-doctor cabin management

---

📸 Screens (Concept)
Login Page
Register Page
Doctor Dashboard
Patient Dashboard
OPD Slip

---

📄 License
This project is for educational purposes.

---

⭐ Conclusion
This project demonstrates a complete healthcare system combining monitoring and management features, making it suitable for academic submission and real-world understanding.
