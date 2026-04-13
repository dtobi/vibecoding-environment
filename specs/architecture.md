# Architecture
Project-specific technical structure.
Use this file to explain how the system is split and where responsibilities belong.
Do not put temporary session notes here.

## Main parts
- [module]: [purpose]
- [module]: [purpose]
- [module]: [purpose]

## Boundaries
- [layer/module] must not depend on [layer/module]
- [module] owns [state/resource]
- [module] is the only entry point for [capability]

## Data flow
1. [source]
2. [processing]
3. [sink]

## Invariants
- [must always hold]
- [must always hold]
- Shared state must stay consistent across concurrent access.
- Long-running work must not stall critical control flow without explicit design.

## Tradeoffs
- [choice] because [reason]
- [choice] accepted despite [cost]

## Concurrency and blocking
- Avoid blocking work in main loop or main thread.
- Avoid busy waiting and unnecessary polling.
- Be careful with shared mutable state.
- Prefer designs that reduce lock contention by ownership, message passing, queues, snapshots, or staged updates.
- If locks or mutexes are required, keep scope and hold time small.
- Do not leave data in inconsistent intermediate states visible to other code.

## Change notes
- Keep interfaces stable unless spec requires change.
- Prefer additive changes before breaking changes.
- Document architectural changes here when they affect future work.