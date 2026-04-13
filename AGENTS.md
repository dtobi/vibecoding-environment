# Purpose

General agent operating rules only.
Keep this file stable and short.
Do not put product facts, target values, UI text, or session notes here.
This file drives the project workflow from discovery to implementation.
Project-specific information belongs in the files listed below.

## Repo layout

General process rules:
- `AGENTS.md`
- `rules/RUNBOOK.md`
- `rules/refactoring-guidelines.md`
- `rules/scripts-guidelines.md`
- `rules/prompts.md`

Project framework and project-specific content:
- `spec/spec.md`
- `spec/architecture.md`
- `spec/current-run.md`
- `spec/logging.md`
- `spec/ui-guidelines.md`
- `spec/product-language.md`
- `spec/test-strategy.md`
- `spec/project-interview-guide.md`

## Workflow order

1. Read `spec/spec.md`.
2. If `spec/spec.md` is missing, weak, or ambiguous, run `spec/project-interview-guide.md` first.
3. Use the interview to create or improve the project files.
4. Read `rules/RUNBOOK.md`.
5. Read `spec/current-run.md`.
6. Read only the relevant domain files.
7. Then implement.

## Read order

1. `spec/spec.md` — product goal, users, constraints, acceptance
2. `spec/project-interview-guide.md` — use if spec is missing or weak
3. `rules/RUNBOOK.md` — how to work in this repo
4. `spec/current-run.md` — current task, plan, risks, next step
5. Domain files only if relevant:
   - `spec/logging.md`
   - `spec/ui-guidelines.md`
   - `spec/product-language.md`
   - `spec/architecture.md`
   - `spec/test-strategy.md`

## Spec rule

- The spec should either be provided by the developer or created in dialogue with the developer.
- Ask for a spec if none exists.
- If only a rough idea exists, use `spec/project-interview-guide.md` to derive a clear project definition.
- Do not start broad implementation while scope, user actions, or expected behavior are unclear.
- Update project files when the agreed scope changes.

## Hard rules

- Plan first for non-trivial work.
- Work in small safe increments.
- After each good increment: verify, document, commit.
- Prefer changing specs/docs over patching symptoms.
- Keep messages to the developer short and descriptive.
- Mark developer actions clearly, for example: `**ACTION REQUIRED:** ...`
- Keep output short. Full logs only on error or request.
- Never assume hidden intent. Use repo docs.
- Keep diffs small and local.
- Preserve behavior unless change is requested.
- Reuse existing project code before writing new code.
- Prefer mature existing library functions over custom generic code.
- Search for fitting libraries before implementing generic helpers.
- Ask before adding any new library or dependency.
- No new deps unless justified in docs.
- No dead code, placeholder code, or silent TODOs.

## Reuse order

Use this order before writing new code:
1. existing repo code
2. standard library / platform SDK
3. already included dependencies
4. proposed new library after asking
5. custom implementation only if needed

## Required loop

1. Read only the docs needed for the task.
2. Write or update the plan in `spec/current-run.md`.
3. Implement one small increment.
4. Run the smallest useful verification.
5. Update affected docs.
6. Remind the developer to commit if the increment is good.

## Git

- Commit often after verified improvements.
- Remind the developer to commit after good verified increments.
- Use clear commit messages that say area and change.
- Read recent git history before risky changes.
- If stuck, quality drops, or context is weak, revert to last good state.
- Prefer many small recoverable commits over large risky edits.

## Build/test output

- Prefer wrappers/scripts with compact output.
- Success output should be one short line.
- Error output should start with a short summary.
- Only show full details when needed to act.

## Logging

- Keep runtime behavior observable.
- Log user input, state changes, timings, retries, and errors.
- Use levels: ERROR, WARN, INFO, DEBUG.
- Default logging must stay cheap enough for normal use.
- Logs should include timestamps and clear code location where useful.
- Error logs should contain enough detail to understand and reproduce the problem.

## Error handling

- Anticipate error cases and implement handling for them.
- When reviewing code, review error cases too.
- When updating code, reflect on possible new or obsolete error cases.
- User-facing errors should state what failed, which conditions led to it, and what to do next if known.
- Keep error messages professional and descriptive.
- Log messages for errors should include function name, relevant parameters, and problematic circumstances where possible.

## Refactoring

- Refactor only with an explicit goal.
- Keep scope narrow and behavior stable.
- Prefer simpler flow, clearer names, fewer branches, and less duplication.
- Verify that refactoring did not break expected behavior.
- When changing code, reflect on new, changed, and obsolete error cases.

## Performance

- Avoid expensive work in hot paths.
- Watch for float ops, blocking calls, deep nesting, repeated allocation, and avoidable polling.
- Avoid busy waiting.
- Be careful with I/O, network requests, waiting for responses, and polling in the main loop or main thread.
- Prefer event-driven or non-blocking designs where practical.
- Document important performance assumptions if they affect design.

## Comments

- Comment intent, invariants, protocol meaning, and non-obvious tradeoffs.
- Do not comment the obvious.
- Keep comments synchronized with behavior.
- Prefer short useful comments over verbose narration.

## UI trigger rule

- Before implementing UI changes, update the UI workflow documentation first.
- Re-evaluate the UI concept after each UI-relevant change.
- Ask focused questions if the UI concept is unclear.

## Completion gate

A task is done only if:
- the requested change exists
- relevant checks pass
- affected docs are updated
- relevant error cases were considered
- `spec/current-run.md` reflects the final state
- changes are ready to be committed
