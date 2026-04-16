# Customer

Customer is a small but complete Quarkus backend centered on customer management. It is the kind of project that sits in the sweet spot between a toy example and a real service: small enough to read in one sitting, but broad enough to cover the pieces that matter in day-to-day backend work.

## What the project does

The application exposes a REST API under `/customers` and supports the usual CRUD flow:

- create a customer
- list all customers
- fetch a single customer by id
- update an existing customer
- delete a customer

Behind that API, the project wires together request validation, exception mapping, persistence, schema migration, and runtime configuration in a way that resembles a real service rather than a one-endpoint tutorial.

## Technical focus

The stack is built around:

- Quarkus 3 with Java 17
- REST endpoints with JSON payloads
- PostgreSQL as the backing database
- Panache for the persistence layer
- Flyway migrations applied at startup
- Hibernate Validator for request validation
- OpenAPI support for endpoint discovery
- basic HTTP auth enabled through configuration
- optional keystore-based HTTPS setup via `generate-keystore.sh`

The project also includes explicit exception types and mappers for common API failures, which makes it useful as a reference for shaping cleaner HTTP responses instead of letting raw server errors leak through.

## Project structure

- `boundary/` contains the REST layer and request DTOs
- `control/` contains mapping, repository, and service logic
- `entity/` holds the persistence model and DTOs
- `exception/` centralizes API error handling
- `src/main/resources/db/migration/` contains the Flyway migrations

That structure makes it easy to follow the request path from HTTP entry point down to persistence and back out through mapped responses.

## Local development

Start PostgreSQL first:

```bash
docker compose up -d
```

The compose file starts a local `customerdb` PostgreSQL container on port `5432`.

Run the service in dev mode:

```bash
mvn quarkus:dev
```

The local datasource is configured as:

- JDBC URL: `jdbc:postgresql://localhost:5432/postgres`
- username: `postgres`
- password: `postgres`

Flyway runs automatically on startup, so the schema is created and updated without extra manual steps.

## Why it matters

Customer is a strong reference project because it captures the most common backend service concerns in one compact codebase: clean REST endpoints, validation, persistence, migrations, API errors, and auth. If the goal is to remember how a straightforward Quarkus CRUD service should feel when it is more than just a demo controller, this is the right kind of project.
