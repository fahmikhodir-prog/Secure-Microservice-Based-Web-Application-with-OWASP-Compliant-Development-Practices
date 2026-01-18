# Secure Django Task Management System

This project is a secure web-based task management system built using Django.  
It demonstrates secure software development practices including authentication, access control, audit logging, and protection against common web vulnerabilities.

The system provides:
- User registration and login
- Role-based access (Admin & Normal User)
- Secure task management (CRUD)
- Audit logging for security events (Admin only)
- Protection against unauthorized access and injection attacks

---

# Team Members

- Muhammad Firdaus bin Shahrin (52215124185)
- Muhammad Asyraf bin Aznan (52215124467)
- Muhammad Faiz Fahmi bin Abdul Khodir (52215124461)
- Muhammad Eizuddin bin Azman (52215124075)

---

# Technology Stack
- Framework: Django (Python)
- Database: SQLite (development)
- Authentication: Django Authentication System
- Authorization: Role-Based Access Control (Admin / User)
- Environment Management: python-dotenv
- Security Features:
  - CSRF Protection
  - Password Hashing (PBKDF2)
  - Secure Sessions
  - ORM-based database access

---

# Security Features Implemented (OWASP-Aligned)

- Server-side input validation using Django Forms (OWASP A03)
- Password hashing using Django’s built-in PBKDF2 hasher (OWASP A02)
- User authentication with secure session management
- Role-Based Access Control (RBAC) for protected resources
- CSRF protection enabled on all forms (OWASP A01)
- ORM usage to prevent SQL Injection
- Output escaping via Django template engine (XSS prevention)
- Secure error handling (no stack traces exposed to users)
- Audit logging of important user activities
- Sensitive configuration stored in environment variables

---

# Project Structure
```text
secure_django/
│
├── .env.example                # Example environment configuration
├── README.md
│
├── secure_project/
│   ├── docs/                     # Screenshots and documentation
│   ├── manage.py
│   ├── db.sqlite3
│   │
│   ├── secure_project/         # Core project configuration
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   │
│   ├── accounts/               # User registration, login, dashboard
│   │   ├── models.py
│   │   ├── forms.py
│   │   ├── views.py
│   │   └── templates/
│   │
│   ├── audit/                  # Audit logging (admin view)
│   │   ├── models.py
│   │   └── views.py
│   │
│   ├── tasks/                  # Secure CRUD module
│   │   ├── models.py
│   │   ├── forms.py
│   │   └── views.py
│   │
│   └── templates/
│
└── venv/                       # Virtual environment

---

# Functional Modules

- User Registration

- User Login & Logout

- User Dashboard

- Secure Task Management (CRUD)

- Role-Based Access Control

- Admin Audit Log Page

---

# Dependencies

- Django
- python-dotenv

---

# Security Notice

This application is developed for academic purposes as part of the Secure
Software Development course. It is not intended for production deployment.

---

# License

For Academic use only.

---

# Screenshots

- 1. Login Page

![Login Page](docs/Login_Page.jpeg)

This screenshot shows the secure login page with CSRF protection enabled.
User credentials are authenticated using Django’s built-in authentication
mechanism with secure session handling.

---

- 2. User Registration Page

![User Registration](docs/User_Registration.jpeg)

This page allows new users to register with server-side input validation
and enforced password policies to prevent weak credentials.

---

- 3. User Dashboard (Normal User)

![User Dashboard](docs/User_Dashboard.jpeg)
![User Dashboard](docs/User_Dashboard_2.jpeg)

The dashboard is accessible only after successful authentication.
Normal users do not have access to administrative functions,
demonstrating Role-Based Access Control (RBAC).

---

- 4. Secure Task Management (CRUD Module)

![Task Management](docs/Secure_Task_Management(CRUD).jpeg)

This screenshot demonstrates the secure CRUD functionality for task
management. All database operations are handled through Django ORM,
preventing SQL Injection attacks.

---

- 5. Admin Audit Log Page

![Admin Audit Log](docs/Admin_Auditlog.jpeg)

This page is accessible only to admin users and displays audit logs
for login attempts and critical user actions, supporting logging
and monitoring requirements.

---

## Installation Steps

1. Clone the repository:
```bash
git clone <https://github.com/fahmikhodir-prog/Secure-Microservice-Based-Web-Application-with-OWASPCompliant-Development-Practices.git>
cd secure_django

2. Create and activate virtual environment:
python -m venv venv
.\venv\Scripts\Activate.ps1

3. Install dependencies:
pip install django python-dotenv

4.Apply migrations:
cd secure_project
python manage.py migrate

5. Create admin account:
python manage.py createsuperuser

## How to Run the Application
cd secure_project
python manage.py runserver

Open in browser:
http://127.0.0.1:8000/
