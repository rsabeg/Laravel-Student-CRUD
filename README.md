# 🎓 Laravel Student CRUD Application

A full-stack web application built with **Laravel 12** that demonstrates complete **CRUD (Create, Read, Update, Delete)** operations on a Student Management System. Built as part of the **Android & Web Application Development** course at the **University of Frontier Technology, Bangladesh**.

---

## Preview

| All Students | Add Student | Edit Student |
|---|---|---|
| List page with Edit & Delete | Form with input fields | Pre-filled editable form |

>  See `Lab_Report.pdf` for full screenshots of every step.

---

## Features

- ✅ **Create** — Add new student records via a simple form
- ✅ **Read** — View all students in a structured table
- ✅ **Update** — Edit any student's information
- ✅ **Delete** — Remove student records instantly
- ✅ MVC Architecture (Model → View → Controller)
- ✅ MySQL database integration via Eloquent ORM
- ✅ Blade templating engine for dynamic views
- ✅ RESTful routing using `Route::resource()`

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Laravel 12 (PHP) |
| Database | MySQL (via XAMPP) |
| Frontend | HTML, Blade Templates |
| ORM | Eloquent |
| Dev Server | PHP Artisan |
| Package Manager | Composer |

---

## 📁 Project Structure

```
Crudapp/
├── app/
│   ├── Http/Controllers/
│   │   └── StudentController.php   ← CRUD logic
│   └── Models/
│       └── Student.php             ← Eloquent Model
├── database/
│   └── migrations/
│       └── ..._create_students_table.php
├── resources/views/students/
│   ├── index.blade.php             ← List all students
│   ├── create.blade.php            ← Add new student form
│   └── edit.blade.php              ← Edit student form
├── routes/
│   └── web.php                     ← Resource routes
└── .env                            ← Database config
```

---

## ⚙️ Installation & Setup

### Prerequisites
- PHP >= 8.2
- Composer
- XAMPP (Apache + MySQL)

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/ICE1945/laravel-crud-app.git
cd laravel-crud-app
```

**2. Install dependencies**
```bash
composer install
```

**3. Configure environment**
```bash
cp .env.example .env
php artisan key:generate
```

**4. Set up database**

Open phpMyAdmin and create a database named `Crudapp`, then update `.env`:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Crudapp
DB_USERNAME=root
DB_PASSWORD=
```

**5. Run migrations**
```bash
php artisan migrate
```

**6. Start the server**
```bash
php artisan serve
```

**7. Open in browser**
```
http://127.0.0.1:8000/students
```

---

## Database Schema

**Table: `students`**

| Column | Type | Description |
|---|---|---|
| id | INT (PK, Auto) | Primary key |
| name | VARCHAR | Student's full name |
| email | VARCHAR | Student's email address |
| phone | VARCHAR | Student's phone number |
| course | VARCHAR | Enrolled course name |
| created_at | TIMESTAMP | Auto-generated |
| updated_at | TIMESTAMP | Auto-generated |

---

## CRUD Routes

| Method | URL | Action | Description |
|---|---|---|---|
| GET | /students | index() | Show all students |
| GET | /students/create | create() | Show add form |
| POST | /students | store() | Save new student |
| GET | /students/{id}/edit | edit() | Show edit form |
| PUT | /students/{id} | update() | Update student |
| DELETE | /students/{id} | destroy() | Delete student |

---

## Lab Report

Full lab report with step-by-step screenshots is available in this repository:
📎 [`Lab_Report_Laravel_CRUD.pdf`](./Lab_Report_Laravel_CRUD.pdf)

**Course:** PROG 212 — Android & Web Application Development Sessional  
**Institution:** University of Frontier Technology, Bangladesh  
**Department:** Cyber Security Engineering

---

## 👨‍💻 Author

**Ragib Shahriar Abeg**  
Cybersecurity Engineering Student | UFTB  
🔗 [LinkedIn](https://linkedin.com/in/rsabeg) · [GitHub](https://github.com/ICE1945)

