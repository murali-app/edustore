# 📚 EduStore – Online Exam & PDF Selling Platform (Spring Boot – Modular Monolith)

**EduStore** is a unified platform designed for students, educators, and professionals to **buy and sell educational PDFs**, as well as to **create, take, and manage online exams**. Built using a modular monolith architecture with Spring Boot, EduStore combines robust user management, secure payments, and real-time notifications to deliver a seamless digital learning experience.

---

## 🏗️ Project Structure (Modular Monolith)

Each feature/domain is organized into self-contained modules, promoting scalability and separation of concerns.

# edustore core modules


•	🛒 **PDF Store:** Upload and sell educational notes, e-books, and guides.
•	🧪 **Online Exams:** Create exams, manage questions, submit results.
•	🔐 **User Authentication:** Secure login, JWT-based auth, OTP & email verification.
•	💳 **Integrated Payments:** Buy PDFs or exams using Razorpay or Stripe.
•	📈 **Sales Tracking:** View purchase history and sales analytics.
•	🔔 **Smart Notifications:** Email & SMS alerts for purchases, exams, and more.
•	👤 **Admin Dashboard:** Manage users, roles, products, and exams.



---

## 📌 Modules Overview

### 1. 🔐 **Auth Module**
Handles:
- User registration and login
- JWT token-based authentication
- Email verification
- OTP (mobile) verification

📦 Packages:
- `com.edustore.auth.controller`
- `com.edustore.auth.service`
- `com.edustore.auth.entity`
- `com.edustore.auth.repository`
- `com.edustore.auth.security`

---

### 2. 👤 **User Module**
Handles:
- User CRUD
- Profile management
- Role management (Admin/User)

📦 Packages:
- `com.edustore.user.entity`
- `com.edustore.user.controller`
- `com.edustore.user.service`
- `com.edustore.user.repository`

---

### 3. 💰 **Sales Module**
Handles:
- Product purchase
- Purchase tracking
- Future: Sales analytics

📦 Packages:
- `com.edustore.sales.entity`
- `com.edustore.sales.controller`
- `com.edustore.sales.service`
- `com.edustore.sales.repository`

---

### 4. 🧪 **Exam Module**
Handles:
- Online exam participation
- Questions & answers
- Exam results

📦 Packages:
- `com.edustore.exam.entity`
- `com.edustore.exam.controller`
- `com.edustore.exam.service`
- `com.edustore.exam.repository`

---

### 5. 💳 **Payment Module**
Handles:
- Integration with Razorpay/Stripe
- Payment status, tracking, invoicing

📦 Packages:
- `com.edustore.payment.entity`
- `com.edustore.payment.controller`
- `com.edustore.payment.service`
- `com.edustore.payment.gateway`

---

### 6. 🔔 **Notification Module**
Handles:
- Email service
- SMS/OTP service
- Notification templates

📦 Packages:
- `com.edustore.notification.email`
- `com.edustore.notification.sms`
- `com.edustore.notification.template`

---

### 7. ⚙️ **Common Module**
Reusable components:
- API response wrappers
- Exception handling
- Constants and enums

📦 Packages:
- `com.edustore.common.response`
- `com.edustore.common.exception`
- `com.edustore.common.enums`
- `com.edustore.common.config`

---

### 8. 🛡️ **Config Module**
Central configuration:
- Spring Security setup
- JWT filters
- Swagger/OpenAPI docs
- Global exception handling

📦 Packages:
- `com.edustore.config.security`
- `com.edustore.config.exception`
- `com.edustore.config.swagger`

---

## 🧩 Entity-Relationship Diagram (ERD)

The system includes the following key entities and relationships:

### ✅ Auth & User
- `User`, `Role`, `VerificationToken`

### ✅ Sales
- `Product`, `Purchase`, `Payment`

### ✅ Exam
- `Exam`, `Question`, `Answer`, `Result`

### ✅ Notification
- `Email`, `SMS`

> 📎 View the full ERD here: **[ERD Diagram](./docs/er-diagram.png)**

---

## 🎯 Who Is EduStore For?

- 📘 **Students** – looking for affordable, high-quality study materials.
- 👩‍🏫 **Educators** – who want to monetize their notes or conduct exams.
- 🏫 **Institutions** – managing certifications or internal assessments.

---

## 🚀 Tech Stack

- **Spring Boot 3.x**
- **Spring Security + JWT**
- **Spring Data JPA**
- **Razorpay / Stripe SDK**
- **Swagger / SpringDoc**
- **PostgreSQL / MySQL**
- **H2 (for dev/testing)**
- **Lombok**, **MapStruct** (optional)

---
