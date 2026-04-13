# Project spec
Project-specific facts only.
This file defines what the product is, what it should do, and what constraints matter.
Do not put generic workflow rules here.
The spec should either be provided by the developer or developed in dialogue with the developer.
If the spec is missing, weak, or ambiguous, ask focused questions until scope, expected behavior, and actions are clear.

## Spec source
- Provided directly by developer as prompt or document
- Or derived jointly through short focused questions

## Rule
- Ask for a spec if none exists.
- If a rough idea exists, turn it into a clear spec through dialogue.
- Do not start broad implementation while scope or expected actions are unclear.
- Update this file when the agreed scope changes.

## Goal
[Short description of the product or feature goal.]

## Users
[Who uses it and in which context.]

## Non-goals
[What this project intentionally does not solve.]

## Core flows
1. [Main user flow]
2. [Main user flow]
3. [Optional important edge flow]

## Constraints
- Platform: [target OS / MCU / board / browser]
- Language/runtime: [e.g. C++20, TS, ESP-IDF]
- Size/speed limits: [RAM, flash, latency, CPU budget]
- Safety/security limits: [if relevant]
- Power or hardware limits: [if relevant]

## External interfaces
- Inputs: [buttons, files, API, serial, network]
- Outputs: [UI, logs, actuator, USB, files]
- Protocols/formats: [if any]

## Acceptance
- [Observable success condition]
- [Observable success condition]
- [Relevant failure behavior if needed]