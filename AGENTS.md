# Elements of LLM Style

Use this file for agent loading, routing, maintenance, and validation.

## Authority

Reusable writing style lives in `STYLE.md`, `common/`, and matching `task/` folders.
When guidance conflicts, use the narrowest source: matching task guidance, then `common/`, then `STYLE.md`.
`README.md` orients humans; `AGENTS.md` files define operations.
`adapter/` files are setup prompts or skill packaging, not style authority.
`reference/` files are private evidence, not style authority, unless a file explicitly says otherwise.
`task/style-update/` is only for updating this repository.

## Roles

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global writing principles, source boundaries, and Markdown conventions.
* `common/LANGUAGE.md`: shared word and sentence guidance.
* `common/CHECKLIST.md`: shared final checks.
* `task/`: task-specific guidance and workflows.
* `adapter/`: derived setup prompts and shared skill packaging for tools that should read this repository.
* `reference/`: private evidence and license notice.

## Loading

For writing tasks, read in this order:

1. `STYLE.md`.
2. `common/LANGUAGE.md`.
3. The narrowest matching `task/<task>/` folder, when present.
4. `common/CHECKLIST.md` and any matching task checklist before final output.
5. A matching `adapter/` file only when the target tool needs setup instructions or a portable prompt.

For repository updates, read in this order:

1. `task/style-update/`.
2. Current repository files that could own the update.
3. `reference/` only when the update needs reference material or the user names a specific reference.

## Maintenance

* Put each directive in its narrowest owner and remove broader duplicates.
* Keep human orientation, layout, and license summaries in `README.md`.
* Keep workflows in `AGENTS.md` files and report templates in `REPORT.md` files.
* Keep adapters derived, profile-neutral, and focused on tool setup or skill packaging.
* Refresh affected adapters when reusable style, source boundaries, or loading rules change.
* Keep private evidence and reference material in `reference/`.
* Describe only real files and directories.
* Add files only when they reduce duplication or have a distinct role.

## Validation

Before finalizing repository changes, run these checks:

* Run `git diff --check`.
* Check that Markdown prose uses one sentence per physical line unless syntax requires otherwise.
* Run `git status --ignored --short --untracked-files=all` and check for unintended or hidden files.
* Report the checks run and any failures.
