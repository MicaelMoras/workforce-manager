# Workforce Manager

A RESTful API developed with **Java and Spring Boot** to manage workers, departments, hourly contracts and calculate employee income.

## About the Project

Workforce Manager is a backend application designed to manage employees and their departments, register hourly contracts and calculate monthly income based on the contracts associated with each worker.

The project was developed to practice object-oriented programming, REST API development, database persistence and entity relationships using the Spring ecosystem.

## Technologies

- Java
- Spring Boot
- Spring Data JPA
- Hibernate
- H2 Database
- Maven

## Features

- Register and manage workers.
- Organize workers by department.
- Manage hourly contracts.
- Associate multiple contracts with a worker.
- Calculate the total value of hourly contracts.
- Calculate monthly worker income.
- Retrieve worker income through a REST endpoint.

## Domain Model

The application uses the following main entities:

| Entity | Description |
|---|---|
| Worker | Represents an employee. |
| Department | Represents an organizational department. |
| HourContract | Represents an hourly employment contract. |
| WorkerLevel | Defines the worker's professional level. |

## API Endpoint

### Get Worker Monthly Income

Retrieves the monthly income of a specific worker.

**Request:**

`GET /workers/{id}/income/{year}/{month}`

**Example:**

`GET /workers/1/income/2018/8`

**Response:**

```json
{
  "name": "Alex",
  "department": "Design",
  "income": 1000.0
}
```

*The response values are illustrative and depend on the registered contracts.*

## Project Structure

```text
src
└── main
    ├── java
    │   └── com.MicaelMoras.Interprise
    │       ├── config
    │       ├── controller
    │       ├── dto
    │       ├── entities
    │       ├── repositories
    │       └── InterpriseApplication.java
    │
    └── resources
        └── application.properties
```

## How to Run

**1. Clone the repository**

```bash
git clone https://github.com/MicaelMoras/workforce-manager.git
```

**2. Enter the project directory**

```bash
cd workforce-manager
```

**3. Run the application using Maven Wrapper**

On Windows:

```bash
mvnw.cmd spring-boot:run
```

On Linux or macOS:

```bash
./mvnw spring-boot:run
```

The application will start using the Spring Boot configuration defined in the project.

## Learning Objectives

This project explores important backend development concepts:

- Object-Oriented Programming (OOP).
- RESTful API architecture.
- Entity relationships (One-to-Many and Many-to-One).
- Data Transfer Objects (DTO).
- Repository Pattern.
- Database persistence with JPA and Hibernate.
- Business logic and income calculations.

## Author

**Micael Moras**

Computer Science Student | Java Backend Developer in Progress

[GitHub Profile](https://github.com/MicaelMoras)

---

*This project is part of my journey to becoming a software engineer, continuously learning and building practical applications.*
