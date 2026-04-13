# How to use these files

This template separates stable operating rules from project facts and temporary run state.
Keep that separation strict so context stays clean and efficient.

## General vs project-specific

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

## Keep separate

- Do not put product facts in `AGENTS.md`.
- Do not put workflow rules in `spec/spec.md`.
- Do not turn `spec/current-run.md` into a diary.
- Do not duplicate the same rule across many files.
- Put user workflow descriptions for the UI into `spec/ui-guidelines.md` or a dedicated UI workflow file.

## Minimal update rules

- Permanent rule change -> `AGENTS.md` or file in `rules/`
- Product behavior change -> `spec/spec.md`
- Architecture change -> `spec/architecture.md`
- Session progress -> `spec/current-run.md`
- UI wording/style change -> `spec/ui-guidelines.md` or `spec/product-language.md`
- Observability change -> `spec/logging.md`
- Test scope/confidence change -> `spec/test-strategy.md`
- Project discovery / requirement interview -> `spec/project-interview-guide.md`
