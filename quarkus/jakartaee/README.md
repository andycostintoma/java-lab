# Jakarta EE Labs

Jakarta EE Labs is a grouped set of small applications that drills into the core Jakarta EE building blocks without hiding them inside a larger framework. Rather than presenting one giant project, it breaks the material into targeted examples so each topic stays visible on its own.

## What the lab covers

The projects span several fundamental areas:

- JSON handling in `json/`
- CDI basics in both `openliberty/cdi/` and `glassfish/cdi/`
- servlet development in both `openliberty/servlet/` and `glassfish/servlet/`
- REST work in `openliberty/rest/rest-sync/`
- persistence-oriented examples under both runtimes, including `customer` and `school-tbd`

The important part is not just the topics themselves, but the side-by-side runtime perspective. Similar concepts are exercised under both GlassFish and Open Liberty, which makes it easier to separate Jakarta EE concepts from server-specific setup.

## Project shape

Each subproject is an independent Maven application. That keeps the lab modular:

- one folder, one concept, one deployable unit
- minimal cross-project coupling
- easy comparison between runtimes
- easier debugging when learning CDI, servlet, REST, or persistence behavior

This makes the lab useful as a reference shelf. If the goal is to remember how a servlet example is wired versus a CDI example, the answers are kept close to the concept instead of being buried in a broader system.

## Local workflow

Work from the specific exercise root you want to run or package, for example:

```bash
mvn package
```

From there, the resulting artifact can be run or deployed in the environment expected by that example. Some folders are pure code exercises, while others are better thought of as deployment-oriented samples for a chosen app server.

## Why it matters

Jakarta EE Labs is valuable because it keeps the classic Java enterprise programming model legible. CDI, servlets, REST resources, JSON handling, and persistence are all here in a stripped-down form, which makes the directory a useful bridge between older Java EE style development and the newer framework-heavy approach many developers learn first.
