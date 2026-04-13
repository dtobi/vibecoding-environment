# Refactoring rules

General change-discipline for cleanup work.
Use this file when simplifying code without changing intended behavior.

## Allowed goals

- simplify control flow
- reduce duplication
- improve naming
- isolate side effects
- reduce hot-path cost

## Must preserve

- external behavior
- public interfaces unless planned
- logging needed for diagnosis

## Process

1. state goal
2. define scope
3. refactor small
4. verify
5. commit

## Smells to target

- long functions
- repeated logic
- hidden state changes
- mixed abstraction levels
- blocking work in critical paths
- busy waiting
- unsafe shared mutable state
- long lock hold times
