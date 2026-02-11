# 📘 Book Management System – Spring Boot CRUD API

A RESTful backend application built using **Spring Boot** to manage books with full CRUD operations. The project follows a clean layered architecture (Controller → Service → Repository) and uses an **H2 in-memory database** for quick development and testing.

This project demonstrates practical backend development concepts such as REST API design, dependency injection, JPA/Hibernate ORM, and structured code organization.

---

## 🚀 Features

• Add new books
• View book details
• Search books by title
• Update book information
• Delete books
• H2 database console for testing
• Clean layered architecture

---

## 🛠 Tech Stack

• Java 17+
• Spring Boot
• Spring Data JPA (Hibernate)
• H2 In‑Memory Database
• Lombok
• Maven

---

## 📂 Project Structure

src/main/java
├── controller → REST endpoints
├── service → business logic
├── repository → database access
├── entity → Book model
└── BookApplication.java

src/main/resources
└── application.properties

---

## ⚙️ Configuration (application.properties)

spring.datasource.url=jdbc:h2:mem:studentdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

---

## ▶️ Running the Application

### Method 1 – Maven

mvn spring-boot:run

### Method 2 – IDE

Run BookApplication.java directly from IntelliJ or Eclipse.

Server starts at:

[http://localhost:8080](http://localhost:8080)

---

## 🌐 REST API Endpoints

### ➕ Add Book

POST /addBook

Request Body:
{
"title": "Clean Code",
"author": "Robert Martin",
"genre": "Programming"
}

---

### 🔍 Get Book By Title

GET /getBook/{bookName}

Example:
/getBook/Clean Code

---

### ✏️ Update Book

PUT /updateBook

Request Body:
{
"id": 1,
"title": "Clean Code 2",
"author": "Robert Martin",
"genre": "Programming"
}

---

### ❌ Delete Book

DELETE /deleteBook/{id}

Example:
/deleteBook/1

---

## 🗄 H2 Database Console

URL:
[http://localhost:8080/h2-console](http://localhost:8080/h2-console)

Login Details:

JDBC URL → jdbc:h2:mem:studentdb
Username → sa
Password → (leave blank)

---

## 🧠 Key Learning Outcomes

• Built REST APIs using Spring Boot
• Applied layered architecture for clean code separation
• Used JPA/Hibernate for ORM mapping
• Performed CRUD operations with JpaRepository
• Tested database using H2 in-memory console
• Implemented dependency injection and service-based design

---

## 📌 Future Enhancements

• Swagger/OpenAPI documentation
• Input validation using @Valid
• Global exception handling (@ControllerAdvice)
• Pagination and sorting
• MySQL/PostgreSQL integration
• Authentication with JWT

---

## 👨‍💻 Author

Vinoth Kumar D
Java Backend Developer
LinkedIn | GitHub
