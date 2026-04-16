# Spring Microservices

Spring Microservices is a compact Spring Cloud system organized as a Maven multi-module build. It introduces service discovery, gateway routing, and service-to-service collaboration without the heavier deployment concerns of the Kubernetes-oriented variant.

## Modules

- `service-registry/`: Eureka server on `8761`
- `api-gateway/`: Spring Cloud Gateway on `9191`
- `department/`: PostgreSQL-backed department service on `8080`
- `employee/`: PostgreSQL-backed employee service on `8081`

## Request flow

- `service-registry` provides discovery
- `department` and `employee` register with Eureka
- `api-gateway` routes incoming requests to the business services using logical service names
- `employee` includes OpenFeign support for direct service-to-service collaboration

The gateway currently routes:

- `/api/employees/**`
- `/api/departments/**`

## What it demonstrates

- decomposing a system into separate Spring Boot services
- service discovery with Netflix Eureka
- entrypoint routing with Spring Cloud Gateway
- keeping persistence concerns inside individual services
- evolving from a monolith mindset toward service boundaries

## Running locally

Both business services point at a local PostgreSQL instance and use `ddl-auto=update`, so local experimentation is straightforward.

Recommended startup order:

1. Start PostgreSQL
2. Start `service-registry`
3. Start `department`
4. Start `employee`
5. Start `api-gateway`

Build all modules with:

```bash
mvn package
```

Run services from their module directories with `./mvnw spring-boot:run` or `mvn spring-boot:run`.
