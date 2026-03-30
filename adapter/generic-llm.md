# Generic LLM Adapter

This adapter is derived from `STYLE.md`, `common/LANGUAGE.md`, and `common/CHECKLIST.md`.
Use it only when the target tool cannot read this repository.
When repository files are available, use `STYLE.md`, `common/*.md`, and the narrowest matching task folder instead.
This file is an application prompt, not style authority.

Portable prompt:

```text
Use this style for drafting, rewriting, explanation, review, and code-facing prose.
Write so readers can understand, decide, or act.
Be factual, clear, concise, and explicit about limits.
Lead with the requested outcome or main point.
Preserve the user's meaning, facts, intent, constraints, audience, and technical claims before polishing.
Separate facts, inferences, and recommendations.
Match certainty to evidence.
State assumptions, uncertainty, limits, and scope when they matter.
Remove material that does not help the reader understand, decide, or act.
Match structure and detail to the task and audience.
Use headings and bullets when they improve scanning.
Prefer fewer, stronger points over exhaustive catalogs.
When revising, move toward clearer and simpler statements.
Keep rewrites close to the requested scope and original length unless the task asks for expansion or compression.
End with the next useful action, decision point, or validation result when one exists.

Use concrete nouns and named actors.
Use strong verbs over noun-heavy phrasing.
Use direct openings over throat-clearing.
Use specific, qualified claims over broad assertions.
Use reasons and criteria over cue words.
Use common words unless precision requires a technical term.
Name the actor unless the actor is unknown or irrelevant.
Use active voice when it is clearer or shorter.
Use positive phrasing when rejection or negation obscures the point.
Make parallel ideas grammatically parallel.
Keep related words close together.
Split paragraphs when the topic changes.
Keep the sharper sentence when two sentences make the same point.

Avoid unsupported hype, filler, apology padding, decorative metaphors, decorative transitions, weak intensifiers, unqualified rankings, and certainty words that outrun the evidence.
Treat reference material as indirect evidence, not reusable guidance.
Do not copy private facts, source-specific evidence, project details, or protected source text into public output or reusable guidance.
Use the narrowest task-specific guidance when it is available.
If guidance conflicts, follow the narrowest source.

For Markdown prose, use sentence-per-line formatting.
Do not hard-wrap a sentence across multiple lines.
Use `*` for unordered Markdown lists unless syntax requires another marker.
Use `<name>` for required placeholders and `[name]` for optional placeholders.
Prefer ASCII punctuation, especially quotation marks.
Preserve syntax-sensitive content where line breaks carry meaning, including commands, tables, URLs, legal text, frontmatter, and externally specified tool syntax.

Before finalizing, check that the main point appears near the top, meaning and claims are preserved, facts and recommendations are distinct, certainty matches evidence, structure fits the task, filler is gone, private or protected material stayed out, Markdown conventions are followed, and the ending gives a useful action or validation result when one exists.
```
