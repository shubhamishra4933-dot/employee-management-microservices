# 🚀 Employee Management Microservices

![Java](https://img.shields.io/badge/Java-17-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-brightgreen)
![Spring Security](https://img.shields.io/badge/Spring_Security-JWT-success)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-purple)
![Maven](https://img.shields.io/badge/Build-Maven-red)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black)

## 📋 Overview

Employee Management Microservices is a production-style backend application developed using Java and Spring Boot. The project demonstrates Microservices Architecture, JWT Authentication, Service Discovery, API Gateway Routing, PostgreSQL Integration, and RESTful API development.

This project is designed to showcase enterprise-level backend development skills for Java Backend Developer roles.

---

## 🏗️ Architecture Diagram

```text
                    +------------------+
                    |    API Gateway   |
                    |      :8080       |
                    +--------+---------+
                             |
          -----------------------------------------
          |                  |                    |
          v                  v                    v

+----------------+  +----------------+  +------------------+
| Auth Service   |  | Employee       |  | Department       |
| JWT Security   |  | Service        |  | Service          |
| :8081          |  | :8082          |  | :8083            |
+--------+-------+  +--------+-------+  +---------+--------+
         \                  |                     /
          \                 |                    /
           --------------------------------------
                             |
                             v

                   +------------------+
                   | Eureka Registry  |
                   |     :8761        |
                   +------------------+

                             |
                             v

                   +------------------+
                   | PostgreSQL DB    |
                   +------------------+
```

---

## 🛠️ Tech Stack

### Backend

* Java 17
* Spring Boot
* Spring MVC
* Spring Security
* Spring Data JPA
* Hibernate

### Microservices

* Eureka Service Registry
* Spring Cloud Gateway
* OpenFeign Client

### Security

* JWT Authentication
* Role-Based Authorization
* BCrypt Password Encryption

### Database

* PostgreSQL
* SQL
* JPA/Hibernate

### Tools

* Maven
* Git
* GitHub
* Postman

---

## 📂 Project Structure

```text
employee-management-microservices

├── service-registry
├── api-gateway
├── auth-service
├── employee-service
├── department-service
├── docs
├── screenshots
├── postman-collection
└── README.md
```

---

## 🔐 Authentication APIs

### Register User

```http
POST /auth/register
```

Request:

```json
{
  "username": "admin",
  "email": "admin@gmail.com",
  "password": "password",
  "role": "ADMIN"
}
```

### Login

```http
POST /auth/login
```

---

## 👨‍💼 Employee APIs

```http
GET     /employees
GET     /employees/{id}
POST    /employees
PUT     /employees/{id}
DELETE  /employees/{id}
```

---

## 🏢 Department APIs

```http
GET     /departments
GET     /departments/{id}
POST    /departments
PUT     /departments/{id}
DELETE  /departments/{id}
```

---

## 💾 Database Design

### Users

```sql
CREATE TABLE users(
id BIGSERIAL PRIMARY KEY,
username VARCHAR(100),
email VARCHAR(150),
password VARCHAR(255),
role VARCHAR(50)
);
```

### Departments

```sql
CREATE TABLE departments(
id BIGSERIAL PRIMARY KEY,
department_name VARCHAR(100),
department_code VARCHAR(50)
);
```

### Employees

```sql
CREATE TABLE employees(
id BIGSERIAL PRIMARY KEY,
employee_name VARCHAR(150),
email VARCHAR(150),
phone VARCHAR(20),
salary NUMERIC(12,2),
department_id BIGINT
);
```

---

## ✨ Features

* JWT Authentication & Authorization
* Employee CRUD Operations
* Department CRUD Operations
* Microservices Architecture
* API Gateway Routing
* Service Discovery with Eureka
* PostgreSQL Integration
* RESTful API Development
* Layered Architecture
* Exception Handling
* Validation

---

## 📸 Screenshots

Add screenshots inside:

```text
screenshots/
```

Example:

* Eureka Dashboard
* PostgreSQL Tables
* Postman API Testing
* API Gateway Routes

---

## 📮 Postman Collection

Store Postman collection inside:

```text
postman-collection/
```

---

## 🚀 Future Enhancements

* Docker Support
* Kubernetes Deployment
* Redis Caching
* Kafka Event Streaming
* CI/CD Pipeline
* AWS Deployment

---

## 👨‍💻 Author

**Shubham Mishra**

* LinkedIn: https://www.linkedin.com/in/shubham-mishra-97b19725a/
* GitHub: https://github.com/shubhamishra4933-dot

---

## 🎯 Resume Keywords

Java, Spring Boot, Spring Security, JWT Authentication, PostgreSQL, REST APIs, Hibernate, JPA, Microservices, Eureka Server, API Gateway, OpenFeign, Maven, Git, GitHub, Backend Development, Distributed Systems, Software Engineering.
