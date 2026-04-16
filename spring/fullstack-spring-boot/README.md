# Fullstack Spring Boot

Fullstack Spring Boot is a customer management application split into a Spring Boot backend and a React frontend. It combines persistence, authentication, API design, frontend integration, and containerized local startup in a single end-to-end project.

## Architecture

- `customer-api/`: Spring Boot 3 backend for customer operations and authentication
- `frontend-react/`: Vite + React frontend for the customer UI
- `docker-compose.yml`: local stack for PostgreSQL, the backend container, and the frontend container

## Backend highlights

The backend uses:

- Spring Web for HTTP APIs
- Spring Data JPA and JDBC for data access
- PostgreSQL as the primary datastore
- Flyway for schema migrations
- Spring Security and JWT for authentication
- Testcontainers for integration-style database testing

The main API entry points are:

- `CustomerController`
- `AuthenticationController`

## Frontend highlights

The frontend uses:

- Chakra UI for components
- Formik and Yup for forms and validation
- Axios for API calls
- React Router for routing
- `jwt-decode` for auth token handling

## What it demonstrates

- building a REST API with Spring Boot 3
- integrating a React client with a secured backend
- managing schema changes with Flyway
- applying JWT-based authentication in a small full-stack system
- running a multi-service development stack with Docker Compose

## Running locally

Run the full stack with containers:

```bash
docker compose up --build
```

That exposes:

- PostgreSQL on `localhost:5332`
- the backend on `localhost:8088`
- the frontend on `localhost:3000`

For a code-first workflow:

1. Start PostgreSQL with `docker compose up db`
2. Start the backend in `customer-api/` with `./mvnw spring-boot:run`
3. Start the frontend in `frontend-react/` with `npm install` and `npm run dev`
