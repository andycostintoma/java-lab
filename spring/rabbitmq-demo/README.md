# RabbitMQ Demo

RabbitMQ Demo is a Spring Boot messaging project that combines HTTP endpoints with asynchronous RabbitMQ publishing and consumption. It is designed to show how Spring AMQP fits into a small application without the overhead of a larger distributed system.

## Core capabilities

- publishing messages to exchanges
- consuming messages from queues
- demonstrating both simple and JSON-based message flows
- triggering messaging behavior through controller endpoints

The main HTTP entry points are:

- `SimpleMessageController`
- `JsomMessageController`

## Messaging model

The application defines two main queue/exchange flows:

- `demo-queue` via `demo-exchange`
- `json-queue` via `json-exchange`

RabbitMQ is expected to be available at:

- host `localhost`
- port `5672`
- username `guest`
- password `guest`

## Tech stack

- Spring Boot 3
- Spring Web
- Spring AMQP
- RabbitMQ
- Maven

## What it demonstrates

- wiring producers and consumers with Spring AMQP
- understanding routing keys, exchanges, and queue bindings
- exposing a simple HTTP-to-message bridge for local experiments

## Running locally

Start RabbitMQ first, then run the application:

```bash
./mvnw spring-boot:run
```

Run tests with:

```bash
./mvnw test
```
