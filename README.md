# EduLibrary Manager

A Spring Boot web application with completed front-end for managing a digital book catalogue with user authentication and role-based authorization.

---

## Overview

This project is a **Book Database Application Library**.
It provides an online catalogue of books and role-based access for Readers, Publishers, Librarians, and Administrators.

---

## Features

### User Roles & Permissions
| Role        | Permissions |
|--------------|-------------|
| **Visitor**   | Can get a list of all books on the site, login, register |
| **Reader**    | Can search a book by it`s title, Can get all books by its genre, Can get list of newest books (last 5) that were added, can view book catalogue |
| **Publisher** | Can get a list of all books on a site, Can add new book, delete, edit, get info about a book, view own books |
| **Librarian** | Can get a list of all users on a site, can get a list of all books in a library, can get a total number of books in library, Add / edit / delete books |
| **Admin**     | Validate accounts, manage users and roles, adding / editing / deleting books, adding / editing / deleting users, gets statical reports about books, can do everyting that other can do |

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

## 🖼️ Screenshots
 - Main Screen (Home)
<img width="2551" height="1286" alt="image" src="https://github.com/user-attachments/assets/b3526114-0fb4-47d0-95de-00e817063ba0" />
 - Details about specific book
<img width="2552" height="428" alt="image" src="https://github.com/user-attachments/assets/70235e34-05da-44fa-ad89-9147217ae946" />
 - Sign in page
<img width="2558" height="560" alt="image" src="https://github.com/user-attachments/assets/6e515234-5b62-4868-8f5f-8985aff5fff2" />
- Register account as a Reader
<img width="2554" height="496" alt="image" src="https://github.com/user-attachments/assets/36a9f11f-da1e-4a28-af43-12e36281d743" />
 - Register account as a Publisher
<img width="2533" height="501" alt="image" src="https://github.com/user-attachments/assets/3a6cd24d-0d83-485b-9a0f-f1705ca730c2" />
 - Register account as a Librarian
<img width="1900" height="433" alt="image" src="https://github.com/user-attachments/assets/f937bbc7-4bb4-4c01-9b67-9e62e61cb192" />

 - Admin panel for managing users
<img width="2554" height="1372" alt="image" src="https://github.com/user-attachments/assets/b25205b1-3ec3-4817-b638-53eacfac596b" />
 - Admin panel for managing a specific user by it`s id
<img width="2553" height="1363" alt="image" src="https://github.com/user-attachments/assets/3be4aaac-b448-44df-82de-00d1c6a190bb" />
 - Statistical report of published books by Publisher
<img width="2557" height="1369" alt="image" src="https://github.com/user-attachments/assets/d81147ab-a9f7-4b3e-be85-799415e278b1" />
 - Adding a book as a Publisher
<img width="2542" height="1370" alt="image" src="https://github.com/user-attachments/assets/23ffb4a7-2667-4a95-8766-36a52fcab200" />

and many other functionalities...
---

## Technologies Used

| Layer | Technologies |
|-------|---------------|
| **Backend** | Java 21, Spring Boot, Spring MVC, Spring Data JPA, Spring Security, Hibernate |
| **Security** | Spring Security, BCrypt |
| **Frontend** | Thymeleaf, HTML5, Bootstrap |
| **Database** | H2 |
| **Build Tool** | Gradle |

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
