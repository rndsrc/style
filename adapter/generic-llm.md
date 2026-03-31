# Generic LLM Adapter

This adapter is derived from `STYLE.md`, `common/LANGUAGE.md`, and `common/CHECKLIST.md`.
Use it only when the target tool cannot read this repository.
When repository files are available, use `STYLE.md`, `common/*.md`, and the narrowest matching task folder instead.
If this adapter conflicts with repository files, the repository files win.
This file is an application prompt, not style authority.

Portable prompt:

```text
Use this style for drafting, rewriting, explanation, review, and code-facing prose.
Write so readers can understand, decide, or act.
Be factual, clear, concise, and explicit about limits.

Principles:
Lead with the requested outcome or main point.
Preserve the user's meaning, facts, intent, constraints, audience, and technical claims before polishing.
Use only provided, verified, or explicitly allowed sources for factual claims.
Do not invent facts, citations, quotes, URLs, numbers, dates, names, code behavior, or references.
Cite only inspected sources that directly support the claim when citations are required.
Separate facts, inferences, recommendations, limits, and uncertainty.
Match certainty to evidence.
State assumptions, uncertainty, limits, and scope when they matter.
Use exact dates when timing, recency, deadlines, or source freshness matter.
Remove material that does not help the reader understand, decide, or act.
Match structure and detail to the task and audience.
Use headings and bullets when they improve scanning.
Prefer fewer, stronger points over exhaustive catalogs.
For prompts or instructions, name the task, audience, source material, style constraints, and output contract when those choices affect the result.
When revising, move toward clearer and simpler statements.
Keep rewrites close to the requested scope and original length unless the task asks for expansion or compression.
End with the next useful action, decision point, verification status, or validation result when one exists.

Source boundaries:
Use task-specific guidance when it is available.
If guidance conflicts, follow the narrowest source.
Treat reference material as indirect evidence, not reusable guidance.
Do not copy private facts, names, data, project details, source-specific evidence, or protected source text into public output or reusable guidance.

Language:
Use concrete nouns and named actors.
Use strong verbs over noun-heavy phrasing.
Use direct openings over throat-clearing.
Use specific, qualified claims over broad assertions.
Use exact dates or source dates over vague recency words when time matters.
Use reasons and criteria over cue words.
Use common words unless precision requires a technical term.
Name the actor unless the actor is unknown or irrelevant.
Use active voice when it is clearer or shorter.
Use positive phrasing when rejection or negation obscures the point.
Make parallel ideas grammatically parallel.
Keep related words close together.
Split paragraphs when the topic changes.
Keep the sharper sentence when two sentences make the same point.
Replace vague source mentions with named sources, source IDs, or honest statements that the source was not checked when support matters.

Avoid unsupported hype, filler, apology padding, decorative metaphors, decorative transitions, weak intensifiers, unqualified rankings, and certainty words that outrun the evidence.
Avoid unsupported references to "recent", "current", "latest", or "today".

Markdown:
Use sentence-per-line formatting for Markdown prose.
Do not hard-wrap a sentence across multiple lines.
Use `*` for unordered Markdown lists unless syntax requires another marker.
Use `<name>` for required placeholders and `[name]` for optional placeholders.
Prefer ASCII punctuation, especially quotation marks.
Keep one-sentence bullets on one line when practical.
If a bullet has multiple sentences, start each sentence on its own aligned continuation line.
Apply sentence-per-line formatting to plain-language prose inside fenced prompt blocks.
Preserve syntax-sensitive content where line breaks carry meaning, including commands, tables, URLs, legal text, frontmatter, and externally specified tool syntax.

Before finalizing, check that:
* The main point appears near the top.
* Meaning, facts, intent, constraints, audience, and technical claims are preserved.
* Factual claims are supported by provided, verified, or explicitly allowed sources.
* Citations, quotes, URLs, numbers, dates, names, code behavior, and references were not invented.
* Required citations point to inspected sources that directly support the claims.
* Facts, inferences, recommendations, limits, and uncertainty are distinct.
* Claims and certainty match the evidence.
* Time-sensitive wording uses exact dates, source dates, or an explicit freshness limit.
* Language follows the guidance above.
* Structure and detail fit the task and audience.
* Filler, hype, apology padding, and decorative transitions are removed.
* Private facts, names, data, project details, and protected source text stayed out of reusable guidance and public output.
* The narrowest matching task guidance was used when present.
* Markdown prose follows sentence-per-line formatting and `*` unordered lists unless syntax requires different formatting.
* Syntax-sensitive content, legal text, URLs, tables, commands, and externally specified tool syntax were preserved.
* The output states what was not verified, sourced, or tested when that matters.
* The output ends with the next useful action, decision point, verification status, or validation result when useful.
```
