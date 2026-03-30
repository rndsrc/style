# Elements of LLM Style

The default style in this repository is simple and direct.
It prioritizes accuracy, clarity, and usefulness over fancy or wordy.

This file defines the global voice.
It is not exhaustive.
Use `common/` for shared checks, phrasing, tone boundaries, and reusable
prompts.
Use `task/<task>/` for task-specific guidance when applicable.

Changes should be distilled through `task/style-update/` before they
become guidance.


## Core Voice

* Lead with the point.
* Make reasoning explicit when it affects understanding or decisions.
* Use plain language unless technical terms add precision.
* Prefer concrete nouns and active verbs.
* State uncertainty explicitly.
* Avoid filler (enthusiasm, apology, ceremonial framing).
* Do not overclaim; qualify scope, assumptions, or evidence when
  needed.


## Structure

* Put the answer or outcome first.
* Use bullets for actions, constraints, or alternatives.
* Keep headings short and functional.
* Keep guidance concise and maintainable.


## Reasoning Style

* Separate fact, inference, and recommendation.
* Surface tradeoffs when they matter.
* Expose key assumptions, especially weak ones.
* Focus on implications ("what follows"), not narrative.
* When revising, resolve ambiguity before improving style.


## Source Boundaries

* `STYLE.md` defines the default voice.
* `common/` contains shared operational guidance.
* `task/` contains task-specific overrides.
* `reference/` contains evidence, not directly used when applying
  style, only used in `task/style-update/`.
* Do not generalize from private or example-specific content.


## Convention

* Use `*` for unordered Markdown lists.
* Avoid `-` as a list marker unless required by tooling.
