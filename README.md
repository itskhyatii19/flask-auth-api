# 🔐 Flask Authentication API  
### *Secure • Scalable • Production-style Backend*

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat-square&logo=python)
![Flask](https://img.shields.io/badge/Flask-Backend-black?style=flat-square&logo=flask)
![JWT](https://img.shields.io/badge/Auth-JWT-orange?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue?style=flat-square&logo=docker)
![Swagger](https://img.shields.io/badge/API-Swagger-green?style=flat-square&logo=swagger)
![SQLite](https://img.shields.io/badge/Database-SQLite-blue?style=flat-square&logo=sqlite)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-purple?style=flat-square)


A **modern authentication system** built using **Flask**, **JWT**, and **SQLite**.  
This project implements **secure login, token-based authentication, role-based authorization, and blacklist logout system**.

> ⚡ Designed following **real-world backend architecture** and security practices.

---

##  Highlights

- ✔ **JWT Authentication** (Access & Refresh Tokens)  
- ✔ **Role-Based Access Control**  
- ✔ **Secure Password Hashing (bcrypt)**  
- ✔ **Token Blacklist Logout**  
- ✔ **Protected Routes**  
- ✔ **Swagger API Documentation**  
- ✔ **Dockerized Application**  
- ✔ **Resume-ready Backend Project**

---

##  Features

-  **JWT Authentication**
-  **User Signup & Login**
-  **Access & Refresh Tokens**
-  **Role-Based Authorization (Admin/User)**
-  **Logout using Token Blacklist**
-  **Protected Routes**
-  **SQLite Database**
-  **API Testing (Swagger / Postman / Terminal)**
-  **Docker Support**

---

## 🛠 Tech Stack

| Layer | Technology |
|--------|------------|
| **Backend** | Flask (Python) |
| **Authentication** | Flask-JWT-Extended |
| **API Docs** | Flask-RESTX (Swagger) |
| **Database** | SQLite |
| **Security** | bcrypt |
| **Containerization** | Docker |
| **Testing** | Postman, curl |

---

## 📁 Project Structure

```text
flask_auth_api/
│
├── app.py              # Main Flask application
├── auth.py             # Authentication logic
├── db.py               # Database operations
├── decorators.py       # Role-based decorators
├── blacklist.py        # Token blacklist logic
├── users.db            # SQLite database
│
├── tests/              # Test scripts
│   ├── test_api.py
│   ├── test_login.py
│   └── test_logout.py
│
├── Dockerfile
├── .dockerignore
├── requirements.txt
└── README.md
```
## Setup & Run (Local)

### Clone Repository
```bash
git clone https://github.com/itskhyatii19/flask-auth-api.git
cd flask-auth-api
Create Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows
Install Dependencies
pip install -r requirements.txt
Run Server
python app.py
The server runs at:
```text
http://127.0.0.1:5000
```
Swagger API Documentation:
```text
http://127.0.0.1:5000/
```
### Run with Docker
```bash
docker build -t flask-auth-api .
docker run -p 5000:5000 flask-auth-api
```
Open:
```text
http://127.0.0.1:5000
```
## API Endpoints
### Signup
### POST /auth/signup
```json
{
  "username": "khyati",
  "password": "1234",
  "role": "admin"
}
```
### Login
### POST /auth/login
```json
{
  "username": "khyati",
  "password": "1234"
}
```
### Response
```json
{
  "access_token": "...",
  "refresh_token": "...",
  "user": {
    "username": "khyati",
    "role": "admin"
  }
}
```
### Protected Route
### GET /auth/dashboard

### Headers
```text
Authorization: Bearer <access_token>
```
### Logout
### POST /auth/logout

### Headers
```text
Authorization: Bearer <access_token>
```
### Security
```text
Passwords hashed using bcrypt
JWT token expiry implemented
Refresh token mechanism
Token blacklist logout
Role-based access control
Protected routes
```
## What I Learned
```text
REST API development with Flask
JWT authentication workflows
Secure password storage using bcrypt
Token-based authorization
Role-based access control
Swagger API documentation
Docker containerization
Debugging backend systems
Designing clean, modular backend architectures
```
## Future Enhancements
```text
Email verification
Password reset workflow
Unit testing with pytest
Advanced Swagger documentation
Docker Compose support
Cloud deployment
```
## Author
### Khyati Sharma
B.Tech AI Student
💻 Backend & ML Enthusiast
