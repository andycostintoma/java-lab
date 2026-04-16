# Functional

Functional is a large Java 17 study project focused on functional programming ideas in everyday Java. It starts with core concepts like purity, closures, currying, and lazy evaluation, then moves through functional interfaces, immutability, records, streams, collectors, file processing, and `Optional`-based error handling.

## Learning path

The project is organized as a multi-part progression.

### Part 1: functional basics

The early examples cover:

- pure versus impure functions
- higher-order functions
- function composition
- currying and partial application
- closures
- lazy evaluation and memoization
- lambdas, method references, and custom functional interfaces

### Part 2: functional interfaces

The next section moves into Java's functional interface model with examples around:

- `Function`, `Predicate`, `Consumer`, and `Supplier`
- primitive specializations
- composition and bridging
- default methods and reusable abstractions

### Part 3: immutability

This part shifts into state management and safer data modeling:

- immutable collections
- the `final` keyword
- records and record constructors
- validation and derived state
- copy-style builder and wither patterns

### Part 4: streams

The streams section is one of the biggest parts of the project. It covers:

- stream creation and iteration styles
- mapping, filtering, reduction, and matching
- primitive streams
- collectors and custom collectors
- spliterators and custom spliterators
- file and directory processing with streams

The included `war-and-peace.txt` gives the stream and file-processing examples a real input source instead of synthetic toy data.

### Part 5: optionals and exceptions

The final section focuses on null handling and safer error modeling with:

- `Optional` basics and operators
- stream integration with `Optional`
- null-handling best practices
- checked exceptions in lambda-heavy flows
- treating errors as values where appropriate

## Local workflow

Build the examples with Maven:

```bash
mvn package
```

Most of the value comes from opening and running the small examples individually, since each class isolates one concept or comparison.

## Why it matters

Functional is useful because it treats functional programming in Java as a practical design toolkit rather than a theory exercise. The project connects lambdas, immutability, records, streams, and `Optional` into one coherent path, which makes it a strong reference when writing more expressive Java without abandoning the language's strengths.
