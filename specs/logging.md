# Logging rules
Project-specific observability rules.
Use this file to define what must be visible during runtime and how noisy logs may be.

## Goals
- Make runs explainable.
- Make failures localizable.
- Keep normal output cheap.

## Levels
- ERROR: failed operation
- WARN: degraded but continued
- INFO: major state or flow change
- DEBUG: detailed diagnosis

## Always log
- startup/shutdown
- user inputs
- mode/state changes
- external I/O start/end
- retries/timeouts
- errors with reason
- timings of key steps
- timestamps for all log entries
- file/function or equivalent code location where useful

## Timing
- Use stable units: ms unless noted.
- Log start, end, duration for long steps.
- Log loop period / latency where relevant.
- Prefer a few meaningful timing points over constant spam.

## Format
- Prefer structured logs.
- Include subsystem tag.
- Include IDs if available.
- Include file/function or equivalent source location where practical.
- Make messages searchable and consistent.

## Rules
- Default level should be INFO or lower cost.
- DEBUG must be easy to disable.
- Do not spam inside tight loops.
- Summarize repeated events.
- Log enough to reconstruct failures without drowning normal runs.
- Error logs should include enough context to reproduce the issue where possible.
- User-facing error text and log-facing error details may differ, but both must be useful.