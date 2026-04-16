# Quiz Engine

Quiz Engine is a Spring Boot API for user registration, authentication, and quiz management. It is a focused backend project for practicing the core Spring stack: security, validation, persistence, and REST endpoint design.

## Core capabilities

- user registration through `RegistrationController`
- quiz operations through `QuizController`
- PostgreSQL-backed persistence
- endpoint protection with Spring Security
- request validation and readable API error messages

## Tech stack

- Spring Boot
- Spring Web
- Spring Security
- Spring Data JPA
- PostgreSQL
- Gradle

## Configuration

The application is configured to:

- run on port `8080`
- connect to a local PostgreSQL database named `quizdb`
- use `ddl-auto=create-drop` for easy learning-oriented resets
- expose management endpoints broadly during development

## What it demonstrates

- securing a REST API with authentication
- modelling and persisting domain entities with JPA
- implementing quiz-specific business behavior on top of standard CRUD flows
- structuring a small but non-trivial Spring backend project

## Running locally

Make sure PostgreSQL is running with settings that match `src/main/resources/application.yml`, then start the application with:

```bash
./gradlew bootRun
```

Run the tests with:

```bash
./gradlew test
```
