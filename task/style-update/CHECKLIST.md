# Style Update Checklist

Before finalizing a style update:

* The affected layer, `<task>`, or repository boundary is named.
* The source material and evidence scope are named.
* Current files that could own the update were read.
* For task-targeted updates, matching `task/<task>/` files were read when present.
* Direct instruction, current guidance, evidence, and inferred traits were separated.
* `reference/` material was treated as private evidence, not reusable guidance.
* Accepted traits are durable enough to guide future work.
* Rejected or deferred traits are noted when they could matter later.
* Each accepted trait landed in its narrowest owning file.
* Task-specific traits from `reference/<task>/` landed in `task/<task>/`, or the reason was reported.
* Shared traits are backed by direct instruction, repeated evidence, or current guidance.
* Conflicts, repetition, stale routing, and unclear ownership were removed or reported.
* Private facts, names, data, project details, and protected source text stayed out of reusable guidance, skill files, and adapters.
* `task/style-update/` and adapter files were not treated as general style authority.
* No unused file or path was added.
* Affected `adapter/` files are profile-neutral and describe current style, repository loading, and intended use.
* A second pass found no substantive conflict, duplication, or ownership problem.
* The guidance is compact enough for a human or less capable LLM to follow.
* `common/CHECKLIST.md` was applied.
* `git diff --check` passes.
* `git status --ignored --short --untracked-files=all` shows no unintended files.
