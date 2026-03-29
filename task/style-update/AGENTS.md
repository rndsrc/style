# Style Update

Use this task to turn endorsed writing samples into durable style
guidance that an LLM can load before drafting, rewriting, reviewing,
or explaining work.

Inputs usually live under `reference/<task>/`, but the user may also
provide examples, notes, or direct instructions in the current
session.
Outputs are edits to the current canonical guidance files for the
affected task.

The goal is not to imitate every reference.
The goal is to infer currently endorsed style traits, decide which
ones are durable enough to keep, and express them as concise guidance.

## Workflow

* Name the affected `<task>` before editing.
* Read the current canonical guidance that could apply to that task.
* Read the endorsed references or user-provided examples for the task.
* Separate explicit user direction from inferred traits.
* Identify conflicts between references, current guidance, and user
  direction.
* Choose the narrowest useful destination for each accepted trait.
* Edit only guidance that the accepted traits actually affect.
* Use `REPORT.md` to summarize sources, decisions, changes, limits,
  and validation.

## Decision Rules

* Treat references as evidence, not authority.
* Prefer explicit user direction over inference from examples.
* Prefer newer endorsed references over older references when they
  conflict.
* Prefer a task-specific rule when a trait applies only to one task.
* Use shared or global guidance only when a trait applies across
  tasks.
* Keep fewer, stronger rules rather than cataloging every observed
  habit.
* Preserve uncertainty in the report instead of inventing a rule.
* Leave existing guidance alone when the evidence is weak or one-off.

## Boundaries

* Do not copy long passages from references into guidance files.
* Do not preserve identifying facts from private examples.
* Do not turn project details, names, data, or temporary circumstances
  into style rules.
* Do not promote every observed habit into a rule.
* Do not treat source samples as endorsed unless the user or
  maintainer says they are.
* Do not add new files for prompts, examples, or templates unless the
  workflow has a concrete repeated need for them.
* Do not rewrite unrelated guidance just to make the repository match
  an older description.
