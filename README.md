# EduLibrary Manager

A Spring Boot web application with completed front-end for managing a digital book catalogue with user authentication and role-based authorization.

---

## Overview

This project is a **Book Database Application Library**, developed as part of the **TPO12** coursework.  
It provides an online catalogue of books and role-based access for Readers, Publishers, Librarians, and Administrators.

Users can browse books, register accounts, and perform actions depending on their assigned roles.

---

## Project Structure

src/main/
│
├── java/com/example/tpo12/
│ ├── controller/ # Web controllers (BookController, AuthController, AdminController)
│ ├── model/ # Entities (Book, User, Role, etc.)
│ ├── repository/ # Spring Data JPA repositories
│ ├── service/ # Business logic (BookService, UserService)
│ └── config/ # Spring Security configuration
│
└── resources/
├── templates/ # Thymeleaf views (catalogue.html, login.html, register.html, admin.html, etc.)
├── static/ # CSS / JS / images
└── application.properties
---

## Features

### User Roles & Permissions
| Role        | Permissions |
|--------------|-------------|
| **Reader**    | View book catalogue, register account |
| **Publisher** | Register publisher account, view own books |
| **Librarian** | Add / edit / delete books |
| **Admin**     | Validate accounts, manage users and roles |

---

### Catalogue
- Displays all books (title, author, ISBN)
- Clicking a book shows detailed information
- Accessible to all users (including guests)

### Registration
Separate registration forms for:
- **Readers**
- **Publishers**

Each form collects:
- First name, last name  
- Email  
- Password  

### Authentication
- Implemented via **Spring Security**
- Role-based access restrictions
- Passwords encrypted with BCrypt

---

## 🖼️ Screenshots

---

## Technologies Used

| Layer | Technologies |
|-------|---------------|
| **Backend** | Java 17, Spring Boot, Spring MVC, Spring Data JPA |
| **Security** | Spring Security, BCrypt |
| **Frontend** | Thymeleaf, HTML5, Bootstrap |
| **Database** | MySQL (or H2 for dev) |
| **Build Tool** | Maven |

---

## 🚀 Running the Application

### 1️⃣ Clone the repository
git clone https://github.com/ovsidee/Java-Spring.git
cd Java-Spring/TPO12/TPO12

### 2️⃣ Configure Database
Edit src/main/resources/application.properties:
spring.datasource.url=jdbc:mysql://localhost:3306/bookdb
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update

### 3️⃣ Run the application
mvn spring-boot:run

Then open:  
👉 http://localhost:8080
