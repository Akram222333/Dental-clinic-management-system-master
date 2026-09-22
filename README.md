# 🦷 Dental Clinic Management System

A web-based management system for dental clinics that handles patient registration, appointment booking, dentist management, and admin operations — built with **PHP** and **MySQL**.

---

## ✨ Features

### 👤 Patient Side
- Register & log in as a patient
- Book appointments by selecting a dental procedure, dentist, date & time
- View available dentists and clinic information
- Browse dental procedure codes and their costs

### 🛠️ Admin Side
- Full dashboard to manage the clinic
- Confirm, cancel, or delete patient appointments
- Add, edit, and remove dentists and staff
- Manage clinic info and available appointment dates
- Manage dental procedure codes and pricing

### 🔐 Role-Based Access
| Role | Access |
|------|--------|
| Patient (user_level = 0) | Booking, viewing dentists & clinic info |
| Admin (user_level = 1) | Full management dashboard |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS |
| Backend | PHP |
| Database | MySQL |
| Server | Apache (XAMPP/WAMP) |

---

## 🗄️ Database Schema

The system uses 7 tables:

| Table | Description |
|---|---|
| `signup` | Patient & admin accounts with role levels |
| `appointement` | Booked appointments with status tracking |
| `dentist` | Dentist profiles and specializations |
| `dentalcode` | Dental procedures with codes and unit costs |
| `clinic` | Clinic name, location, and working hours |
| `staff` | Non-dentist staff records |
| `adminreg` | Admin-controlled available appointment dates |

---

## 🚀 Getting Started

### Prerequisites
- [XAMPP](https://www.apachefriends.org/) or [WAMP](https://www.wampserver.com/) installed
- PHP 5.6+
- MySQL 5.6+

### Installation

1. **Clone or download the project**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Dental-clinic-management-system.git
   ```

2. **Move to your server's root folder**
   - For XAMPP: copy the `dental/` folder to `C:/xampp/htdocs/`
   - For WAMP: copy to `C:/wamp/www/`

3. **Import the database**
   - Open **phpMyAdmin** → `http://localhost/phpmyadmin`
   - Create a new database named `dentalclinic`
   - Import the file: `dentalclinic.sql`

4. **Configure the database connection**

   Open `dental/connect-mysql.php` and update your credentials:
   ```php
   $dbcon = mysqli_connect("localhost", "root", "", "dentalclinic");
   ```

5. **Run the app**

   Open your browser and go to:
   ```
   http://localhost/dental/index.html
   ```

---

## 👤 Default Admin Login

| Field | Value |
|---|---|
| Email | `sumitnarang76@gmail.com` |
| Password | `sumit` |

> ⚠️ Change the admin credentials after your first login.

---

## 📂 Project Structure

```
dental/
├── index.html              # Landing page
├── login.php               # Login & session handler
├── signup.php              # Patient registration
├── admin.php               # Admin dashboard
├── appointement.php        # Book an appointment
├── confirmappoint.php      # Admin confirms appointments
├── dentist.php             # Dentist listing (admin)
├── dentistuser.php         # Dentist listing (patient view)
├── clinic.php              # Clinic info (admin)
├── clinicinfo.php          # Clinic info (patient view)
├── dentalcodes.php         # Manage dental codes (admin)
├── staff.php               # Staff management
├── connect-mysql.php       # Database connection
└── dentalclinic.sql        # Full database dump
```

---

## ⚠️ Known Limitations

- Passwords are stored in **plain text** — not suitable for production use
- Some files mix deprecated `mysql_*` functions with `mysqli_*`
- No input sanitization against SQL injection in all files
- Recommended for learning/demo purposes only

---

## 🔮 Possible Improvements

- [ ] Password hashing (bcrypt)
- [ ] Full migration to `mysqli_*` or PDO
- [ ] Patient appointment history view
- [ ] Email notifications on appointment confirmation
- [ ] Responsive mobile design

---

## 👤 Author

**Akram Muhammad Ali**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akram-el-metwally-04896333a)
