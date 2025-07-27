📚 AcademIQ – Educational Institution Management Web App
AcademIQ is a role-based educational web application designed to help institutions like schools, colleges, or coaching centers efficiently manage academic operations. Built using pure PHP, MySQL, and HTML/CSS/JS, it offers separate login and dashboard experiences for admins and students.

🧩 Key Modules and Workflow
🔑 1. Authentication System
Login Pages for Admin & Student

Users authenticate via login forms.

Credentials are verified using PHP sessions and MySQL queries.

Upon login, users are redirected to their respective dashboards.

🧑‍💼 2. Admin Dashboard
Once the admin logs in, they can:

✅ View & manage student records

Add new student entries

Edit or delete existing ones

📊 Dashboard Overview

Quick stats on number of students or courses

🧱 Modular structure

Admin functionalities are split across multiple PHP pages (e.g., manage-students.php, add-class.php, etc.)

Uses common includes: header.php, footer.php, sidebar.php

👨‍🎓 3. Student Dashboard
Once logged in, students can:

🗂 Access their profile

View their academic details (name, course, ID, etc.)

📌 Track updates

Notifications or messages (static for now, but extendable)

👁 User Interface

Clean, responsive layout

Shared styling with admin for consistency

🛠 4. Includes and Reusability
includes/header.php, sidebar.php, and footer.php are reused across all pages

dbconnection.php handles MySQL connections

Ensures DRY (Don't Repeat Yourself) coding principles

🖼️ 5. Static Assets
Located inside assets/

CSS/, JS/, images/, SCSS/, and vendor/ folders

Uses Bootstrap-like structure for responsiveness and UI components

SCSS files can be compiled manually if modified

🧪 Database Integration
📂 File: database/eduauth.sql
Contains schema for:

Admin and student tables

Seed data for testing

Must be imported into MySQL before using the system

📁 File: dbconnection.php
Connects to MySQL using mysqli_connect()

Requires setting DB host, username, password, and DB name

🧰 How the Website Works (Behind the Scenes)
User visits site → Lands on login page (index.php)

Login form submission → Validated with PHP + MySQL query

Session is created → Stores user info for authenticated access

Redirected to dashboard → Depending on role (admin/student)

Each dashboard loads pages via PHP includes (e.g., sidebar, header)

Admin pages interact with database to perform CRUD (Create, Read, Update, Delete) operations

Assets like CSS/JS are loaded from relative paths to style and enhance UX

🌟 Unique Selling Points
✅ Built from scratch – No frameworks

🔐 Basic but functional login system

🔄 Reusable structure using includes

🧩 Easily extendable – Add modules like attendance, grading, etc.

🎯 Perfect for learning core web development principles
