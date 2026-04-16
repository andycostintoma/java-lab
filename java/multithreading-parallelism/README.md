# Multithreading Parallelism

Multithreading Parallelism is a Java 17 project that covers both sides of concurrent programming: coordinating threads safely and using parallel computation effectively. It combines classic multithreading topics with higher-level parallelism tools such as executors, concurrent collections, fork/join, and parallel streams.

## What the project covers

The source is split into two broad areas.

### Multithreading fundamentals

The `multithreading/` packages cover:

- thread basics, daemon threads, and priorities
- synchronization with intrinsic locks and `ReentrantLock`
- inter-thread communication with producer-consumer examples
- race conditions and lock behavior
- atomic variables and `volatile`
- deadlock and livelock
- synchronization primitives such as semaphores, latches, barriers, mutex-style coordination, and exchangers
- concurrent collections including blocking queues, delay queues, concurrent maps, priority blocking queues, synchronized collections, and copy-on-write lists
- executor services including fixed, cached, single-thread, and scheduled thread pools
- the dining philosophers problem as a classic coordination case study

### Parallelism and performance

The `parralelism/` packages focus on dividing work across cores:

- sequential versus parallel sum implementations
- sequential versus parallel merge sort
- fork/join tasks and recursive actions
- thread optimization examples
- parallel streams for sorting, summation, prime calculations, and file processing
- direct comparison examples for merge sort and sum performance

The included `war-and-peace.txt` is used as realistic input for some of the file-processing and performance-oriented examples.

## Local workflow

Build the project with Maven:

```bash
mvn package
```

The examples are best explored one class at a time from the IDE so you can watch the behavior of each concurrency primitive or parallel strategy in isolation.

## Why it matters

This project is valuable because it does not treat concurrency as one topic. It separates the correctness side of multithreading from the throughput side of parallelism, then shows where they overlap. That makes it a strong reference for understanding when you are solving a coordination problem, when you are solving a performance problem, and when the two start to interfere with each other.
