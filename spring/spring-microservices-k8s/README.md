# Spring Microservices K8s

Spring Microservices K8s is a multi-module Spring system designed for local container orchestration and Kubernetes-style deployment. It combines service discovery, gateway routing, messaging, tracing, and environment-specific configuration in one project.

## Modules

- `eureka-server/`: discovery server
- `apigw/`: API gateway on `8083`
- `customer/`: customer-facing service on `8080`
- `fraud/`: fraud-checking service on `8081`
- `notification/`: notification service on `8082`
- `clients/`: shared client configuration for environment-specific service access
- `amqp/`: shared messaging support

## Supporting platform

Local orchestration includes:

- PostgreSQL
- pgAdmin
- RabbitMQ with management UI
- Zipkin for distributed tracing

## What it demonstrates

- service discovery with Eureka
- gateway-based request routing
- synchronous collaboration between services
- asynchronous messaging through RabbitMQ
- distributed tracing through Zipkin
- profile-based configuration for local, Docker, and Kubernetes environments
- container image workflows with Jib

## Runtime model

The service configuration includes multiple environment variants such as default, Docker, and Kubernetes profiles. That makes the project useful for understanding how a Spring system changes across deployment targets instead of staying limited to a single local setup.

## Running locally

Bring up the shared infrastructure and service containers with:

```bash
docker compose up -d
```

Build the modules with:

```bash
mvn package
```

To run from source instead of containers, keep the shared infrastructure running and start the modules individually from their own directories.

## Suggested approach

If the system feels dense, work through it in layers:

1. start `eureka-server` and `apigw`
2. add `customer` and `fraud`
3. inspect the notification and RabbitMQ flow
4. use Zipkin to trace requests across service boundaries
5. review `k8s/` after the Docker-based local setup is clear
