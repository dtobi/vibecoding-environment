# UI guidelines

Project-specific UI rules.
Use this file to define interaction, terminology, layout expectations, and the intended user workflow.

## General

- Default to dark mode if project wants it.
- Use domain terms from `spec/product-language.md`.
- Prefer clear labels over cute labels.
- Prefer clear indicative colors.
- Prefer graphical representations over tables and lists when they communicate better.
- One screen should have one obvious main action.
- Minimize clicks and unnecessary actions.

## Workflow-first rule

- Before implementing UI changes, update the UI workflow documentation first.
- Describe complete user workflows from defined start to end.
- Use a clear start state such as: application freshly opened.
- Include normal flow, key branch points, and likely error flow.
- Prefer fewer clicks, fewer mode changes, and fewer unnecessary confirmations.

## Layout

- Keep primary actions easy to find.
- Keep enough click/tap area.
- Make long panels scrollable.
- Avoid hidden critical actions.
- Group related controls visually.
- Use tables and lists carefully.
- Do not expose unnecessary details.
- Restrict UI to meaningful input and output.

## Text

- Button text should describe the action.
- Errors should say what failed, why it failed if known, and what to do next.
- Use help/tooltips only where confusion is likely.
- Prefer short direct text over marketing wording.
- Keep error text professional, descriptive, and actionable.

## Flow

- Show the next step clearly.
- Show busy/progress states.
- Confirm destructive actions.
- Avoid dead ends without explanation.
- Make common paths short and obvious.

## Data extraction

- Consider when users need to extract data from a table, message, or panel.
- Make copy/export actions easy.
- Avoid forcing users to manually reconstruct important data.
- Prefer clearer presentation that removes the need for extraction where possible.

## Consistency

- Same concept, same word.
- Same action, same color/icon pattern.
- Keep naming aligned with logs and docs.

## Review after UI changes

- After each UI-relevant change, review the UI concept again.
- Re-evaluate arrangement, size, usefulness, and workflow cost of UI elements.
- If the UI concept is unclear, ask focused questions before extending it further.
