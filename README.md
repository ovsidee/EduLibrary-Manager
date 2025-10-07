# EduLibrary Manager

A Spring Boot web application with completed front-end for managing a digital book catalogue with user authentication and role-based authorization.

---

## Overview

This project is a **Book Database Application Library**, developed as part of the **TPO12** coursework.  
It provides an online catalogue of books and role-based access for Readers, Publishers, Librarians, and Administrators.

Users can browse books, register accounts, and perform actions depending on their assigned roles.

---

## Project Structure

- src/main/
  - java/com/example/tpo12/
    - controller/ → Web controllers (BookController, AuthController, AdminController)
    - model/ → Entities (Book, User, Role, etc.)
    - repository/ → Spring Data JPA repositories
    - service/ → Business logic (BookService, UserService)
    - config/ → Spring Security configuration
  - resources/
    - templates/ → Thymeleaf views (catalogue.html, login.html, register.html, admin.html, etc.)
    - static/ → CSS / JS / images
    - application.properties

---

## Features

### User Roles & Permissions
| Role        | Permissions |
|--------------|-------------|
| **Reader**    | View book catalogue, register account, login |
| **Publisher** | Register publisher account, view own books |
| **Librarian** | Add / edit / delete books, get statical reports about books |
| **Admin**     | Validate accounts, manage users and roles, adding / editing / deleting books, gets statical reports about books |

---

### Catalogue
- Displays all books (title, author, ISBN etc)
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
 - Main Screen (Home)
<img width="2551" height="1286" alt="image" src="https://github.com/user-attachments/assets/b3526114-0fb4-47d0-95de-00e817063ba0" />
 - Details about specific book
<img width="2553" height="1358" alt="image" src="https://github.com/user-attachments/assets/37ad2a1c-9e60-4d77-8a78-8993f2f8d68d" />
 - Sign in page
<img width="2551" height="1280" alt="image" src="https://github.com/user-attachments/assets/96f124ce-c098-4e97-9bba-eba69acf240f" />
 - Register account as a Reader
<img width="2552" height="1284" alt="image" src="https://github.com/user-attachments/assets/e0a0acdc-92d2-456e-aedd-4b36d5ddd729" />
 - Register account as a Publisher
<img width="2560" height="1273" alt="image" src="https://github.com/user-attachments/assets/6c1149d3-a32a-4227-9336-7534ab64aa6d" />
 - Admin panel for managing users
<img width="2554" height="1372" alt="image" src="https://github.com/user-attachments/assets/b25205b1-3ec3-4817-b638-53eacfac596b" />
 - Admin panel for managing a specific user by it`s id
<img width="2553" height="1363" alt="image" src="https://github.com/user-attachments/assets/3be4aaac-b448-44df-82de-00d1c6a190bb" />
 - Statistical report of published books by Publisher
<img width="2557" height="1369" alt="image" src="https://github.com/user-attachments/assets/d81147ab-a9f7-4b3e-be85-799415e278b1" />
 - Adding a book as a Publisher
<img width="2542" height="1370" alt="image" src="https://github.com/user-attachments/assets/23ffb4a7-2667-4a95-8766-36a52fcab200" />

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
