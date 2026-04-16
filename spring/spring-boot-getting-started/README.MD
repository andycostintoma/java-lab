# Spring Boot Getting Started

Spring Boot Getting Started is a PostgreSQL-backed CRUD application built around a `StudentController`. It is the most direct introduction here to the standard Spring Boot web and persistence stack.

## Core capabilities

- exposing CRUD endpoints with Spring MVC
- persisting student data with Spring Data JPA
- connecting a Spring Boot application to PostgreSQL
- showing generated SQL during development

## Tech stack

- Spring Boot 2.7
- Spring Web
- Spring Data JPA
- PostgreSQL
- Maven

## Configuration

The application is configured to:

- connect to a local PostgreSQL database named `student`
- use `create-drop` for schema lifecycle during development
- show formatted Hibernate SQL
- include error messages in HTTP responses while debugging

## What it demonstrates

- the basic Spring Boot request-to-database flow
- a small layered architecture with controller, service, and persistence concerns
- the minimal pieces needed for a real database-backed web service

## Running locally

Make sure PostgreSQL is running with credentials that match `src/main/resources/application.properties`, then start the application with:

```bash
./mvnw spring-boot:run
```

Run the tests with:

```bash
./mvnw test
```
