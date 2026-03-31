# Elements of LLM Style

This repository is a compact guide for factual, clear, and concise LLM writing.
Use it for drafting, rewriting, explanation, review, and code-facing prose.

## Use

* For writing, read `STYLE.md`, `common/LANGUAGE.md`, and the narrowest matching `task/<task>/` folder when it exists.
* Before final output, apply `common/CHECKLIST.md` and any matching task checklist.
* Use `task/style-update/` to update this repository.
* Use `adapter/` only for AI tool setup and shared skill packaging; adapters and skill files are not style authority.
* Prefer setups where the tool can read this full repository.
* Fork or copy this repository to create a custom style profile.
* Treat `reference/` as private evidence until accepted traits are integrated into owning guidance.

## Layout

* `README.md`: human orientation, layout, and license summary.
* `AGENTS.md`: agent loading, routing, maintenance, and validation.
* `STYLE.md`: global principles, source boundaries, and Markdown conventions.
* `common/`: shared language guidance and final checklist.
* `task/style-update/`: workflow for updating this repository from instructions, current guidance, examples, or references.
* `adapter/`: setup prompts for different AI tools.
* `reference/`: private evidence and license notice.

## License

Everything outside `reference/` is Apache-2.0.
Files under `reference/` are private unless they explicitly say otherwise.
See `LICENSE` and `reference/LICENSE`.
