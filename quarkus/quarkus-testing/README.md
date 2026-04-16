# Quarkus Testing

Quarkus Testing is a multi-project lab built around one of the most useful questions in backend development: how do you test behavior that spans more than one service and more than one process? Instead of treating testing as a single-module concern, it builds a small coffee shop system and then exercises it at multiple levels.

## System overview

The lab is centered on three pieces:

- `coffee-shop/` as the main Quarkus service
- `barista/` as a collaborating downstream service
- `system-tests/` as the higher-level verification layer

The main service is not minimal. It pulls in REST endpoints, scheduling, validation, persistence, health checks, metrics, and templating-oriented dependencies. The supporting project and test module then give it something real to talk to and something meaningful to validate.

## Testing depth

What makes the project more serious than a normal sample app is the range of testing tools and execution modes involved:

- JUnit and Quarkus test support
- Mockito and AssertJ
- WireMock-based service simulation
- Awaitility for asynchronous assertions
- Testcontainers for environment-aware testing
- compose files for local end-to-end orchestration

There is also a distinction between the standard local compose setup and the `system-test-local.yml` style of execution, where parts of the system can be replaced with mocks to validate more focused scenarios.

## Local workflow

Build the service artifacts and container images with:

```bash
./build-all.sh
```

Start the composed environment with:

```bash
docker compose up -d
```

The default stack starts:

- PostgreSQL on `5432`
- `coffee-shop` on `8080`
- `barista` on `8081`

Additional compose files are available for system-test-focused setups, including one where `barista` is replaced by a WireMock container.

## Why it matters

Quarkus Testing is valuable because it treats testing as a system design concern, not just a method-level concern. It shows how to combine application code, infrastructure, mocks, containers, and higher-level assertions into one workflow that is much closer to how real service behavior is validated before deployment.
