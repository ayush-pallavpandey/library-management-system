# 📚 Library Management System

<div align="center">

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green?style=for-the-badge&logo=springboot)
![Spring Security](https://img.shields.io/badge/Spring_Security-6.x-success?style=for-the-badge)
![JWT](https://img.shields.io/badge/JWT-Authentication-blue?style=for-the-badge)
![Hibernate](https://img.shields.io/badge/Hibernate-JPA-brown?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?style=for-the-badge&logo=mysql)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker)
![Swagger](https://img.shields.io/badge/Swagger-API_Docs-85EA2D?style=for-the-badge&logo=swagger)
![JUnit](https://img.shields.io/badge/JUnit-Testing-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### Production-Ready Library Management REST API built using Spring Boot

*A secure and scalable backend application for managing books, users, borrowing transactions, and library operations.*

</div>

---

# 📖 Table of Contents

- Overview
- Problem Statement
- Why I Built This
- Key Features
- Technology Stack
- System Architecture
- Project Structure
- Getting Started
- API Documentation
- REST Endpoints
- Security
- Testing
- Docker Support
- Future Improvements
- License
- Author

---

# 📚 Overview

The **Library Management System** is a backend REST API designed to automate and simplify library operations.

The application enables librarians and administrators to efficiently manage books, members, borrowing records, and returns while ensuring secure authentication and role-based authorization.

The project follows modern backend engineering practices including layered architecture, JWT authentication, API documentation, exception handling, validation, unit testing, and containerized deployment.

---

# ❓ What Problem Does This Solve?

Traditional library management often relies on manual record keeping or outdated desktop software, resulting in:

- Lost borrowing records
- Duplicate book entries
- Difficulty tracking issued books
- Limited accessibility
- Lack of secure authentication
- Poor scalability

This project solves these issues by providing a centralized RESTful backend capable of handling library operations securely and efficiently.

### Benefits

- Digital book catalog
- Easy member management
- Track book availability
- Prevent duplicate records
- Secure login using JWT
- Faster search operations
- Scalable backend architecture
- API-first design for future web/mobile applications

---

# 💡 Why Did I Build This?

I built this project to strengthen my backend engineering skills while solving a real-world business problem.

The primary objectives were to:

- Learn Spring Boot development
- Implement secure authentication using Spring Security and JWT
- Design scalable REST APIs
- Practice layered architecture
- Work with relational databases using JPA/Hibernate
- Build production-style backend applications
- Gain hands-on experience with Docker, Swagger, testing, and CI/CD

This project also serves as a portfolio project demonstrating backend development best practices.

---

# ✨ Key Features

## Authentication

- User Registration
- Secure Login
- JWT Authentication
- Role-Based Authorization
- Password Encryption (BCrypt)

---

## Book Management

- Add Books
- Update Books
- Delete Books
- Search Books
- View Available Books
- Book Availability Tracking

---

## Member Management

- Register Members
- Update Member Information
- Delete Members
- View Member Details

---

## Borrow & Return

- Issue Books
- Return Books
- Borrow History
- Due Date Tracking
- Fine Calculation (Future)

---

## Validation

- Request Validation
- Global Exception Handling
- Meaningful Error Responses

---

## Documentation

- Swagger UI
- OpenAPI Specification

---

## Testing

- Unit Testing
- Integration Testing
- Service Layer Testing
- Repository Testing

---

# 🛠 Technology Stack

| Category | Technologies |
|----------|--------------|
| Language | Java 21 |
| Framework | Spring Boot |
| Security | Spring Security, JWT |
| ORM | Hibernate, Spring Data JPA |
| Database | MySQL |
| Documentation | Swagger / OpenAPI |
| Build Tool | Maven |
| Testing | JUnit 5, Mockito |
| Containerization | Docker |
| Version Control | Git, GitHub |
| API Testing | Postman |

---

# 🏗 Architecture

The project follows a clean layered architecture.

```
                Client
                   │
        REST API Requests
                   │
        Controller Layer
                   │
         Service Layer
                   │
      Business Logic Layer
                   │
       Repository Layer (JPA)
                   │
             MySQL Database
```

### Architectural Principles

- Separation of Concerns
- Layered Architecture
- Dependency Injection
- SOLID Principles
- RESTful API Design

---

# 📂 Project Structure

```
library-management-system
│
├── src
│   ├── controller
│   ├── service
│   ├── repository
│   ├── entity
│   ├── dto
│   ├── config
│   ├── security
│   ├── exception
│   ├── util
│   └── test
│
├── docs
│   ├── architecture.png
│   ├── swagger-ui.png
│   └── postman-collection.json
│
├── Dockerfile
├── docker-compose.yml
├── pom.xml
└── README.md
```

---

# 🚀 How Do I Run It?

## Clone Repository

```bash
git clone https://github.com/yourusername/library-management-system.git
```

---

## Navigate

```bash
cd library-management-system
```

---

## Configure Database

Update:

```
application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/librarydb
spring.datasource.username=root
spring.datasource.password=yourpassword
```

---

## Build Project

```bash
mvn clean install
```

---

## Run Application

```bash
mvn spring-boot:run
```

Application starts on:

```
http://localhost:8080
```

---

## Swagger

```
http://localhost:8080/swagger-ui/index.html
```

---

# 🐳 Docker

Build Image

```bash
docker build -t library-management-system .
```

Run Container

```bash
docker run -p 8080:8080 library-management-system
```

---

# 📄 API Documentation

Swagger UI provides interactive API documentation for testing endpoints directly from the browser.

Example APIs include:

- Authentication
- Books
- Members
- Borrow Records
- Returns

---

# 🔗 Available APIs

## Authentication

```
POST /api/auth/register
POST /api/auth/login
```

---

## Books

```
GET /api/books

GET /api/books/{id}

POST /api/books

PUT /api/books/{id}

DELETE /api/books/{id}
```

---

## Members

```
GET /api/members

POST /api/members

PUT /api/members/{id}

DELETE /api/members/{id}
```

---

## Borrow

```
POST /api/borrow

POST /api/return

GET /api/history
```

---

# 🔒 Security

This application uses:

- Spring Security
- JWT Authentication
- BCrypt Password Encryption
- Stateless Authentication
- Role-Based Access Control

Supported Roles:

- ADMIN
- LIBRARIAN
- MEMBER

---

# ✅ Testing

Testing is implemented using:

- JUnit 5
- Mockito
- Spring Boot Test

Coverage includes:

- Service Layer
- Controller Layer
- Repository Layer
- Authentication
- Validation

---

# 📈 Planned Improvements

The following enhancements are planned for future releases:

- AI-powered book recommendations using Spring AI
- Natural language search
- Email notifications for due dates
- Fine calculation and payment integration
- Barcode and QR code support
- Book reservation system
- Multi-branch library support
- Redis caching
- Elasticsearch integration
- AWS deployment
- Kubernetes support
- CI/CD using GitHub Actions
- Monitoring with Prometheus and Grafana
- Microservices architecture
- Role-based analytics dashboard

---

# 🤝 Contributing

Contributions are welcome.

If you'd like to improve this project:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Ayush Pallav Pandey**

Java Backend Developer

- Java
- Spring Boot
- Spring Security
- Hibernate
- Docker
- AWS
- REST APIs
- Spring AI

⭐ If you found this project helpful, consider giving it a star!
