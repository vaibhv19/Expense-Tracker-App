# 💰 Expense Tracker Microservices Application

A scalable, production-ready **Expense Tracker** built using **Java, Spring Boot, Kafka, and Microservices Architecture**.
This application helps users manage expenses, track spending patterns, and gain insights into their financial behavior.

---

## 🚀 Overview

This project is designed using a **microservices architecture** where each service is independently deployable and scalable.
It supports real-time expense tracking, asynchronous processing, and secure authentication.

---

## 🧩 Architecture

### 🔹 Services

* 🔐 **Auth Service**

  * Handles authentication & authorization
  * Generates JWT & refresh tokens

* 👤 **User Service**

  * Manages user profile and preferences

* 💸 **Expense Service**

  * Core service for managing expenses
  * Handles CRUD operations for transactions

* 📊 **Analytics Service**

  * Processes expense data
  * Generates reports and insights using event-driven architecture

---

## 🔗 System Flow

1. User logs in via **Auth Service** → receives JWT
2. Requests go through **API Gateway** (optional)
3. Expense is created via **Expense Service**
4. Expense Service publishes event to **Kafka**
5. **Analytics Service** consumes events and generates insights

---

## ⚙️ Tech Stack

### 🖥️ Backend

* Java
* Spring Boot
* Spring Security (JWT)
* Spring Data JPA

### 🗄️ Database

* MySQL (per service architecture)

### 📡 Messaging

* Apache Kafka (event-driven communication)

### ⚡ Caching (Optional)

* Redis

### 🐳 DevOps

* Docker
* Docker Compose

---

## 📡 API Endpoints (Sample)

### 🔐 Auth Service

```
POST /auth/signup
POST /auth/login
POST /auth/refresh
```

### 👤 User Service

```
GET /users/{id}
PUT /users/{id}
```

### 💸 Expense Service

```
POST /expenses
GET /expenses?userId={id}
DELETE /expenses/{id}
```

---

## 📊 Features

* ✅ Secure Authentication using JWT
* ✅ Expense Tracking & Categorization
* ✅ Event-Driven Architecture using Kafka
* ✅ Scalable Microservices Design
* ✅ Real-time Analytics Processing
* ✅ Configurable & Extensible System

---

## 🔮 Future Enhancements

* 🤖 AI-based financial insights & recommendations
* 📩 Automatic expense tracking via SMS parsing
* 🔔 Smart notifications (overspending alerts)
* 📱 Mobile app integration (React Native)
* ☁️ Cloud deployment (AWS / Kubernetes)

---

## 🧠 Key Concepts Demonstrated

* Microservices Architecture
* Event-Driven Systems (Kafka)
* JWT Authentication & Security
* RESTful API Design
* Distributed System Design
* Docker-based Deployment

---

## 🛠️ Setup Instructions

### 1. Clone the Repository

```
git clone https://github.com/your-username/expense-tracker-microservices.git
cd expense-tracker-microservices
```

### 2. Start Infrastructure (Kafka, MySQL)

```
docker-compose up -d
```

### 3. Run Services

Run each service individually:

```
./gradlew bootRun
```

---

## 📁 Project Structure

```
expense-tracker/
│
├── auth-service/
├── user-service/
├── expense-service/
├── analytics-service/
├── docker-compose.yml
└── README.md
```

---

## 👨‍💻 Author

**Vaibhav Gupta**

---

## ⭐ If you like this project

Give it a star ⭐ and share your feedback!
