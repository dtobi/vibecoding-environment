# Script guidelines

Rules for build/test/flash/helper scripts.
Use scripts to hide noisy tools behind compact agent-friendly commands.

## Goal

Agent-friendly scripts with low-noise output and reliable exit codes.

## Rules

- Success prints one line: `OK: <action>`
- Failure prints short summary first
- Verbose mode only on demand
- Exit codes must be reliable
- Avoid progress spam
- Write artifacts to known paths

## Standard commands

- `scripts/build`
- `scripts/test`
- `scripts/flash`
- `scripts/lint`

## Output contract

- stdout: concise summary
- stderr: actionable errors
- full tool output: only when requested or when needed for diagnosis
