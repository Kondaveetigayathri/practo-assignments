Medical Appointments Management Database
This document provides an overview of the medical appointments management database, including the schema, relationships, sample queries, and their explanations.

Database Schema
Tables and Relationships
Users_New

Columns: user_id, name, email, birthdate, phone_number
Description: Stores information about users who can make appointments.
Clinics_New

Columns: clinic_id, name, address, phone_number
Description: Represents clinics where appointments can take place.
Doctors_New

Columns: doctor_id, name, specialty
Description: Contains data on doctors available for appointments.
Doctor_Clinics_New

Columns: doctor_clinic_id, doctor_id, clinic_id
Description: Associates doctors with clinics where they practice.
Foreign Keys: References Doctors_New(doctor_id) and Clinics_New(clinic_id).
Appointments_New

Columns: appointment_id, user_id, doctor_clinic_id, appointment_time, booking_time, status
Description: Tracks scheduled appointments.
Foreign Keys: References Users_New(user_id) and Doctor_Clinics_New(doctor_clinic_id).
ER Diagram
The ER diagram shows the relationships between the tables, depicting how they interact with each other.


SQL Queries and Explanations
