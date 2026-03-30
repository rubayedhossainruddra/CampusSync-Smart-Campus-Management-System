# CampusSync Smart Campus Management System - APU

CampusSync is a comprehensive Campus Management System designed for School/College. It provides separate interfaces for Administrators, Lecturers, and Students to manage campus activities, timetables, announcements, bookings, and more.

---

## Features

- **Admin Panel**: Manage users, courses, intakes, departments, classrooms, Bookings, announcements, and timetables
- **Lecturer Portal**: View timetable, announcements, manage attendance, and room bookings
- **Student Portal**: View timetable, announcements, attendance records, and book facilities
- **Authentication**: Secure login with OTP-based password reset
- **Campus Navigation**: Interactive campus map and room navigation

---

## Prerequisites

- XAMPP (with Apache and MySQL modules)
- PHP 7.4 or higher
- Web browser (Chrome, Firefox, Edge)

---

## Installation Guide (XAMPP)

### Step 1: Install XAMPP

1. Download XAMPP from [apachefriends.org](https://www.apachefriends.org/)
2. Install XAMPP with default settings
3. Start **Apache** and **MySQL** services from XAMPP Control Panel


### STEP 2: SETUP DATABASE (XAMPP - phpMyAdmin)

Follow these instructions carefully to create and configure the database
for CampusSync CMS.

  --------------------------------------------------
  METHOD 1: IMPORT DATABASE.SQL FILE (Recommended)
  --------------------------------------------------

1.  Open your web browser.
2.  Go to phpMyAdmin: http://localhost/phpmyadmin
3.  In phpMyAdmin, click the “New” button from the left sidebar.
4.  Enter the database name: campus_sync
5.  Set Collation to: utf8mb4_general_ci
6.  Click the “Create” button.
7.  After creating, click the database name “campus_sync” from the left
    panel.
8.  Click the “Import” tab at the top.
9.  Click the “Choose File” button.
10. Select the file: database.sql (located inside the campussync-cms
    project folder)
11. Scroll down and click the “Import” button.
12. Wait until you see the success message: “Import has been
    successfully finished.”

  ---------------------------------------
  METHOD 2: COPY AND PASTE SQL MANUALLY
  ---------------------------------------

Use this method if import does not work.

1.  Open phpMyAdmin: http://localhost/phpmyadmin
2.  Click “New”
3.  Create database: campus_sync
4.  Click “Create”
5.  Click the “campus_sync” database from the left panel.
6.  Click the “SQL” tab.
7.  Open the file: campus_sync.sql using Notepad, VS Code, or any text
    editor.
8.  Select ALL contents: Press CTRL + A Then CTRL + C
9.  Go back to phpMyAdmin SQL tab.
10. Paste the SQL: Press CTRL + V
11. Click the “Go” button.
12. Wait until phpMyAdmin shows success message.
Your database is now fully configured.


### Step 3: Configure Project

1. Ensure the project folder is placed in the correct location:
   ```
   C:\xampp\htdocs\campussync-cms-apu
   ```

2. The database configuration in `config.php` is pre-configured for XAMPP:
   - **DB Host**: `localhost`
   - **DB User**: `root`
   - **DB Password**: (empty)
   - **DB Name**: `campus_sync`

### Step 4: Access the Application

#### User Login (Students & Lecturers)
```
http://localhost/campussync-cms-apu/index.php
```

#### Admin Login
```
http://localhost/campussync-cms-apu/Admin/login.php
```

---

## Default Admin Credentials

| Field | Value |
|-------|-------|
| **Username** | Admin |
| **Password** | password |

> **Important**: For security reasons, change the default admin password after first login.

---

## User Roles

- **Admin**: Full access to all features and settings
- **Lecturer**: Manage timetable, attendance, announcements, and room bookings
- **Student**: View timetable, attendance, announcements, and book facilities

---

## Project Structure

```
campussync-cms-apu/
├── Admin/                  # Admin panel files
│   ├── login.php          # Admin login
│   ├── dashboard.php      # Admin dashboard
│   ├── users.php          # User management
│   ├── courses.php        # Course management
│   ├── intakes.php        # Intake management
│   ├── departments.php    # Department management
│   ├── classrooms.php     # Classroom management
│   ├── facilities.php     # Facility management
│   ├── announcements.php  # Announcement management
│   ├── timetable.php      # Timetable management
│   └── profile.php        # Admin profile
├── student/               # Student portal files
├── lecturer/              # Lecturer portal files
├── navbar/                # Shared navigation components
├── IMG/                   # Images and assets
├── PHPMailer-master/      # Email library
├── campus_sync.sql        # Database schema
├── config.php             # Configuration file
└── index.php              # Main entry point (User login)
```

---

## Troubleshooting

### Issue: Cannot connect to database
- Ensure MySQL service is running in XAMPP
- Verify database name is `campus_sync`
- Check credentials in `config.php`

### Issue: Page not found (404)
- Ensure project is in `C:\xampp\htdocs\campussync-cms-apu`
- Restart Apache in XAMPP

### Issue: Email/OTP not working
- Email is configured for production SMTP
- In XAMPP testing mode, OTP will be displayed on screen

---

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: PHP
- **Database**: MySQL
- **Email**: PHPMailer

---

## License

This project is developed for Capstone Project educational purposes at Asia Pacific University of Technology and Innovation (APU/APIIT).
