# Java Lab

Java Lab brings together core language study, reactive programming, messaging, Quarkus services, and Spring applications, with each major project area documented through its own README.

## Core Java

- [`java/async-reactive/`](./java/async-reactive/README.md) covers callbacks, futures, `CompletableFuture`, RxJava, subjects, schedulers, and reactive concurrency.
- [`java/design-patterns/`](./java/design-patterns/README.md) compares classic object-oriented patterns with more functional Java implementations.
- [`java/functional/`](./java/functional/README.md) explores lambdas, higher-order functions, immutability, records, streams, collectors, and `Optional`.
- [`java/multithreading-parallelism/`](./java/multithreading-parallelism/README.md) focuses on synchronization, executors, concurrent collections, fork/join, and parallel streams.

## Kafka

- [`kafka/`](./kafka/README.md) provides the messaging and stream-processing track, from topics and plain Java clients to schema-based messaging and Kafka Streams.

## Quarkus

- [`quarkus/customer/`](./quarkus/customer/README.md) is a compact Quarkus CRUD backend with PostgreSQL, Panache, Flyway, validation, and auth.
- [`quarkus/jakartaee/`](./quarkus/jakartaee/README.md) groups Jakarta EE exercises across GlassFish and Open Liberty.
- [`quarkus/jenkins_tdd/`](./quarkus/jenkins_tdd/README.md) covers testing, TDD, code quality, Cypress, and Jenkins pipeline work.
- [`quarkus/quarkus-demo/`](./quarkus/quarkus-demo/README.md) is a broader Quarkus sandbox mixing REST, Qute, persistence, security, metrics, and external API access.
- [`quarkus/quarkus-microservices/`](./quarkus/quarkus-microservices/README.md) documents the large microservices learning track across testing, reactive systems, security, deployment, resilience, and observability.
- [`quarkus/quarkus-testing/`](./quarkus/quarkus-testing/README.md) focuses on multi-service testing with Quarkus apps, Compose, mocks, and system tests.

## Spring

- [`spring/fullstack-spring-boot/`](./spring/fullstack-spring-boot/README.md) combines a Spring Boot backend and React frontend with JWT auth and PostgreSQL.
- [`spring/quiz-engine/`](./spring/quiz-engine/README.md) covers registration, quiz management, Spring Security, JPA, and PostgreSQL.
- [`spring/rabbitmq-demo/`](./spring/rabbitmq-demo/README.md) demonstrates HTTP-triggered RabbitMQ messaging with simple and JSON flows.
- [`spring/spring-boot-getting-started/`](./spring/spring-boot-getting-started/README.md) is a minimal CRUD student application built on Spring MVC and JPA.
- [`spring/spring-microservices/`](./spring/spring-microservices/README.md) covers Eureka, API Gateway, OpenFeign, and service-to-service Spring microservices.
- [`spring/spring-microservices-k8s/`](./spring/spring-microservices-k8s/README.md) expands that into a larger distributed system with messaging, tracing, and Kubernetes-oriented setup.

## How to use this lab

The top-level README is the map. For actual project details, start with the linked README inside the area you want to study, then work from that project root.

Most Java and Quarkus projects build with Maven, while some Spring and frontend pieces use Gradle or npm in their own directories. The linked READMEs call out the relevant workflow for each project.
