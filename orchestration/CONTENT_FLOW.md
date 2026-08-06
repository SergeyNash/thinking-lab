# CONTENT FLOW

This document defines how Thinking Lab creates content from a natural dialogue.

The goal is not to make publishing easier at the cost of thinking.
The goal is to let a user request a content artifact while the system still
preserves research, reasoning, traceability, and style.

Public-facing outputs are in Russian by default.

---

## 1. Purpose

`CONTENT_FLOW.md` coordinates:

- user intent;
- research optics;
- output type;
- module routing;
- output decision;
- draft or outline creation;
- knowledge updates.

It exists because a user should be able to say:

> Сделай Telegram-пост про почему SQL жив 50 лет.

and the system should understand both:

- the requested output type is `telegram_note`;
- the research still needs enough reasoning to avoid shallow content.

---

## 2. Core Rule

Requested output type does not cancel research.

Format affects adaptation.
It does not lower the standard of reasoning.

If the topic is weak, unclear, or unsupported, the system should produce a
research plan, working note, or unfinished investigation instead of a confident
public post.

---

## 3. Intake Fields

When a user asks for content, extract these fields from the dialogue:

```markdown
Topic / artifact:
Requested output type:
Research optics:
Audience:
Depth:
Existing research:
Draft provided:
Language:
Constraints:
```

Defaults:

- `Language`: Russian for public-facing output.
- `Audience`: product-minded engineers, product leaders, engineering managers,
  security and AI practitioners, unless specified otherwise.
- `Depth`: medium.
- `Research optics`: infer from the request; ask only if ambiguity affects the
  result.
- `Requested output type`: infer from words such as Telegram, LinkedIn, essay,
  note, unfinished research, failure analysis.

Ask follow-up questions only when missing information materially changes the
work. Prefer 2-4 short questions.

---

## 4. Output Types v0.1

Supported output types:

- `telegram_note`: compact public research note.
- `linkedin_post`: professional public note for peers.
- `essay`: long-form investigation.
- `working_note`: internal or semi-private thinking artifact.
- `unfinished_research`: honest public or private note about thinking in
  progress.
- `failure_analysis`: investigation of why an idea, product, architecture,
  process, or system failed.

Research optics and output types are different things.

Example:

```text
Topic: Git
Research optics: archaeology of engineering decisions, mental model
Output type: telegram_note
```

---

## 5. Operating Modes

### New Research

Use when the topic is new or not yet represented in `knowledge/`.

Route:

```text
intake -> TOPICS.md candidate -> module pass -> RESEARCH_NOTES.md -> output decision
```

### Continue Existing Research

Use when a topic or research note already exists.

Route:

```text
intake -> find existing note -> identify missing step -> continue module pass -> output decision
```

### Transform Existing Note

Use when the research exists and the user wants a specific format.

Route:

```text
research note -> Editor -> communication format -> draft or outline
```

### Humanize Existing Draft

Use when the user provides a draft and asks to make it sound more human,
product-minded, or closer to the author's voice.

Route:

```text
draft -> STYLE.md -> RUSSIAN_ANTI_PATTERNS.md -> humanize-ru -> HUMANIZER_CORE.md -> HUMANIZER_RULES.md -> product/JTBD voice check -> revised draft
```

Do not invent new research during humanization. If reasoning is weak, say so.

---

## 6. Reasoning Routes

Choose the smallest route that preserves understanding.

### Light Pass

Use when the idea is already clear and low-risk.

Minimum checks:

- question;
- tension;
- obvious weak explanation;
- mechanism;
- principle;
- limit.

### Full Module Pipeline

Use when the topic is new, complex, or likely to produce shallow claims.

Route:

```text
Archaeologist -> Historian -> Opponent -> Transfer -> Synthesizer -> Editor
```

### Humanizer Pass

Use for style transformation of an existing draft.

Checks:

- natural Russian;
- no generic AI rhythm;
- no forced bullets;
- no repeated rhetorical patterns;
- product/JTBD lens where useful;
- no polishing of weak thought.

### Output Adaptation

Use when research is ready but the format changes.

Example:

```text
essay outline -> telegram_note
research note -> linkedin_post
working note -> unfinished_research
```

---

## 7. Publication Readiness

Before drafting a public output, check:

- Is there a research question?
- Is the selected research optic clear?
- Is the requested output type clear?
- Is the core mechanism understandable?
- Is there at least one rejected shallow explanation or known limit?
- Is the principle connected to the artifact?
- Is the audience clear?
- Would a public draft hide missing evidence?

If the answer is weak, do not force a polished post.

Recommended fallback:

- `working_note` for private thinking;
- `unfinished_research` for honest public thinking in progress;
- research plan if the topic is still too early.

---

## 8. Output Plan Template

Use this before writing:

```markdown
## Output Plan

Topic / artifact:
Requested output type:
Actual output decision:
Research optics:
Audience:
Depth:
Language:
Core question:
Tension:
Mechanism:
Rejected explanation:
Principle:
Limit:
Format notes:
Knowledge updates:
```

`Requested output type` records what the user asked for.
`Actual output decision` records what the system decided is justified.

These can differ.

---

## 9. Knowledge Updates

After content work, recommend updates to:

- `knowledge/TOPICS.md` when the topic is new;
- `knowledge/RESEARCH_NOTES.md` when reasoning was performed;
- `knowledge/FRAMEWORKS.md` when a reusable model appeared;
- `knowledge/ANALOGIES.md` when transfer was tested;
- `knowledge/FAILURES.md` when a weak explanation was rejected;
- `knowledge/OUTPUTS.md` when a draft, outline, or publication exists.

Real draft files should live in `outputs/`.

`knowledge/OUTPUTS.md` remains the index that connects outputs back to
research.

---

## 10. Summary

Dialog-first content creation should feel natural to the user and disciplined
inside the system.

The short version:

> The user may ask for a format.
> The system must still protect the thinking.
