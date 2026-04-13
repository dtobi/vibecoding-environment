# Standard prompts

Short reusable task starters.
Use them to keep prompting compact and consistent.

## Interview

Run `spec/project-interview-guide.md`. Keep the interview short. Infer defaults where possible. At the end, draft the project files and list only important open questions.

## Plan

Read `AGENTS.md`, `spec/spec.md`, `spec/current-run.md`. Do not code yet. Write a short plan, risks, files in scope, and checks.

## Implement

Implement only the next planned step. Keep diff small. Run the smallest useful verification. Update `spec/current-run.md`. Remind the developer to commit if checks pass.

## Bugfix

Find the root cause, not just the symptom. Check whether `spec/spec.md` or related docs are weak. Update docs first if needed, then patch. Keep the fix minimal. Verify the affected behavior.

## Refactor

Refactor only the named files. Goal: [goal]. Preserve behavior. No new deps. Verify with focused checks. Summarize simplifications.

## Perf review

Review the named files for hot-path cost, blocking calls, float usage, repeated allocation, and deep nesting. Mark each suggestion as safe, likely safe, or needs measurement.

## UI review

Review UI text and flow against `spec/ui-guidelines.md` and `spec/product-language.md`. Suggest only concrete wording/layout improvements.

## Logging review

Review whether user inputs, state changes, errors, and timings are observable without noisy logs. Suggest concise improvements only.
