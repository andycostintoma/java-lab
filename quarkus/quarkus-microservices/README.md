# Quarkus Microservices

Quarkus Microservices is one of the biggest systems-oriented tracks in Java Lab. It is organized as numbered labs, but the overall arc is much more ambitious than a sequence of isolated demos. The material walks through how distributed Java services evolve from simple endpoints into systems that must be reactive, secure, deployable, resilient, and observable.

## What the track covers

The lesson flow is broad and intentionally staged:

- `01` to `05` cover configuration, REST development, persistence, native packaging, and review work
- `06` to `09` move into testing and multi-service review scenarios
- `10` to `13` shift into reactive architecture and event-driven design
- `14` to `16` cover security topics such as JWT and SSO
- `17` to `20` focus on deployment-oriented workflows
- `21` to `23` add resilience, fault tolerance, and health concerns
- `24` to `26` focus on logging, metrics, and tracing

What makes the track feel substantial is that those concerns are not described abstractly. They show up as working service modules and multi-project lesson roots.

## Project shape

Some lessons are single-service exercises. Others are mini-systems made of several collaborating apps. Representative examples include:

- `02-develop-rest/` with `expense-client` and `expense-service`
- `09-test-review/` with `schedule`, `session`, and `speaker`
- `10-reactive-architecture/` with `prices` and `products`
- `12-reactive-eda/` with `fraud-detector` and `red-hat-bank`
- `20-deploy-review/` with multiple review services
- `23-tolerance-review/` as an aggregator over `session` and `speaker`
- `26-monitor-trace/` with `adder`, `multiplier`, and `solver`

That means the directory is not just about writing Quarkus services. It is about understanding how service boundaries, cross-service communication, deployment concerns, and operational visibility change the way those services are built.

## Local workflow

Each lesson should be treated as its own working area. Most modules use the standard Quarkus dev loop:

```bash
./mvnw quarkus:dev
```

From there, the exact workflow depends on the lesson. Some projects are self-contained, while others assume supporting infrastructure, multiple service processes, containerization, or platform tooling such as OpenShift.

## Why it matters

This track is valuable because it captures the full lifecycle of microservice work. It starts with service construction, but it does not stop there. It keeps going into testing strategy, reactive messaging, security, deployment mechanics, fault tolerance, health checks, logging, metrics, and tracing. In other words, it treats microservices as operating systems problems as much as application code problems, which is what makes the material feel real.
