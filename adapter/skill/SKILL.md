---
name: elements-of-llm-style
description: Apply Elements of LLM Style when the user asks for this repository's style, a style profile, or style-consistent drafting, rewriting, reviewing, editing, explanation, documentation, or code-facing prose; read the style repository as source of truth and use the generic adapter only as a fallback.
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

Use the current `STYLE.md` and `common/*.md` guidance as the source of truth.
If this skill conflicts with those repository files, the repository files win.

* Preserve facts, meaning, intent, constraints, audience, technical claims, and evidence limits before polish.
* Lead with the requested outcome or main point.
* Use only provided, verified, or explicitly allowed sources for factual claims.
* Do not invent facts, citations, quotes, URLs, numbers, dates, names, code behavior, or references.
* Cite only inspected sources that directly support the claim when citations are required.
* Use concise, concrete language.
* Use concrete nouns, named actors, strong verbs, direct openings, and specific qualified claims.
* Separate facts, inferences, recommendations, limits, and uncertainty.
* State assumptions, uncertainty, limits, and scope when they matter.
* Keep claims proportional to evidence.
* Use exact dates when timing, recency, deadlines, or source freshness matter.
* Match structure and detail to the task and audience.
* Remove material that does not help the reader understand, decide, or act.
* Use headings and bullets when they improve scanning.
* Prefer fewer, stronger points over exhaustive catalogs.
* For prompts or instructions, name the task, audience, source material, style constraints, and output contract when those choices affect the result.
* Keep rewrites close to the requested scope and original length unless the task asks for expansion or compression.
* Keep code-facing prose consistent with this style without overriding local project conventions.
* Treat `adapter/skill/` as agent-loading material, not style authority.
* Treat `adapter/` as setup material, not style authority.
* Treat `reference/` as indirect evidence, not reusable guidance.
* Use `adapter/generic-llm.md` only when repository files are unavailable.
* Avoid filler, unsupported hype, apology padding, decorative transitions, weak intensifiers, vague recency words, and certainty that outruns evidence.
* Use sentence-per-line formatting, `*` unordered lists, `<name>` for required placeholders, and `[name]` for optional placeholders unless syntax requires otherwise.
* Preserve syntax-sensitive content where line breaks carry meaning.
* End with the next useful action, decision point, verification status, or validation result when one exists.
* If a named path is unavailable, report the gap instead of inventing guidance.

## Final Check

Apply `common/CHECKLIST.md` before final output.
Check factual support, citation support, date freshness, language, task fit, source boundaries, Markdown conventions, and anything not verified, sourced, or tested.
If repository style files changed, run the validation checks required by `AGENTS.md`.
Report validation honestly, including skipped checks, unavailable source files, and anything not verified, sourced, or tested when that matters.
