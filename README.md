# 🚀 Taskify – Scalable Task Management System

A **production-ready backend system** built using **Spring Boot Microservices Architecture**, designed to handle secure task management with **JWT-based authentication**, optimized database performance, and scalable REST API design.

---

## 🧠 System Overview

Taskify is a **microservices-based task management platform** that enables users to securely manage tasks with full CRUD operations.

The system is divided into independent services:

* 🔐 **User Service** – Handles authentication & user management
* 📝 **Task Service** – Manages task operations
* 🌐 **API Gateway** – Central entry point for routing and security

---

## 🏗️ Architecture

```
Client → API Gateway → (User Service / Task Service) → MySQL
```

* Microservices communication via REST APIs
* Stateless authentication using JWT
* Layered architecture (Controller → Service → Repository)
* Independent services for scalability and maintainability

---

## ⚙️ Tech Stack

* **Java 22**
* **Spring Boot 3**

  * Spring Security
  * Spring Data JPA
  * Spring MVC
* **MySQL 8**
* **JWT (JSON Web Tokens)**
* **Maven**
* **Postman (API Testing)**

---

## 🔐 Key Features

* ✅ Secure **JWT-based authentication & authorization**
* ✅ User registration & login system
* ✅ Full CRUD operations on tasks
* ✅ Task filtering (completed / pending)
* ✅ Search functionality (by title)
* ✅ Microservices-based architecture
* ✅ API Gateway routing
* ✅ Scalable and modular backend design

---

## 📈 Performance & Optimization

* Optimized database queries using **indexing**
* Reduced response time through efficient service-layer design
* Stateless authentication ensures scalability
* Modular services allow independent scaling and maintenance

---

## 📡 API Endpoints

### 🔐 User Service

| Method | Endpoint          | Description                    |
| ------ | ----------------- | ------------------------------ |
| POST   | `/users/register` | Register a new user            |
| POST   | `/users/login`    | Authenticate user & return JWT |

---

### 📝 Task Service

| Method | Endpoint             | Description         | Auth Required |
| ------ | -------------------- | ------------------- | ------------- |
| POST   | `/tasks/add`         | Add a new task      | ✅             |
| GET    | `/tasks/all`         | Get all tasks       | ✅             |
| PUT    | `/tasks/update`      | Update a task       | ✅             |
| DELETE | `/tasks/delete/{id}` | Delete a task       | ✅             |
| GET    | `/tasks/pending`     | Get pending tasks   | ✅             |
| GET    | `/tasks/completed`   | Get completed tasks | ✅             |

---

## 🚀 Getting Started

### 1️⃣ Clone Repository

```bash
git clone https://github.com/Nimarjot1/Taskify_Springboot.git
cd Taskify_Springboot
```

---

### 2️⃣ Configure Database

Update `application.properties` in each service:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

---

### 3️⃣ Build Project

```bash
mvn clean install
```

---

### 4️⃣ Run Services

```bash
# Run User Service
cd user-service
mvn spring-boot:run

# Run Task Service
cd task-service
mvn spring-boot:run

# Run API Gateway
cd api-gateway
mvn spring-boot:run
```

---

## 🧪 Testing APIs

Use **Postman** or any API client:

1. Register user → `/users/register`
2. Login → `/users/login` → get JWT token
3. Use token in header:

```
Authorization: Bearer <your_token>
```

4. Access secured endpoints

---

## 🧩 Future Enhancements

* 🔄 Redis caching for improved performance
* 📊 Analytics dashboard (task insights & usage tracking)
* 📬 Email notifications for task updates
* 🐳 Docker containerization
* ☁️ Cloud deployment (AWS / Render)

---

## 💡 Key Learnings

* Designed scalable **microservices architecture**
* Implemented secure authentication using **Spring Security + JWT**
* Optimized relational databases using indexing strategies
* Built modular backend systems following industry best practices

---

## 📌 Author

**Nimarjot Kaur**
🔗 GitHub: https://github.com/Nimarjot1
