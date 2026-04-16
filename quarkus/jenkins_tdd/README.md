# Jenkins And TDD Labs

Jenkins And TDD Labs is a delivery-focused training track built around testing discipline, feedback loops, and automation. It is not just about writing a few tests around a service. The material moves from unit tests to integration tests, then into functional checks, quality analysis, multi-service review exercises, and finally Jenkins pipeline setup.

## Learning path

- `01-unit-testing/` focuses on small-scope Quarkus tests and isolated behavior
- `02-integration-testing/` shifts into service integration and higher-confidence backend checks
- `03-functional-testing/` uses a React scoreboard app with Cypress to cover browser-level behavior
- `04-testing-review/` introduces a multi-service setup with `adder`, `multiplier`, and `solver`
- `05-tdd-introduction/` and `07-tdd-review/` focus on TDD practice and reinforcing the red-green-refactor loop
- `06-analyze-code-quality/` introduces code quality tooling and review-oriented feedback
- `08-jenkinsfile/` moves into Jenkins and GitHub pipeline integration

## Why this track is stronger than a normal test folder

What makes this set more substantial is the range of concerns it covers:

- isolated business logic testing
- integration testing of service behavior
- end-to-end style browser testing
- multi-service collaboration in review exercises
- automated quality gates
- CI workflow thinking through Jenkins pipelines

That gives the folder a real progression. It mirrors how confidence in software grows in practice: not from one test type, but from layered validation.

## Local workflow

Most backend exercises are Quarkus Maven projects and can be worked on with commands like:

```bash
./mvnw test
./mvnw quarkus:dev
```

The frontend exercise in `03-functional-testing/` uses Node, npm, and Cypress:

```bash
npm install
npm start
npm run cy:open
```

The Jenkins section in `08-jenkinsfile/` is more infrastructure-oriented and is aimed at wiring GitHub activity into Jenkins jobs and stage-based pipelines.

## Why it matters

This lab is useful because it teaches the full testing and automation story instead of freezing at unit tests. It gives you examples of how quality work scales from one method, to one service, to a small system, and then into a CI pipeline that can enforce that quality automatically.
