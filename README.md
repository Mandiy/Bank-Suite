# Bank-Suite — Microservices Based Banking Application

A **Java Full Stack Microservices Banking System** built using **Spring Boot, Spring Cloud, JWT Security, and React.js**.

This project demonstrates a **scalable microservices architecture** for banking operations such as account management, transactions, authentication, and KYC verification.

---

# Project Overview

Bank-Suite simulates a real-world banking backend where different services operate independently but communicate through an **API Gateway and Service Discovery**.

The system follows modern **microservices architecture principles**:

* Independent services
* Secure authentication using JWT
* Centralized routing via API Gateway
* Dynamic service discovery
* Scalable backend architecture

---

# Architecture

```text
Frontend (React)
       │
       ▼
API Gateway
       │
       ▼
Service Discovery (Eureka)
       │
 ┌─────┼─────────┬─────────┬─────────┐
 ▼     ▼         ▼         ▼         ▼
Auth   Account   Transaction Loan    KYC
Service Service   Service     Service Service
       │
       ▼
      MySQL
```

---

# Features

Secure Authentication using **JWT**

Microservices-based architecture

API Gateway for centralized routing

Service Discovery using **Eureka**

Account Management

* Create account
* Deposit money
* Withdraw money
* Transfer funds

Transaction history tracking

KYC verification service

Loan service simulation

RESTful API communication

Docker support (optional)

---

# Tech Stack

### Backend

Java 17
Spring Boot
Spring Security
JWT Authentication
Spring Cloud Gateway
Eureka Service Discovery
JPA / Hibernate
MySQL
Maven

### Frontend

React.js
Axios
Bootstrap / CSS

### DevOps

Docker (optional)
Git & GitHub

---

# Project Structure

```text
Bank-Suite
│
├── api-gateway
│
├── discovery-service
│
├── auth-service
│
├── transaction-service
│
├── loan-service
│
├── kyc-service
│
├── frontendBank
│
└── README.md
```

---

# How to Run the Project

### 1 Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Bank-Suite.git
cd Bank-Suite
```

---

### 2 Start Discovery Server

```bash
cd discovery-service
mvn spring-boot:run
```

Eureka dashboard:

```
http://localhost:8761
```

---

### 3 Start API Gateway

```bash
cd api-gateway
mvn spring-boot:run
```

---

### 4 Start Microservices

Run each service individually.

```bash
cd auth-service
mvn spring-boot:run
```

```bash
cd transaction-service
mvn spring-boot:run
```

```bash
cd loan-service
mvn spring-boot:run
```

```bash
cd kyc-service
mvn spring-boot:run
```

---

### 5 Start Frontend

```bash
cd frontendBank
npm install
npm start
```

Application runs on:

```
http://localhost:3000
```

---

# Default Test Credentials

```text
Username: admin
Password: admin123
```

---

# API Endpoints Example

Authentication

```
POST /auth/login
POST /auth/register
```

Transactions

```
POST /transactions/deposit
POST /transactions/withdraw
POST /transactions/transfer
GET  /transactions/history
```

Loan

```
POST /loan/apply
GET  /loan/status
```

KYC

```
POST /kyc/verify
GET  /kyc/status
```

---

# Future Improvements

Add Redis caching

Add distributed tracing

Implement rate limiting

Add Kubernetes deployment

Improve UI dashboard

---

# Author
Manvendra Singh 
Backend & Microservices Developer

---

# License

This project is for **educational and learning purposes**.
