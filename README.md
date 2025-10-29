# Bookstore User Service

## 🎯 Description
Spring Boot microservice for managing users in the Bookstore system.  
Provides CRUD operations for users and is prepared to connect to a MySQL database.

## ⚡ Features
- Spring Boot 3.x
- Java 17
- REST API with Spring Web
- Data persistence with Spring Data JPA
- Lombok for boilerplate reduction
- Validation for input data
- MySQL integration

## 🛠 Requirements
- Java 17
- Maven
- MySQL 8.x running locally

## 🚀 Setup

1. **Clone the repository**
```bash

git clone https://github.com/LuizSaraiva/bookstore-user-service.git
cd bookstore-user-service
```

Create the MySQL database
```
CREATE DATABASE bookstore_db;
```
Configure database credentials in src/main/resources/application.yml
```
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/bookstore_db?useSSL=false&serverTimezone=UTC
    username: root
    password: root
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
    database-platform: org.hibernate.dialect.MySQL8Dialect
```

Build and run the project
```
mvn clean install
mvn spring-boot:run
```

Testing
```
mvn test
```

📁 Project Structure
```
src/main/java/com/bookstore/userservice/
 ├─ controller       # REST controllers
 ├─ service          # Business logic
 ├─ repository       # JPA repositories
 ├─ entity           # Database entities
 ├─ dto              # Data transfer objects (optional)
 ├─ exception        # Custom exceptions
 └─ config           # Application configurations

src/main/resources/
 ├─ application.yml      # Main Spring Boot config
 ├─ application-dev.yml  # Optional: dev profile
 ├─ application-prod.yml # Optional: prod profile
 └─ static/              # Static resources (optional)

```

✅ Notes

This project is prepared to be extended with authentication, security, and microservices patterns.

Follow this README to set up the environment locally before developing new features.

📝 License

MIT License