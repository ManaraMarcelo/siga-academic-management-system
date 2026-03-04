# SIGA: Integrated Academic Management System with Spring Boot 📚

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) ![Thymeleaf](https://img.shields.io/badge/Thymeleaf-%23005F0F.svg?style=for-the-badge&logo=Thymeleaf&logoColor=white) ![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)

> **Course:** Object-Oriented Programming (OOP)  
> **Professor:** Marcos Roberto de Moraes (Maromo)

**SIGA** is a professional-grade Fullstack web application (REST API + Thymeleaf Frontend) developed for school administration. It centralizes student records, teacher assignments, and automated grade calculations within a robust Spring Boot architecture.

---

### 💡 Project Overview

**The Problem:** Academic institutions often struggle with fragmented data. Managing the complex relationship between students, teachers, subjects, and grades manually leads to data inconsistency and administrative delays.

**The Solution:** A centralized Integrated Academic Management System. SIGA uses a relational model to link all academic entities, ensuring data integrity. It provides a RESTful interface for external integrations and a Thymeleaf-based UI for direct user interaction.



**Technical Challenges:**
- **Relational Integrity:** Implementing JPA (Java Persistence API) to manage complex "Many-to-Many" and "One-to-Many" relationships between Teachers, Subjects, and Classes.
- **Automated Calculations:** Developing business logic that automatically calculates student averages and updates academic status (Pass/Fail) in real-time.
- **Developer Experience:** Integrating SpringDoc OpenAPI to provide a live, interactive documentation environment (Swagger UI) for API testing.

---

## 📌 Table of Contents
1. [Technologies Used](#-technologies-used)
2. [Project Architecture](#-project-architecture)
3. [API Endpoints](#-api-structure-endpoints)
4. [Installation & Execution](#-installation-and-execution)
5. [Database Configuration](#-database-configuration-h2)
6. [User Manual](#-user-manual---siga)
7. [Implementation Backlog](#-project-backlog)
8. [Contact](#-contact)

---

## 🚀 Technologies Used

- **Core:** Java 21 (LTS), Spring Boot 3.x
- **Persistence:** Spring Data JPA, H2 Database (File Mode)
- **Web Layer:** Spring Web, Thymeleaf, Validation
- **Documentation:** SpringDoc OpenAPI (Swagger UI)
- **Build & Management:** Maven (Wrapper included)
- **UI:** Bootstrap 5 (via CDN)

---

## 📂 Project Architecture

The system follows a strict **MVC** and **Layered Architecture** pattern:



```text
com.poo.siga  
├── config/        # API Documentation & CORS settings
├── controller/    # REST Layer (Request Mapping)
├── model/         # JPA Entities & Business Logic
├── repository/    # Data Access Layer (Spring Data)
└── SigaApplication.java

```

---

## 🛠️ Installation and Execution

### Prerequisites

* **JDK 21** or higher.
* **Git** for cloning.

### ▶️ Step-by-Step

1. **Clone the Repository:**

```sh
git clone [https://github.com/ManaraMarcelo/siga-academic-management-system.git](https://github.com/ManaraMarcelo/siga-academic-management-system.git)
cd siga-academic-management-system

```

2. **Run the Application:**

**Windows:**

```sh
./mvnw.cmd spring-boot:run

```

**Linux / Mac:**

```sh
chmod +x mvnw
./mvnw spring-boot:run

```

3. **Access the Services:**

* **Web UI:** `http://localhost:8080`
* **Interactive API (Swagger):** `http://localhost:8080/swagger-ui/index.html`
* **DB Console (H2):** `http://localhost:8080/h2-console`

---

## 📚 API Structure (Endpoints)

| Method | Endpoint | Description |
| --- | --- | --- |
| GET | `/api/alunos` | List all students |
| POST | `/api/alunos` | Register new student |
| GET | `/api/turmas` | List available classes |
| POST | `/api/turmas` | Link Teacher to Subject |
| PUT | `/api/matriculas/{id}/notas` | Update student grades (P1, P2, P3) |

---

## 📖 User Manual - SIGA

<details> <summary><strong>Click to expand Full Manual</strong></summary>

### 1. Registration Flow

For data consistency, please follow this order: **Teachers -> Subjects -> Classes -> Students -> Grades.**

### 2. Grade Entry Logic

The system allows inputting three exam scores (P1, P2, P3). Upon saving, the system automatically calculates the weighted average and determines if the student is **Approved** or **Reproved**.

### 3. Visual Examples

</details>

---

## 📝 Project Backlog

| ID | Task | Module | Status |
| --- | --- | --- | --- |
| B01 | MVC Architecture Setup | Planning | ✅ Done |
| B15 | Grade Logic (P1-P3) | Grades | ✅ Done |
| B17 | Swagger UI Integration | Infra | ✅ Done |

---

## 👨‍💻 Development Team

* [Lucas Vieira](https://github.com/Lucas-WBB)
* [Marcelo Belloto](https://github.com/marcelo-belotto)
* [Marcelo Manara](https://github.com/ManaraMarcelo)
* [Vinícius Emanuel](https://github.com/vinicius-emanuelds)

---

## 🔗 Contact

**Marcelo Manara** [LinkedIn](https://www.linkedin.com/in/marcelo-manara) | [Portfolio](https://portifolio-peach-beta.vercel.app/)
