# Vibe Coding Guidelines and Framework

This repository provides a reusable, model-agnostic framework for guiding AI-assisted software development in a strict **100% vibe-coding** workflow.

The purpose of these files is to improve the quality, consistency, and maintainability of AI-generated software by structuring how the AI gathers requirements, interprets project intent, documents decisions, and performs implementation work. The contents of these files are based both on practical experience and on sound software engineering and development standards.

The framework is intentionally designed without relying on vendor-specific or model-specific features. It should therefore be suitable for a wide range of projects and usable with many different AI systems and development environments.

Suggestions for extending, simplifying, or reducing these files are welcome. Additional prompts and improvements to the workflow are also welcome.

## General Idea

The framework separates:

- **stable, reusable process rules** from
- **project-specific and evolving specifications**

This is intended to keep the AI context clean, reusable, and efficient, while still allowing each project to define its own scope, workflows, terminology, UI expectations, and constraints.

## Structure

The AI should begin by reading **`AGENTS.md`**.

This file acts as the main entry point and defines the overall workflow, including when to gather requirements, when to read project documents, and how implementation should proceed.

For project setup, the repository also contains **`README-project-setup.md`**, which may likewise be read and processed by the AI.

### `rules/`
The `rules/` directory contains **static and reusable rules**. These files are intended to remain broadly applicable across many projects and should only change when the general framework itself is improved.

Typical contents include:
- workflow and runbook rules
- refactoring guidance
- script and tool output conventions
- reusable prompt templates

### `spec/`
The `spec/` directory contains **more dynamic project-facing documents**. These files are expected to be adapted for the specific project and to evolve during the course of development.

Typical contents include:
- the project specification
- architecture notes
- current run state
- logging expectations
- UI guidance
- project terminology
- test strategy
- project interview guide

## Project Interview Guide

The **Project Interview Guide** supports the initial setup of a project by asking structured questions that help the AI understand the project correctly before implementation begins.

Its purpose is to guide the AI in identifying:

- the actual project goal
- the relevant users and user groups
- important workflows and use cases
- naming and terminology
- UI expectations
- likely misuse and user error cases
- the minimum technical framing needed to start correctly

This helps the AI begin the project on a sound basis and make better decisions regarding users, use cases, and technical direction.

## Intended Use

1. Start with **`AGENTS.md`**.
2. If the project is not yet clearly specified, use the **Project Interview Guide**.
3. Create or refine the project-specific files in `spec/`.
4. Proceed with implementation using the reusable rules from `rules/`.
5. Update the project-facing files as the project evolves.

## Contribution

Contributions, corrections, reductions, extensions, and additional prompts are explicitly welcome.

The framework is meant to remain practical, concise, and broadly reusable.

## Warning and Disclaimer

It is discouraged to use 100% vibe coding for important commercial projects, for projects with safety concerns, and for other projects where people rely on the correct function of the code. Keep in mind that this framework is intended for experimentation purposes, and that you use these rules at your own discretion. Before trusting code produced by AI, conduct an appropriate security and functionality review. You use this code and the results that AI generates based on these files at your own risk.

