# 🎓 ECUSTA Online Exam System

A modern, web-based online examination platform built with PHP and MySQL. Designed for educational institutions to manage quizzes, students, and teachers through a clean, role-based dashboard system.

![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-5.7+-4479A1?logo=mysql&logoColor=white)
![License](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey)

---

## ✨ Features

### 👨‍🎓 Student Portal
- Sign in / Sign up with a modern glassmorphism interface
- Browse and take multiple-choice exams
- View results immediately after submission
- Track exam history and overall rankings

### 👩‍🏫 Teacher Dashboard
- Create quizzes with custom time limits, marks, and penalties
- Add multiple-choice questions with 4 options each
- View student scores for your quizzes
- Remove quizzes you've created

### 🛡️ Admin Dashboard
- **System overview** with live stats (students, quizzes, teachers, feedback)
- **Full quiz management** — create, add questions, and remove any quiz
- **User management** — view all students, add new students, remove accounts
- **Teacher management** — add/remove teacher accounts
- **Feedback inbox** — read and manage student feedback
- **Rankings** — view the overall student leaderboard

---

## 🛠️ Installation

### Prerequisites
- [XAMPP](https://www.apachefriends.org/) or [WAMP](https://www.wampserver.com/) (Apache + PHP + MySQL)
- phpMyAdmin (included with XAMPP/WAMP)

### Steps

1. **Clone or copy** the project into your web server directory:
   ```bash
   # For XAMPP
   cp -r Online-exam-system /opt/lampp/htdocs/

   # For WAMP
   cp -r Online-exam-system C:/wamp64/www/
   ```

2. **Create the database:**
   - Open [phpMyAdmin](http://localhost/phpmyadmin)
   - Create a new database named **`project1`**
   - Import the file `database/project1.sql`

3. **Configure the database connection** (if needed):
   - Edit `config/dbConnection.php` with your credentials
   - Defaults: host=`localhost`, user=`root`, password=`""`, database=`project1`

4. **Open in your browser:**
   ```
   http://localhost/Online-exam-system/
   ```

---

## 🔐 Default Login Credentials

| Role     | Email               | Password   | Dashboard        |
|----------|---------------------|------------|------------------|
| Admin    | `admin@gmail.com`    | `admin123`     | `headdash.php`   |
| Teacher  | `teacher1@gmail.com`| `teacher1` | `dash.php`       |
| Student  | *(sign up to create)* | —        | `account.php`    |

- **Students** log in at the main page (`index.php`)
- **Admin & Teachers** log in at the admin portal (`admin_login.php`)

---

## 📁 Project Structure

```
Online-exam-system/
├── index.php              # Student sign-in / sign-up portal
├── admin_login.php        # Admin & Teacher login portal
├── account.php            # Student dashboard
├── dash.php               # Teacher dashboard
├── headdash.php           # Admin dashboard
├── update.php             # Backend operations (quiz, user, admin CRUD)
├── logout.php             # Session destroyer
├── assets/
│   └── img/
│       └── ecusta_logo.png  # University logo
├── config/
│   └── dbConnection.php   # Database connection config
├── css/
│   └── theme.css          # Global stylesheet & theme variables
├── js/
│   └── theme.js           # Theme toggle & shared UI scripts
├── fonts/
│   ├── gothic.ttf         # Gothic font
│   └── typo.ttf           # Typo font
├── includes/
│   ├── login.php          # Student login handler
│   ├── sign.php           # Student registration handler
│   ├── head.php           # Admin login handler
│   ├── admin.php          # Teacher login handler
│   ├── signadmin.php      # Teacher registration handler
│   └── feed.php           # Feedback submission handler
└── database/
    ├── project1.sql       # Database schema & seed data
    ├── patch_schema.php   # Schema patch v1
    ├── patch_schema_v2.php
    ├── patch_schema_v3.php
    └── patch_schema_v4.php
```

---

## 🗄️ Database Schema

| Table       | Purpose                                |
|-------------|----------------------------------------|
| `user`      | Student accounts (name, email, college, etc.) |
| `admin`     | Teacher & admin accounts (email, password, role) |
| `quiz`      | Quiz metadata (title, marks, time limit) |
| `questions` | Quiz questions                         |
| `options`   | Answer options for each question       |
| `answer`    | Correct answer mapping                 |
| `history`   | Student exam attempts & scores         |
| `rank`      | Cumulative student rankings            |
| `feedback`  | Student feedback messages              |

---

## 🎨 Tech Stack

- **Backend:** PHP 7.4+
- **Database:** MySQL 5.7+
- **Frontend:** HTML5, CSS3, JavaScript
- **Fonts:** [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts)
- **Icons:** [Material Icons](https://fonts.google.com/icons) (Google Fonts)
- **Design:** Glassmorphism, dark theme, responsive sidebar layout

---

