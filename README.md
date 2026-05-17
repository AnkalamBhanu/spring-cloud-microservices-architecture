# 🚀 Spring Cloud Microservices Architecture

A hands-on, production-inspired microservices project built with **Spring Boot** and **Spring Cloud**, demonstrating real-world patterns used in enterprise backend systems.

> 📄 A detailed notes document (`Spring-Cloud-Microservices-Notes-Updated.docx`) is included — covering architecture decisions, configurations, and key learnings.

---

## 🧩 Services Overview

| Service | Description |
|---|---|
| `service-registry` | Eureka Server — handles service discovery & registration |
| `cloud-config-server` | Centralized configuration management for all services |
| `cloud-gateway` | API Gateway — single entry point, routing & filtering |
| `order-service` | Handles order creation and management |
| `payment-service` | Processes payments with fault tolerance |

---

## ⚙️ Key Concepts Covered

- 🔍 **Service Discovery** — Eureka-based dynamic service registration
- 🗂️ **Centralized Configuration** — Spring Cloud Config Server serving shared & per-service configs
- 🌐 **API Gateway** — Unified routing via Spring Cloud Gateway
- ⚡ **Circuit Breaker & Fallback** — Resilience4j for fault tolerance
- 🔗 **Inter-service Communication** — Using `@HttpExchange` (Spring 6+)
- 🔄 **Retry Mechanisms** — Graceful degradation under failure

---

## 🛠️ Tech Stack

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)

- **Java** + **Spring Boot 3**
- **Spring Cloud** (Eureka, Config Server, Gateway)
- **Resilience4j** (Circuit Breaker, Retry)
- **Maven** (multi-module build)
- **REST APIs**

---

## 📁 Project Structure

```
spring-cloud-microservices-architecture/
├── service-registry/         # Eureka Server
├── cloud-config-server/      # Config Server
├── cloud-gateway/            # API Gateway
├── order-service/            # Order Management
├── payment-service/          # Payment Processing
└── Spring-Cloud-Microservices-Notes-Updated.docx
```

---

## 🚦 How to Run

> Start services **in this exact order** — each depends on the previous.

### 1. Clone the repo

```bash
git clone https://github.com/AnkalamBhanu/spring-cloud-microservices-architecture.git
cd spring-cloud-microservices-architecture
```

### 2. Start services in order

```bash
# Step 1 - Service Registry (Eureka)
cd service-registry
mvn spring-boot:run

# Step 2 - Config Server
cd ../cloud-config-server
mvn spring-boot:run

# Step 3 - API Gateway
cd ../cloud-gateway
mvn spring-boot:run

# Step 4 - Order Service
cd ../order-service
mvn spring-boot:run

# Step 5 - Payment Service
cd ../payment-service
mvn spring-boot:run
```

### 3. Access Eureka Dashboard

```
http://localhost:8761
```

All registered services will be visible here.

---

## 📄 Documentation

A comprehensive notes document is included in the repo:

📎 [`Spring-Cloud-Microservices-Notes-Updated.docx`](./Spring-Cloud-Microservices-Notes-Updated.docx)

Covers:
- Architecture decisions
- Service configurations
- Circuit breaker setup
- Config server integration
- Key learnings and gotchas

---

## 👤 Author

**Bhanu Ankalam**
- GitHub: [@AnkalamBhanu](https://github.com/AnkalamBhanu)

---

> ⭐ If you find this helpful, feel free to star the repo!
