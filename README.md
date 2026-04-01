# Elements of LLM Style

This repository is a compact guide for factual, clear, and concise LLM writing.
Use it for drafting, rewriting, explanation, review, and code-facing prose.

## Use

* For writing, read `STYLE.md`, `common/LANGUAGE.md`, and the narrowest matching `task/<task>/` folder when present.
* Before final output, apply `common/CHECKLIST.md` and any matching task checklist.
* Use `task/style-update/` to update this repository.
* Use `adapter/` only for AI tool setup and shared skill packaging; it is not style authority.
* Fork or copy this repository to create a custom style profile.
* Treat `reference/` as private evidence, not guidance.

## Layout

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global principles, source boundaries, and Markdown conventions.
* `common/`: shared language guidance and final checklist.
* `task/`: task-specific guidance, checklists, and workflows, including the style-update workflow.
* `adapter/`: AI tool setup prompts and shared skill packaging.
* `reference/`: private evidence and license notice.

## License

Everything outside `reference/` is Apache-2.0.
Files under `reference/` are private unless they explicitly say otherwise.
See `LICENSE` and `reference/LICENSE`.
