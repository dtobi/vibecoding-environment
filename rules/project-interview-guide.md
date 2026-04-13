# Project interview guide

Use this before coding starts.
Its job is to turn an idea into clear project-specific documents.
Keep the interview short.
Infer as much as possible from the answers.
Do not ask implementation-specific technical detail unless it is required to define the project.

## Purpose

* discover the project scope
* clarify user intent and expected workflows
* define basic project parameters
* uncover UI expectations, naming, and misuse cases
* gather enough information to create or update:

  * `spec.md`
  * `ui-guidelines.md`
  * `product-language.md`
  * `logging.md` only if needed by the project

## Interview rules

* Ask short focused questions.
* Ask only for information needed to define the project.
* Infer reasonable defaults where possible.
* Ask follow-up questions only when an answer is vague, contradictory, or opens an important branch.
* Do not ask deep implementation questions the AI can decide later from general coding rules.
* Summarize findings and ask for confirmation.

## Output of the interview

At the end, produce:

1. a concise project summary
2. draft content for the relevant project-specific md files
3. a short list of open questions only if needed
4. a short list of assumptions made by the AI

## Interview flow

1. Project intent
2. Users and usage context
3. Main workflows
4. Basic technical frame
5. UI and interaction model
6. Misuse and expected user errors
7. Final gap check

## 1. Project intent

Ask:

* What is the project?
* What should it do?
* What should the user be able to do with it?
* What is the main value of the project?
* What is out of scope?

Follow up if needed:

* Is this a tool, app, device, script, service, or prototype?
* What would a first useful version look like?

Target files:

* `spec.md`

## 2. Users and usage context

Ask:

* Who is the user?
* In which context do they use it?
* What do they already know?
* What misunderstandings or mistakes are likely?

Follow up if needed:

* Is there one user type or more than one?
* Is the user a developer, operator, student, end user, or admin?

Target files:

* `spec.md`
* `product-language.md`
* `ui-guidelines.md`

## 3. Main workflows

Ask:

* Describe the main workflows from start to finish.
* What does the user do first?
* What are the common repeated actions?
* What counts as success?

Follow up if needed:

* Which steps are optional?
* Which workflows are most important?
* Which workflows are confusing or error-prone?

Output requirement:

* Write complete high-level workflows with clear start and end.
* Minimize clicks and unnecessary actions.

Target files:

* `spec.md`
* `ui-guidelines.md`

## 4. Basic technical frame

Ask only the minimum needed:

* What kind of project is it technically: web app, desktop app, firmware, script, backend, device, or other?
* Are there required languages, platforms, environments, or protocols?
* Are there existing libraries, APIs, or systems that must be used?

Follow up if needed:

* Ask only if the answer changes project scope or structure.

Target files:

* `spec.md`

## 5. UI and interaction model

Ask:

* What kind of user experience do you want?
* Should the UI be guided, expert-focused, minimal, graphical, form-based, or mostly automatic?
* Should changes apply immediately or only after save/commit?
* What are the main screens, dialogs, or areas called?
* Which data should be graphical, tabular, textual, copyable, or exportable?

Follow up if needed:

* What should the user see immediately after opening the app?
* What should be visible at a glance?
* What should stay hidden unless needed?
* Are there language or tone requirements?

Target files:

* `ui-guidelines.md`
* `product-language.md`
* `spec.md`

## 6. Misuse and expected user errors

Ask:

* What wrong use can you already anticipate?
* What user errors are likely?
* Which mistakes should be prevented, explained, or recoverable?
* What should the user be told when something goes wrong?

Follow up if needed:

* Which wrong actions are harmless and which are serious?
* What remediation should be suggested to the user?

Target files:

* `spec.md`
* `ui-guidelines.md`
* `logging.md` only if the project needs explicit runtime diagnostics

## 7. Final gap check

Ask:

* What is still unclear?
* Which names, workflows, or expectations are still provisional?
* Do we have enough detail to draft the project-specific files?

## Final deliverable template

Produce:

* Project summary
* Draft `spec.md`
* Draft `ui-guidelines.md`
* Draft `product-language.md`
* Draft `logging.md` only if needed
* Open questions
* Assumptions

## Starter prompt for the interview

Use this to start:

"We will first define the project clearly before coding.
I will ask a small number of focused questions.
Please answer concretely and use examples where helpful.
I will infer reasonable defaults where possible.
At the end I will draft the project-specific markdown files and list only the remaining important open questions."
