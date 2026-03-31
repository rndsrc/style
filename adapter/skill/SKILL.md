---
name: elements-of-llm-style
description: Apply Elements of LLM Style when the user asks for this repository's style, a style profile, or style-consistent drafting, rewriting, reviewing, editing, explanation, documentation, or code-facing prose. Read the style repository as source of truth; use the generic adapter only as a fallback.
---

# Elements of LLM Style Skill

Use this skill when the user asks for this repository's style, a style profile, or style-consistent work.
Read the repository files rather than treating this skill file as style authority.

## Locate

1. If the current directory is the style repository or is inside it, use the nearest ancestor that contains `STYLE.md`.
2. Otherwise, if the workspace contains `style/STYLE.md`, use that `style/` directory as the source repository.
3. If multiple style repositories are present, use the one named by the user, or the one nearest the current directory.
4. If repository files are unavailable, use `adapter/generic-llm.md` only when the user provided it or it is already present in context.
5. If neither the repository nor the generic adapter is available, state that the style source files are unavailable.

## Load

For style-consistent writing, read in this order:

1. `STYLE.md`.
2. `common/LANGUAGE.md`.
3. The narrowest matching `task/<task>/` folder, when present.
4. `common/CHECKLIST.md` and any matching task checklist before final output.
5. `AGENTS.md` when routing, repository maintenance, adapter policy, or source boundaries matter.

For repository updates, read in this order:

1. `task/style-update/`.
2. `AGENTS.md` for ownership, routing, maintenance, and validation rules.
3. Current repository files that could own the update.
4. `reference/` only when the update needs reference material or the user names a specific reference.

## Apply

* Preserve facts, meaning, intent, constraints, audience, technical claims, and evidence limits before polish.
* Lead with the requested outcome or main point.
* Use concise, concrete language.
* Separate facts, inferences, and recommendations.
* State assumptions and uncertainty when they matter.
* Keep claims proportional to evidence.
* Match structure and detail to the task and audience.
* Remove material that does not help the reader understand, decide, or act.
* Keep code-facing prose consistent with this style without overriding local project conventions.
* Treat `adapter/skill/` as agent-loading material, not style authority.
* Treat `adapter/` as setup material, not style authority.
* Treat `reference/` as private evidence, not reusable guidance.
* Use `adapter/generic-llm.md` only when repository files are unavailable.
* Avoid filler, unsupported hype, empty apology, decorative transitions, and certainty that outruns evidence.
* If a named path is unavailable, report the gap instead of inventing guidance.

## Final Check

Apply `common/CHECKLIST.md` before final output.
If repository style files changed, run the validation checks required by `AGENTS.md`.
Report validation honestly, including skipped checks and unavailable source files.
