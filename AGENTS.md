# AGENTS.md

These instructions apply to the whole repository.


## Purpose

This repo defines how to write and code.
Use it when drafting, rewriting, reviewing, or explaining work.

`README.md` is for humans.
This file tells agents what to do.


## Source Of Truth

* `STYLE.md` defines the overall voice and judgment.
* `common/` contains shared rules, tone guidance, and checks.
* `task/` contains task-specific guidance.
* `reference/` holds example writing for future updates.
  It is not used other than the `task/style-update` task.
* Tool-specific adapter files are exports or setup helpers.
  They are not separate style guidance.
* Adapter snapshots may duplicate guidance for installation elsewhere.
  The canonical files still win when there is a conflict.


## File Responsibilities

Task folders may include:

* `AGENTS.md`  : how to run the task
* `STYLE.md`   : task-specific voice and rules
* `PROMPT.md`  : reusable prompts
* `REPORT.md`  : output structure (optional)
* `RUBRIC.md`  : quality checks
* `EXAMPLE.md` : real examples, only if useful

Do not add files just for consistency.
If something is missing, use the best available guidance.


## Loading Order

When applying the style:

1. Read `STYLE.md`.
2. If present, read `common/*.md`.
3. If a relevant task folder exists, read exactly one relevant task
   folder unless the user asks for a cross-task output.
4. Within a task folder, prefer:
   * `AGENTS.md` : procedure
   * `STYLE.md`  : task voice
   * `PROMPT.md` : reusable prompts
   * `REPORT.md` : report template
   * `RUBRIC.md` : final checks
5. If the target task folder or a task file is missing, use the
   closest available guidance and state the gap only when it affects
   the result.
6. Read `EXAMPLE.md` only when needed to resolve tone, structure, or
   phrasing.


## Adapter Policy

* Treat `adapter/` as tool-specific exports and setup guides.
* Do not make `adapter/` a separate style authority.
* Keep adapters thin and traceable to `STYLE.md`, `common/`, and
  `task/`.
* When canonical guidance changes, update matching adapter text or
  mark the adapter as needing regeneration.
* If an adapter duplicates guidance, the canonical source wins.
* Generated adapter snapshots should say what canonical files they mirror.


## Task Routing

* Style evolution from liked source writing: use `task/style-update/`.
* General style rewriting: use `common/PROMPT.md` if present, then
  choose the closest task folder if one applies.
  If neither exists, use `STYLE.md`.
* Do not use `task/style-update/` unless updating the style itself.


## Validation

Before finalizing repository changes:

* Run `git diff --check`.
* Check for adapter references to files that do not exist.
* Check `git status --ignored --short --untracked-files=all` for
  accidentally ignored adapter exports or local editor backups.
