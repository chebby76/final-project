Run
Copy code
# Clinic Booking System

## Project Overview

The Clinic Booking System is a comprehensive database designed to manage healthcare operations including patient registration, doctor management, appointment scheduling, clinic services, and medical record keeping. This system supports multiple clinics, doctors with specializations, appointment services, and patient insurance details, delivering a robust solution for efficient clinic management.

## Features

- **Patient Management:** Store and manage patient demographic details, medical history, and insurance information.
- **Doctor Management:** Maintain doctor profiles, including multiple specializations.
- **Clinic Services:** Define and manage services offered by clinics.
- **Appointment Scheduling:** Schedule appointments linking patients, doctors, services, and available schedule slots.
- **Detailed Relationships:** Support many-to-many relationships such as doctors to specializations and appointments to services.
- **Data Integrity:** Enforce robust constraints with primary and foreign keys to maintain data consistency.

## Database Schema

The system includes the following main tables:

- `Patients`
- `Clinics`
- `Doctors`
- `Doctor_Specializations` (many-to-many)
- `Specializations`
- `Services`
- `Clinic_Services` (many-to-many)
- `Appointments`
- `Appointment_Services` (many-to-many)
- `Medical_History`
- `Insurance`
- `Doctor_Schedules`

## Technologies Used

- MySQL (Relational Database Management System)
- SQL for schema creation and data operations

## Getting Started

### Prerequisites

- MySQL installed and running
- Access to MySQL client or workbench for running SQL scripts

### Installation

1. Clone this repository or copy the SQL script file.
2. Open your MySQL client.
3. Create a new database for the project, e.g.,
   ```sql
   CREATE DATABASE ClinicBookingSystem;
   USE ClinicBookingSystem;
Run the provided SQL script to create tables and constraints.
(Optional) Insert sample data to start testing the system.
Usage
Use standard SQL queries to manage patients, doctors, appointments, services, and more.
Employ JOINs as needed to fetch comprehensive information across related tables.
Example Query
Fetch upcoming appointments for a specific doctor:

sql
Run
Copy code
SELECT a.appointment_id, p.first_name, p.last_name, a.appointment_date, a.start_time, a.end_time
FROM Appointments a
JOIN Patients p ON a.patient_id = p.patient_id
WHERE a.doctor_id = 1 AND a.status = 'scheduled' AND a.appointment_date >= CURDATE()
ORDER BY a.appointment_date, a.start_time;
Contributing
Contributions are welcome! Feel free to fork the project and submit pull requests for enhancements or bug fixes.
## Entity-Relationship Diagram (ERD)

Below is the ERD illustrating the database schema and relationships for the Clinic Booking System:

![ERD Diagram](## Entity-Relationship Diagram (ERD)

Below is the ERD illustrating the database schema and relationships for the Clinic Booking System:

![Image](https://github.com/user-attachments/assets/7be4d903-c349-46d2-b853-4bde91c3d2b7)
Contact
For queries, please contact:

VIVIAN CHEBII
Email: vchebby876@gmail.com
GitHub: chebby76
Run


---


