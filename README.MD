# Rotaflow Backend API

> An automated workforce scheduling and shift management REST API engineered with **Node.js**, **Express.js**, **PostgreSQL**, **Docker**, and **Swagger**.

Rotaflow solves complex shift generation by implementing custom business logic that automates 4-week cyclical rotations (3 weeks active shift work, 1 week rest off) across multi-role workforce teams.

---

## 🏛️ System Architecture & Domain Design

The API is structured with clean separation of concerns across core modules:

| Module | Core Logic & Responsibilities |
| :--- | :--- |
| **`Auth & RBAC`** | JWT-based authentication with role-based access control (`ADMIN`, `MANAGER`, `WORKER`). |
| **`Worker Management`** | Profile management, availability tracking, and role assignment. |
| **`Scheduler Engine`** | Algorithmic shift generator enforcing cyclical work/rest constraints (3:1 rotation logic). |
| **`Reporting & Export`** | Printable schedule generation and output formatting. |

---

## 💡 Engineering Highlights

### 1. Algorithmic Shift Generation Engine
* **Deterministic Rotation Logic:** Computes future shift assignments programmatically across a 28-day sliding cycle, ensuring strict compliance with operational rules (21 days active / 7 days rest).
* **Conflict Prevention:** Validates worker availability and role dependencies to prevent double-booking or compliance violations.

### 2. Enterprise Integration Readiness
* **Containerized Workflows:** Fully Dockerized development and production setup with PostgreSQL container orchestration.
* **OpenAPI Documentation:** Standardized API contracts documented via Swagger UI for front-end and mobile consumption.

---

## 🛠️ Tech Stack

* **Runtime:** Node.js (v18+)
* **Framework:** Express.js
* **Database:** PostgreSQL
* **Authentication:** JSON Web Tokens (JWT) + bcrypt passkey hashing
* **Documentation:** Swagger / OpenAPI
* **DevOps & Infrastructure:** Docker, Docker Compose, Render

---

## ⚙️ Quickstart (Docker Setup)

### 1. Clone & Configure
```bash
git clone https://github.com/<your-new-username>/rotaflow-backend.git
cd rotaflow-backend
cp .env.example .env
```

### 2. Spin Up Containers
```bash
docker-compose up --build -d
```

### 3. API Documentation
Access the interactive OpenAPI interface at:
```text
http://localhost:5000/api-docs
```

---

## 🧪 Verification & Features Checklist

- [x] JWT Token Authentication & Protected Route Guards
- [x] Role-Based Access Control (RBAC)
- [x] Cyclical Worker Scheduling Algorithm (3 Weeks On / 1 Week Off)
- [x] Swagger API Documentation
- [x] Containerized Docker Deployment Setup

---

> *Note 1: Architected and developed as a specialized workforce scheduling service.*
> *Note 2: This project was originally conceptualized, architected, and migrated from my previous developer profile.*
