# Async Reactive

Async Reactive is a broad Java 17 playground for asynchronous and reactive programming. It starts with the lower-level building blocks of callbacks, callables, futures, and `CompletableFuture`, then moves into a much larger RxJava section that explores observables, operators, multicasting, subjects, scheduling, and concurrency.

## What the project covers

The material is organized as a progression rather than a single app:

- `basics/` for callback, callable, and future-based examples
- `completable_futures/` for creation, composition, coordination, exception handling, timeouts, and async versus sync execution
- `rxjava/` for a large set of focused RxJava examples

Inside the RxJava section, the project goes well beyond the intro material. The packages cover:

- observable and observer basics
- factory methods and stream creation
- `Single`, `Maybe`, and `Completable`
- disposal and subscription lifecycle management
- transforming, suppressing, reducing, and collecting operators
- combining observables with `zip`, `merge`, `concat`, `flatMap`, and related operators
- multicasting, replaying, caching, and sharing
- subjects such as `PublishSubject`, `BehaviorSubject`, `ReplaySubject`, `AsyncSubject`, and `UnicastSubject`
- concurrency and scheduler behavior, including computation, single-thread, and new-thread schedulers

## Why it feels substantial

This is not just a small RxJava demo project. It captures the transition from classic asynchronous Java techniques to more composable reactive flows. That makes it useful both as a learning path and as a reference shelf when you want to quickly remember how a specific operator or scheduling pattern behaves.

## Companion TypeScript workspace

The project also includes a `typescript/` subproject with local TypeScript tooling via `typescript` and `ts-node`. That companion area makes sense in the context of reactive and async learning because it gives you a place to contrast Java patterns with the equivalent JavaScript or TypeScript event-driven style.

## Local workflow

Build the Java examples from the project root with Maven:

```bash
mvn package
```

Run individual demo classes from your IDE or preferred Java runner.

For the TypeScript companion workspace:

```bash
cd typescript
npm install
```

## Why it matters

Async Reactive is valuable because it keeps several generations of Java async thinking in one place. You can move from futures, to `CompletableFuture`, to RxJava streams and schedulers without switching repositories or mental context. That makes it a strong reference project for understanding how asynchronous composition in Java gets progressively more expressive.
