# Kafka Labs

Kafka Labs is a progression of messaging and stream-processing projects that builds up from the broker itself to client applications, then into Quarkus-based messaging, schema-aware pipelines, and Kafka Streams. It reads like a learning path rather than a random bag of demos, which is what gives it weight.

## Track outline

- `01-kafka-topics/` focuses on topic setup and partitioning behavior
- `02-kafka-producers/` introduces producers in both plain Java and Quarkus
- `03-kafka-consumers/` does the same on the consumer side
- `04-kafka-schemas/` brings in schema-aware messaging with Apicurio Registry and Avro
- `05-kafka-basics/` contains the `energy-meter` plain Java client example
- `06-streams-interaction/` moves into Kafka Streams with Quarkus
- `07-streams-data/` extends that into the `vehicles` streams application

## Why the track feels substantial

The folder deliberately mixes different levels of abstraction instead of forcing everything through one framework:

- topic-focused scenario folders for understanding broker behavior first
- plain Java clients built with `kafka-clients` and shaded jars
- Quarkus projects using reactive messaging
- stream-processing apps using `quarkus-kafka-streams`
- schema-oriented projects using registry-backed serialization
- multi-module builds such as `02-kafka-producers/plain`, where producer and viewer roles are separated cleanly

That structure matters because it teaches Kafka in layers. You learn what the broker is doing, then what the client code is doing, then how frameworks like Quarkus simplify those patterns.

## Representative projects

Some of the more illustrative pieces in the track are:

- `02-kafka-producers/plain/` as a Maven reactor around `producer` and `viewer`
- `02-kafka-producers/quarkus/` for framework-backed producer development
- `03-kafka-consumers/plain/` and `03-kafka-consumers/quarkus/` for the same contrast on the consuming side
- `04-kafka-schemas/` as the point where message contracts become explicit
- `05-kafka-basics/energy-meter/` as a lightweight plain client example
- `06-streams-interaction/` and `07-streams-data/` as the transition into stream processing

## Local workflow

The working style depends on the project type.

Quarkus-based projects typically use:

```bash
./mvnw quarkus:dev
```

Plain Java client projects generally package runnable jars with Maven:

```bash
mvn package
```

Some folders are less about one application and more about exercising Kafka concepts directly, especially the topic-oriented material at the start of the track.

## Why it matters

Kafka Labs is useful because it does not skip the fundamentals. It starts close to the broker, then grows into producers, consumers, schemas, and streams. That makes it a better learning path than a framework-only introduction, because the abstractions come after the underlying messaging model is already visible.
