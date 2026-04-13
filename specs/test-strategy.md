# Test strategy
Project-specific test rules.
Use this file to define what kinds of tests matter and how much confidence they provide.

## Goals
- Catch regressions early.
- Verify behavior, not implementation trivia.
- Keep tests cheap enough to run often.

## Levels
- unit: logic
- integration: boundaries
- e2e/manual: main flows

## Rules
- Add focused tests for new behavior.
- Add tests for relevant error cases where practical.
- Prefer deterministic tests.
- Avoid brittle timing tests unless required.
- Keep fixtures small.
- Run the smallest useful test first.

## Reality check
- Passing tests reduce risk.
- Passing tests do not prove correctness.
- Missing tests increase regression risk quickly.