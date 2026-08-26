# RESQ — Backend Platform Super-Repository (`resq-backend-platform`)

## Student & Assessment Details
- **Student Name:** H.V.Gamitha Gimhana Jayasanka
- **Student ID / Number:** 241711007
- **Slack Handle:** Gamitha Gimhana
- **GCP Project ID:** `resq-enterprise-cloud-01`
- **Course:** ITS 2130 — Enterprise Cloud Architecture

---

## 1. Project Description
`resq-backend-platform` is the parent super-repository consolidating the foundational **Spring Cloud Platform Infrastructure** components for the RESQ Disaster Response System using **Git Submodules**. It provides centralized external configuration management, dynamic service discovery, distributed load balancing, and secure edge API routing.

---

## 2. Platform Architecture & Submodules
```
resq-backend-platform/
├── config-server/      (Submodule -> resq-config-server, Port 8888)
├── eureka-server/      (Submodule -> resq-eureka-server, Port 8761)
├── api-gateway/        (Submodule -> resq-api-gateway, Port 8080)
└── .gitmodules
```

### Components:
1. **`resq-config-server` (Port 8888):** Spring Cloud Config Server managing centralized profile-based configurations (`application.yml`, `incident-service.yml`, `response-service.yml`, `evidence-service.yml`, `api-gateway.yml`).
2. **`resq-eureka-server` (Port 8761):** Netflix Eureka Service Discovery Registry coordinating multi-zone microservice registration and health monitoring.
3. **`resq-api-gateway` (Port 8080):** Reactive Spring Cloud Gateway providing JWT authentication, Role-Based Access Control (RBAC), distributed trace injection (`X-Trace-Id`), and reverse proxy routing.

---

## 3. Technology Stack
- **Language & Runtimes:** Java 25 / 21 LTS
- **Frameworks:** Spring Boot 3.3.5, Spring Cloud 2023.0.3 (Config, Eureka, Gateway)
- **Deployment:** Google Cloud Compute Engine Multi-Zone MIG (IaaS)
- **Process Manager:** PM2 Process Manager

---

## 4. Setup & Getting Started Instructions

### Clone with Submodules
```bash
git clone --recurse-submodules https://github.com/GamithaGimhana/RESQ-Backend-Platform.git
cd RESQ-Backend-Platform
```

### Update Submodules
```bash
git submodule update --init --recursive
```

### Build All Platform Components
```bash
mvn clean package -DskipTests
```
