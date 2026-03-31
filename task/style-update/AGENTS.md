# Style Update

Use this task to update repository guidance from user instructions, current guidance, examples, repository self-updates, or `reference/`.
For repository self-updates, current guidance is both source and target.
`reference/` is private evidence, not guidance, until accepted traits are integrated into owning files.

## Owners

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global writing principles, source boundaries, and Markdown conventions.
* `common/LANGUAGE.md`: shared word choice and sentence guidance.
* `common/CHECKLIST.md`: shared final checks.
* `task/<task>/*.md`: task-specific guidance and workflows.
* `adapter/`: setup prompts and shared skill packaging for tools that should read this repository.
* `reference/`: private evidence and license notice.

## Routing

* Put each accepted trait in the narrowest owner.
* Use `STYLE.md` or `common/*.md` only for traits that should apply across tasks.
* Use `task/<task>/` for task-specific audience, genre, artifact, workflow, rubric, prompt, or checklist guidance.
* For `reference/<task>/`, target the matching `task/<task>/` first.
* Do not use one `reference/<task>/` directory to update another `task/<task>/` unless the user names that target.
* Promote a reference trait to shared guidance only when direct instruction, repeated evidence, or current guidance supports it.

## Workflow

* Name the affected repository boundary, style layer, or `<task>`.
* Identify the source: user instruction, current guidance, examples, repository self-update, root `reference/`, or `reference/<task>/`.
* Read the current files that could own the update.
  For a task target, read matching `task/<task>/` files when present, plus `STYLE.md`, relevant `common/*.md`, and the source material.
* Separate direct instruction, current guidance, evidence, and inferred traits.
* Identify conflicts, duplication, stale routing, and unclear ownership.
* Keep only durable traits that can guide future work.
* Keep private facts, names, data, project details, and protected wording out of reusable guidance, skill files, and adapters.
* Edit only files whose roles own accepted traits.
* Remove repeated or stale rules from less appropriate files.
* Refresh affected adapters when reusable style, source boundaries, or loading rules change.
* Keep adapters profile-neutral and focused on current writing style, repository loading, and intended use.
* For broad rewrites, repeat read, edit, and check passes until another pass would only be cosmetic.
* Use `REPORT.md` only when the update needs a structured report or the user asks for one.

## Decisions

* Follow `STYLE.md` source boundaries.
* Prefer explicit user direction over inference from examples.
* Prefer durable, broadly useful guidance over source-specific habits.
* Treat protected sources as high-level influence unless the user provides permission or a short excerpt.
* Keep fewer, stronger rules instead of cataloging every observed habit.
* Preserve uncertainty in the report instead of inventing rules.
* Do not add files unless the new file has a distinct role.
* Do not describe unused paths or rewrite unrelated guidance to match an older structure.
