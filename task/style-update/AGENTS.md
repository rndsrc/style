# Style Update

Use this task to update repository guidance from direct instruction, current guidance, examples, repository self-updates, or `reference/`.
For repository self-updates, current guidance is both source and target.
References are indirect evidence.
They become guidance only after integration into owning repository files.

## Owner Map

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global writing principles, source boundaries, and Markdown conventions.
* `common/LANGUAGE.md`: shared word choice and sentence guidance.
* `common/CHECKLIST.md`: shared final checks.
* `task/<task>/*.md`: task-specific guidance or workflows.
* `adapter/generic-llm.md`: derived prompt for tools that cannot read this repository.
* `reference/`: private evidence and license notice.

## Style Targets

For reference-driven style updates, use these targets:

* Update `STYLE.md` for repository-wide principles, source boundaries, or Markdown conventions.
* Update `common/LANGUAGE.md` for shared word choice, sentence shape, and prose mechanics.
* Update `common/CHECKLIST.md` for shared final checks that apply across writing tasks.
* Update `task/<task>/*.md` for audience, genre, artifact, workflow, rubric, prompt, or checklist guidance that belongs to one task.
* Do not promote a trait from one task reference into `STYLE.md` or `common/*.md` unless direct instruction, repeated evidence, or current guidance supports that broader scope.

## Reference Routing

Route reference material by path before extracting traits:

* Treat root `reference/` material as shared evidence only when the user names no narrower task.
* Treat `reference/<task>/` as evidence for `task/<task>/`.
* Target `task/<task>/` first for every trait from `reference/<task>/`.
* Update an existing `task/<task>/` file when it owns the accepted trait.
* Create a new `task/<task>/` file only when accepted task-specific guidance has a distinct role that reduces duplication.
* Defer or report task-specific traits when no useful task file should be created.
* Process multiple `reference/<task>/` subdirectories as separate task updates before extracting shared guidance.
* Move a trait from `reference/<task>/` into `STYLE.md` or `common/*.md` only when direct instruction, repeated evidence across tasks, or current guidance supports broader scope.
* Do not use one `reference/<task>/` directory to update another `task/<task>/` unless the user names that target.

## Workflow

* Name the affected repository boundary, style layer, or `<task>`.
* Identify the reference scope: root `reference/`, one `reference/<task>/`, multiple task subdirectories, or user-provided material outside `reference/`.
* For each `reference/<task>/`, name the matching target `task/<task>/` before extracting traits.
* Read the current repository files that could own the update.
  For a task target, read the matching `task/<task>/` files when they exist, plus `STYLE.md`, relevant `common/*.md`, and the reference material.
* Read the direct user instruction, current guidance, references, examples, or repository self-updates that motivate it.
* Separate direct user instruction, current guidance, reference evidence, and inferred traits.
* Identify conflicts, duplication, stale routing, and unclear ownership.
* Extract only durable traits that can guide future work.
* Keep private facts, source-specific details, and protected wording out of guidance.
* Map every accepted trait to its narrowest owner in the owner map.
* Use the reference routing rules before changing `STYLE.md`, `common/*.md`, or `task/<task>/*.md`.
* Put reference-derived writing style only in `STYLE.md`, `common/*.md`, or `task/<task>/*.md`.
* Put broader writing style traits in `STYLE.md` or `common/*.md`.
* Put broader repository-operation or human-orientation traits in `AGENTS.md` or `README.md`.
* Edit only files whose roles own accepted traits.
* Remove repeated or stale rules from less appropriate files.
* Verify that each reference-derived trait landed in an owning repository file before treating it as usable guidance.
* Refresh `adapter/generic-llm.md` when reusable writing style changes.
* Make the adapter describe the current writing style and intended applications, not the update workflow or private evidence.
* For broad rewrites, repeat read, edit, and check passes until another pass would only be cosmetic.
* Use `REPORT.md` only when the update needs a structured report or the user asks for one.

## Decision Rules

* Follow `STYLE.md` source boundaries.
* Treat references as indirect evidence, not authority.
* Prefer explicit user direction over inference from examples.
* Prefer durable, broadly useful guidance over source-specific habits.
* Treat protected sources as high-level influence unless the user provides permission or a short excerpt.
* Keep fewer, stronger rules instead of cataloging every observed habit.
* Preserve uncertainty in the report instead of inventing rules.
* Do not add files unless the new file has a distinct role that reduces duplication.
* Do not describe unused paths or rewrite unrelated guidance to match an older structure.
