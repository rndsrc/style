# Elements of LLM Style

`README.md` orients humans.
This file tells agents what to read, edit, and validate.

## Authority

Reusable writing style lives in `STYLE.md`, `common/`, and matching task folders.
When guidance conflicts, use the narrowest source: matching task guidance, then `common/`, then `STYLE.md`.
`README.md` orients humans.
`AGENTS.md` files define operations.
Adapter files are derived prompts, not style authority.
Reference files are evidence, not style authority.
`task/style-update/` is only for updating this repository.
Files under `reference/` are private unless they explicitly say otherwise.

## Roles

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global writing principles, source boundaries, and Markdown conventions.
* `common/LANGUAGE.md`: shared word and sentence guidance.
* `common/CHECKLIST.md`: shared final checks.
* `task/`: task-specific guidance and workflows.
* `adapter/generic-llm.md`: derived portable prompt for tools that cannot read this repository.
* `reference/`: private evidence and license notice.

## Loading

For writing tasks, read in this order:

1. `STYLE.md`.
2. `common/LANGUAGE.md`.
3. The narrowest matching `task/<task>/` folder, when it exists.
4. `common/CHECKLIST.md` and any matching task checklist before final output.
5. `adapter/generic-llm.md` only when the target tool needs a portable prompt.

For repository updates, read in this order:

1. `task/style-update/`.
2. Current repository files that could own the update.
3. `reference/` only when the update needs reference material or the user names a specific reference.

## Maintenance

* Put each directive in its narrowest owner.
* Remove repeated directives from broader or derived files once a narrower owner exists.
* Keep human orientation, use, layout, and license summaries in `README.md`.
* Keep workflow instructions in `AGENTS.md` files and report templates in `REPORT.md` files.
* Keep adapter files derived from reusable writing style, and refresh them whenever reusable style changes.
* Keep source-specific evidence and private reference material in `reference/`.
* Describe only real or intentionally reserved files and directories.
* Add or keep a file only when it has a distinct role that reduces duplication, not for symmetry.

## Validation

Before finalizing repository changes, run these checks:

* Run `git diff --check`.
* Check that Markdown prose uses one sentence per physical line unless syntax requires otherwise.
* Run `git status --ignored --short --untracked-files=all` and check for unintended or hidden files.
* Report the checks run and any failures.
