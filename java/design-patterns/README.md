# Design Patterns

Design Patterns is a Java 17 project for revisiting classic object-oriented patterns and comparing them with more functional alternatives. It is less about framework integration and more about implementation style, tradeoffs, and the shape of the code itself.

## What the project covers

The source is split across two main themes.

The first theme is direct pattern comparison:

- `FactoryOOP` and `FactoryFP`
- `StrategyOOP` and `StrategyFP`
- `BuilderOOP` and `BuilderFP`
- `CommandOOP` and `CommandFP`
- `DecoratorOOP` and `DecoratorFP`

That side-by-side structure is the strongest part of the project. It lets you compare how the same design goal changes when you lean on interfaces, inheritance, and classical object collaboration versus lambdas, higher-order functions, and a more functional style.

The second theme is SOLID-oriented design under `solid/shapes/`, with examples such as:

- `Shape`, `Rectangle`, and `TextBox`
- `Graphics` and `ConsoleGraphics`
- `Shapes` and `ShapesDemo`

Those classes give the project a more general design dimension beyond named GoF patterns.

## Local workflow

Build the project with Maven:

```bash
mvn package
```

Most of the examples are small runnable classes, so the easiest way to explore them is by launching individual demos from the IDE and comparing the OOP and FP variants side by side.

## Why it matters

Design pattern discussions often stay abstract. This project is useful because it makes the tradeoffs concrete in code. It shows where the classic patterns still fit naturally, and where Java's functional features can reduce ceremony or change the design entirely. That makes it a good reference when you want to think about design patterns as implementation choices rather than memorized definitions.
