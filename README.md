
# event-basket
A REST API for event booking platform
=======
# Event Basket Platform

A Java 17, Spring Boot 3.x microservices project for events, orders, and users. Each service is containerized with Docker and uses MySQL, Kafka, and Flyway for database migrations.

## Services
- user-service: User registration, authentication, and profiles
- order-service: Orders and ticketing
- event-service: Event management

## Tech Stack
- Java 17, Spring Boot 3.x, Spring MVC, Spring Data JPA, Spring Security
- Lombok, MapStruct
- MySQL, Flyway
- Kafka (Apache Kafka / Spring for Apache Kafka)
- Docker / Docker Compose
- Maven

## Prerequisites
- Java 17 (JDK)
- Docker and Docker Compose
- Maven or Maven Wrapper (recommended: `./mvnw`)
- A running MySQL and Kafka (or use Docker Compose)

## Environment Variables
Provide these in your environment (e.g., `.env`, Kubernetes secrets, or CI/CD secrets):
- `JWT_SECRET=<your_secure_jwt_secret>`
- `DB_HOST=<db_host>`
- `DB_PORT=<db_port>`
- `DB_NAME=<db_name>`
- `DB_USERNAME=<db_username>`
- `DB_PASSWORD=<db_password>`
- `KAFKA_BOOTSTRAP_SERVERS=<host:port>`
- `SPRING_PROFILES_ACTIVE=dev` (optional)

Each service should read these via `application.yml`/`application.properties`. Example (do not commit real secrets):# Event Basket Application

Event Basket is a microservices-based application for managing events, users, and orders. It's built using Spring Boot and utilizes Apache Kafka for inter-service communication.

## Project Structure

The application consists of three main microservices:

1. User Service
2. Event Service
3. Order Service

Each service is contained in its own directory and can be run independently.

## Services

### User Service

Handles user-related operations and listens to order events.

Key components:
- Spring Security for authentication
- Kafka consumer for order events
- JPA for database interactions

### Event Service

Manages event-related operations.

Key components:
- RESTful API for event management
- JPA for database interactions
- Springdoc OpenAPI for API documentation

### Order Service

Handles order processing and publishes order events.

Key components:
- Kafka producer for order events
- JPA for database interactions
- Springdoc OpenAPI for API documentation

## Setup and Running

### Prerequisites

- Java 17
- Docker and Docker Compose
- Maven

### Steps to Run

1. Clone the repository:
>>>>>>> e7dc9e8 (solve failing builds issue)
