# Quarkus Demo

Quarkus Demo is a broader application sandbox that pulls together several parts of the Quarkus platform in one place. Instead of stopping at a single REST endpoint, it mixes API work, HTML rendering, persistence, auth, metrics, scheduled behavior, and external integrations so the project feels closer to a real application slice.

## What the project does

The app spans multiple interaction styles:

- a simple `hello` endpoint for basic API wiring
- customer APIs and UI flows for create and listing behavior
- country lookup resources backed by a REST client
- server-rendered pages such as `create.html` and `customers.html`
- SSE-style customer streaming endpoints under `customers/sse`

That mix makes the project more than a CRUD example. It works as a tour through different Quarkus capabilities living together in the same codebase.

## Technical focus

The project pulls in a wider range of Quarkus features than the smaller examples:

- RESTEasy Reactive for APIs
- Qute for HTML rendering
- PostgreSQL, Panache, and Flyway for persistence
- REST client integration for external country data
- scheduler support
- health checks and Prometheus metrics
- reactive messaging dependencies
- security with file-based users and roles
- YAML-based configuration and environment overrides

The `application.yml` also shows a useful split between default container-oriented settings and `%dev` overrides, which makes it a good example of how local development and container deployment config can coexist cleanly.

## Supporting infrastructure

The included `docker-compose.yml` starts:

- PostgreSQL as `customerdb`
- Prometheus for metrics scraping on port `9090`

This gives the project a monitoring angle in addition to the usual persistence setup.

## Local development

Start the supporting services first:

```bash
docker compose up -d
```

Run the application in dev mode:

```bash
./mvnw quarkus:dev
```

In development, the datasource points to `localhost:5432`. Outside the `%dev` profile, the configuration expects the database hostname `customerdb`, which matches the compose setup.

## Why it matters

Quarkus Demo is valuable because it shows how a Quarkus codebase starts to look once it grows beyond one endpoint and one datasource. It brings together UI, APIs, persistence, security, monitoring, and external service access in a way that makes it useful as a reusable reference project, not just a one-off lab.
