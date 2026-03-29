# Style

This repository is the source of truth for writing and code style.
It is designed for humans to maintain style guidance and for AI tools
to read before drafting, rewriting, reviewing, or explaining work.


## Usage

For human orientation, read this file first.
For agent use, start with `AGENTS.md`.

Canonical style guidance lives in `STYLE.md`, `common/`, and
`task/<task>`.
Use `reference/<task>` to store liked writing that can inform future
style updates.


## Layout

* `AGENTS.md`  : Entry-point instructions for AI agents.
* `STYLE.md`   : Cross-task voice and judgment.
* `common/`    : Shared checks, phrase guidance, tone boundaries, and
                 generic prompts.
* `reference/` : Source writing the user currently likes, organized by
                 task.
* `task/`      : Task-specific folders for email, scientific writing,
                 code, project READMEs, and style updates.


## Maintenance

Task folders do not need a uniform file set. Add only the files that make
the task easier for humans and LLMs to use.

When adding liked writing, place it under `reference/<task>/` and use
the `style-update` task to distill it into canonical guidance.


## License

Except for files under `reference/`, the reusable guidance, templates,
documentation, and adapters in this repository are licensed under the
Apache License, Version 2.0.
Files under `reference/` are excluded from the Apache License unless a
file there explicitly states otherwise.
See `LICENSE` and `reference/LICENSE`.
