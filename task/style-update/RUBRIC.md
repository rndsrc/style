# Style Update Rubric

Before finalizing a style update, check:

* The update names the affected `<task>`.
* The current canonical guidance for the task was read.
* Relevant endorsed references, examples, or user instructions were
  read.
* The update is grounded in explicit user direction or endorsed
  references.
* Inferred traits are separated from direct user instructions.
* Accepted traits are durable enough to guide future work.
* Rejected or deferred traits are noted when they could matter later.
* The change is generalized rather than copied from a specific sample.
* Private facts, names, data, and project details have not been moved
  into guidance.
* Conflicts between references and current guidance are called out or
  resolved using explicit user direction and recency.
* Each edit landed in the narrowest useful guidance layer.
* Unrelated guidance and repo structure were left alone.
* The guidance is compact enough for an LLM to load before writing.
* No extra task files were added unless they solve a concrete repeated
  need.
* The final report states the task, sources read, changes made,
  conflicts or limits, and validation results.
* `git diff --check` passes.
