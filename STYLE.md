# Elements of LLM Style

Write so readers can understand, decide, or act.
Be factual, clear, concise, and explicit about limits.
Keep reusable guidance in its narrowest owner: global principles here, shared language in `common/`, and task-specific guidance in `task/`.

## Principles

* Lead with the requested outcome or main point.
* Preserve meaning, facts, intent, constraints, audience, and technical claims before polish.
* Separate facts, inferences, and recommendations.
* Match certainty to evidence.
* State assumptions, uncertainty, limits, or scope when they matter.
* Remove material that does not help the reader understand, decide, or act.
* Match structure and detail to the task and audience.
* Use headings and bullets when they improve scanning.
* Prefer fewer, stronger points over exhaustive catalogs.
* In revisions, move toward clearer and simpler statements.
* Keep rewrites close to the requested scope and original length unless the task asks for expansion or compression.
* End with the next useful action, decision point, or validation result when one exists.

## Source Boundaries

Use `STYLE.md`, `common/*.md`, and matching task guidance as reusable writing style.
Use `README.md` for repository orientation, not writing style.
Use `AGENTS.md` files for agent operations, not writing style.
Use `task/style-update/` for repository updates, not ordinary writing tasks.
Use `adapter/` as derived application prompts, not style authority.
Use `reference/` as indirect evidence, not reusable guidance.
Reference-derived writing traits become guidance only after integration into `STYLE.md`, `common/*.md`, or a matching task folder.
Reference-derived repository-operation traits become guidance only after integration into `README.md`, `AGENTS.md`, or a matching task workflow.
Do not move private facts, names, data, project details, or protected source text into reusable guidance, adapters, templates, documentation, or generated public text.
When adapting examples or protected sources, distill durable rules instead of copying sample prose.

## Markdown Conventions

Use `<name>` for required placeholders and `[name]` for optional placeholders.
Use `*` for unordered Markdown lists.
Prefer ASCII punctuation, especially quotation marks.
Start each prose sentence on its own physical line.
Do not hard-wrap a sentence across multiple lines.
Keep one-sentence bullets on one line when practical.
If a bullet has multiple sentences, start each sentence on its own aligned continuation line.
Apply sentence-per-line formatting to plain-language prose inside fenced prompt blocks.
Preserve syntax-sensitive content where line breaks carry meaning, including commands, tables, URLs, legal text, frontmatter, and externally specified tool syntax.
