# Inventory Service

Inventory is the core backend microservice responsible for managing personal asset data within the Keepwise ecosystem. It handles all inventory-related operations such as item tracking, categorization, and metadata management.

> 🚧 **Status**: Building – MVP in active development

---

## 📦 Overview

This service implements the **Inventory bounded context** following **Domain-Driven Design (DDD)** principles to ensure maintainability, scalability, and clear separation of concerns.

* Backend RESTful API built with **Java 21** and **Spring Boot 3**
* Persistence with **PostgreSQL** using **Spring Data JPA**
* Containerized with **Docker** for consistent environment setup
* Layered architecture with explicit separation:

  * `controller` — REST API endpoints
  * `service` — Business logic and orchestration
  * `repository` — Data access and persistence
  * `model` — DTOs and data transfer objects
  * `domain` — Core entities, value objects, and domain logic
  * `mapper` — Conversion between domain and model layers

---

## 🏗 Architecture & Design

* The project follows a **clean layered architecture** to promote separation of concerns and testability.
* Business rules are encapsulated inside the **domain** layer, ensuring domain purity.
* The **mapper** layer guarantees decoupling between domain entities and external API contracts.
* **Service** layer orchestrates use cases and transactions, acting as the application core.
* The **repository** layer abstracts all persistence concerns with Spring Data JPA.

---

## ⚙️ Key Features

* Full CRUD operations for inventory items, with validation and business rules enforcement
* Flexible categorization of items (e.g., clothing, electronics, tools)
* Rich metadata management (brand, purchase date, estimated value, condition)
* Support for pagination, sorting, and filtering on queries
* Robust exception handling with standardized API error responses

---

## 🧪 Testing & Quality Assurance

* Aim for **100% code coverage** with comprehensive tests:

  * Unit tests covering domain, service, and mapper layers using **JUnit 5** and **Mockito**
  * Integration tests leveraging **Testcontainers** to run a real PostgreSQL instance in Docker
  * Controller tests with **Spring MockMvc** for API validation
* Automated test execution integrated in build lifecycle (Maven/Gradle)

---

## 🚀 Getting Started

1. Clone the repository
2. Configure PostgreSQL connection in `application.yml` or use provided Docker Compose setup for local environment
3. Build and run the service using Maven or Docker commands
4. API documentation available via OpenAPI/Swagger for endpoint exploration

---

## 📚 Tech Stack

* Java 21
* Spring Boot 3
* Spring Data JPA
* PostgreSQL
* Docker & Docker Compose
* JUnit 5, Mockito

