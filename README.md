# RESQ — Backend Platform Super-Repository (`resq-backend-platform`)

## Student & Assessment Details
- **Student Name:** Gamitha
- **Student Number:** HDSE-ITS2130-ECA
- **Slack Handle:** `@gamitha`
- **GCP Project ID:** `resq-enterprise-cloud`
- **Course:** ITS 2130 — Enterprise Cloud Architecture

---

## 1. Repository Architecture & Git Submodules
This parent super-repository consolidates the Spring Cloud platform infrastructure components using **Git Submodules**:

```
resq-backend-platform/
├── config-server/      (Submodule -> resq-config-server)
├── eureka-server/      (Submodule -> resq-eureka-server)
├── api-gateway/        (Submodule -> resq-api-gateway)
└── .gitmodules
```

---

## 2. Platform Components
1. **`config-server` (Port 8888):** Spring Cloud Config Server managing all environment configuration files.
2. **`eureka-server` (Port 8761):** Netflix Eureka Service Discovery Registry.
3. **`api-gateway` (Port 8080):** Spring Cloud API Gateway with HMAC-SHA256 JWT Authentication, RBAC, and dynamic routing.

---

## 3. Cloning & Setup
To clone this super-repository along with all submodules:
```bash
git clone --recurse-submodules <REPOSITORY_URL>
```

To update existing submodules:
```bash
git submodule update --init --recursive
```
