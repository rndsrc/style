# Style Update Checklist

Before finalizing a style update:

* The affected layer, `<task>`, or repository boundary is named.
* The reference scope is named.
* Each `reference/<task>/` source has a target `task/<task>/` before traits are extracted.
* Multiple `reference/<task>/` sources were processed as separate task updates before any shared guidance was extracted.
* Current files that could own the update were read.
* For task-targeted updates, matching `task/<task>/` files were read when present.
* Relevant direct instruction, current guidance, references, examples, or self-updates were read.
* Direct user instruction, current guidance, indirect reference evidence, and inferred traits were separated.
* References were treated as indirect evidence and not as reusable guidance.
* Accepted traits are durable enough to guide future work.
* Rejected or deferred traits are noted when they could matter later.
* Each accepted trait landed in its owning file.
* Each reference-derived trait was mapped to an owning file before use.
* Reference-derived writing style landed only in `STYLE.md`, `common/*.md`, or `task/<task>/*.md`.
* Existing `reference/<task>/` subdirectories were checked against matching `task/<task>/` folders.
* Task-specific traits from `reference/<task>/` landed in `task/<task>/`, or the reason for not creating or updating that task folder was reported.
* Traits from one task reference were not promoted to `STYLE.md` or `common/*.md` without direct instruction, repeated evidence, or current guidance.
* One `reference/<task>/` directory did not update another `task/<task>/` unless the user named that target.
* `README.md` was updated with `AGENTS.md` when the trait changed human-facing repository use, layout, or orientation.
* Root `AGENTS.md` was updated when the trait affected agent loading, routing, maintenance, or validation.
* Conflicts between sources were resolved or reported.
* Repetition, conflicts, stale routing, and unclear ownership were removed or reported.
* Reference facts, private details, and protected source text stayed out of reusable guidance and adapters.
* `task/style-update/` and `adapter/` were not treated as style authority outside their own roles.
* No unused file or path was added or described only for symmetry.
* `adapter/generic-llm.md` describes the current writing style and intended applications, or the reason was reported.
* A second pass found no substantive conflict, duplication, or ownership problem.
* The guidance is compact enough for a human or less capable LLM to follow.
* `common/CHECKLIST.md` was applied.
* `git diff --check` passes.
* `git status --ignored --short --untracked-files=all` shows no unintended files.
