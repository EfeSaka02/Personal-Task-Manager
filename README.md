# TaskManagerPro – PHP MVC Based Task Management App

TaskManagerPro is a feature-rich personal task management application developed using PHP and the MVC (Model-View-Controller) architectural pattern. It helps users to efficiently manage their daily tasks, organize them into categories, and monitor progress with status and reporting tools.

---

## 👤 Developer

- Name: Efe Saka
- Student ID: 55934

---

## 🛠 Installation Guide

### Prerequisites

- XAMPP or equivalent (Apache, MySQL, PHP 8+)
- Modern web browser (Chrome, Firefox, etc.)
- phpMyAdmin for database operations

### Steps to Set Up

1. **Install and Launch XAMPP**

   - Start Apache and MySQL from the XAMPP control panel

2. **Create the Database**

   - Open `http://localhost/phpmyadmin` in your browser
   - Click "New" and create a database named `personal_task_manager`
   - Choose collation `utf8mb4_general_ci`

3. **Import the Database Schema**

   - Select the `personal_task_manager` database
   - Go to the “Import” tab and upload `schema.sql` from the `database/` folder
   - Click “Go” to import tables and structure

4. **Place the Project in htdocs**

   - Copy the `TaskManagerPro_EfeSaka` project folder into:
     - Windows: `C:\xampp\htdocs\TaskManagerPro_EfeSaka`
     - macOS: `/Applications/XAMPP/htdocs/TaskManagerPro_EfeSaka`

5. **Configure Database Connection**

   - Open `config.php`
   - Ensure the PDO connection settings are:
     ```php
     $host = 'localhost';
     $db   = 'personal_task_manager';
     $user = 'root';
     $pass = '';
     ```

6. **Launch the App**
   - In browser, go to:  
     `http://localhost/TaskManagerPro_EfeSaka/public/`

---

## 👨‍🏫 How to Use the App

### User Registration and Login

- Register with a username, email, and password
- Log in to access your personal dashboard
- Sessions are used to maintain login state

### Task Features

- Add tasks with title, description, due date, and priority
- Tasks can be updated or deleted
- Mark tasks as done, or switch between “to-do”, “in progress”, and “done”
- Tasks are grouped by user and optional category

### Category System

- Create your own categories (Work, Personal, etc.)
- Assign tasks to categories
- Edit or delete categories

### Search, Filter & Sorting

- Search tasks by title or description
- Filter by category, status, or priority
- Sort tasks by due date or importance

### Reports

- Get summary of tasks by status
- See overdue tasks
- View total tasks by category and how many are completed

---

## ✔ Features Overview

- Secure registration and login system
- Task and category CRUD
- Filtering and searching of tasks
- Status management: todo / in progress / done
- Detailed task reports and overdue tracking
- Sorting and clean UI
- Password hashing and XSS-safe output

---

## ❗ Common Issues & Fixes

- **Blank screen**: Check PHP error logs in XAMPP
- **403 Forbidden**: On macOS, run `chmod -R 755` on project folder
- **Can’t connect to DB**: Double-check config.php credentials
- **Session not working**: Ensure sessions are enabled in php.ini
