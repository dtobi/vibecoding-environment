# Agent runbook

How to work in this repo.
This file defines process, not product facts.
Use it to keep sessions stable, small, and recoverable.

## Session start

1. Read `AGENTS.md` and `spec/spec.md`.
2. If `spec/spec.md` is missing, weak, or ambiguous, run `spec/project-interview-guide.md` and improve the spec before broad implementation.
3. Read `spec/current-run.md`.
4. Read only relevant domain docs.
5. Inspect git status and recent commits.
6. Restate the task in 3-7 bullets before large edits.

## Discovery mode

- Use `spec/project-interview-guide.md` before coding if the project is not clearly defined.
- Keep the interview short.
- Infer reasonable defaults where possible.
- Ask follow-up questions only when answers are vague, contradictory, or open an important branch.
- After the interview, draft or update the project files before implementation.

## Change strategy

- Prefer one small change per step.
- Prefer design fixes over symptom fixes.
- For bugs: find root cause, improve docs/spec if needed, then patch.
- For broad work: split into phases and finish one phase at a time.

## Verification strategy

Run the smallest useful check first:
1. lint / format
2. typecheck / compile
3. focused tests
4. integration or full tests only when needed
5. runtime/manual checks only when needed

## Output rules

- Keep messages to the developer short and descriptive.
- Summarize first.
- Quote only the lines needed to act.
- Avoid flooding context with raw logs.
- Mark developer actions clearly, for example: `**ACTION REQUIRED:** ...`

## Commit policy

Commit after each verified improvement.

Template:
- `<area>: <change>`

Examples:
- `ui: clarify device pairing flow`
- `firmware: reduce debounce CPU cost`
- `build: add quiet flash wrapper`

## Stuck policy

If two attempts fail:
1. stop patching
2. write current hypothesis in `spec/current-run.md`
3. inspect logs/tests/git history
4. revert to last good state if needed
5. choose a smaller next step

## Doc policy

Update docs when behavior, architecture, UI text, logs, assumptions, or test strategy change.
Keep docs concise, current, and useful for the next session.
