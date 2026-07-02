---
name: thinking-lab-content
description: Use when the user asks Thinking Lab to create, plan, adapt, humanize, or choose a format for content from a topic, research note, draft, or idea. Triggers include requests for Telegram posts, LinkedIn posts, essays, working notes, unfinished research notes, failure analysis, product-minded humanization, or dialog-first content creation while preserving Thinking Lab reasoning.
---

# Thinking Lab Content

## Overview

Run the Thinking Lab dialog-first content flow.

This skill is an orchestration skill, not a generic writing skill. It helps move
from a user's natural request to research routing, output decision, and a
Russian draft or outline without skipping reasoning.

## Source Documents

When working inside the Thinking Lab repository, use these documents as the
source of truth:

- `orchestration/CONTENT_FLOW.md`
- `reasoning/RESEARCH_METHOD.md`
- `knowledge/TOPICS.md`
- `knowledge/RESEARCH_NOTES.md`
- `knowledge/OUTPUTS.md`
- `modules/MODULES.md`
- `modules/editor.md`
- `communication/WRITING.md`
- `communication/STYLE.md`
- `communication/RUSSIAN_ANTI_PATTERNS.md`
- `communication/FORMATS.md`

If a document is missing, continue with the closest available project context
and mention the gap.

## Intake

Extract these fields from the user's request:

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

- Language: Russian for public-facing output.
- Audience: product-minded engineers, product leaders, engineering managers,
  security and AI practitioners.
- Depth: medium.
- Research optics: infer from the request when possible.
- Requested output type: infer from words such as Telegram, LinkedIn, essay,
  note, unfinished research, failure analysis.

Ask 2-4 short questions only when missing information materially changes the
result.

## Output Types

Supported v0.1 output types:

- `telegram_note`
- `linkedin_post`
- `essay`
- `working_note`
- `unfinished_research`
- `failure_analysis`

Do not confuse output type with research optic.

Example:

```text
Topic: Git
Research optics: archaeology of engineering decisions, mental model
Output type: telegram_note
```

## Research Optics

Use one or more optics:

- archaeology of engineering decisions;
- engineering of management;
- cross-domain analogies;
- mental models;
- future of engineering;
- unfinished investigations;
- failure analysis;
- principle extraction.

Optics are not rubrics or content categories. They are ways of investigating
the topic.

## Route Selection

Choose the smallest route that preserves understanding.

### New Research

Use when the topic is new or unsupported.

Route:

```text
intake -> light/full module pass -> research note -> output decision
```

### Continue Existing Research

Use when the topic already exists in `knowledge/`.

Route:

```text
intake -> existing note -> missing reasoning step -> output decision
```

### Transform Existing Note

Use when research exists and the user asks for a specific format.

Route:

```text
research note -> Editor -> selected format -> draft or outline
```

### Humanize Existing Draft

Use when the user provides a draft and asks to make it sound more human or
closer to the author's product-minded style.

Route:

```text
draft -> STYLE.md -> RUSSIAN_ANTI_PATTERNS.md -> humanized product voice -> revised draft
```

Do not invent research during humanization. If the reasoning is weak, say so.

Always run the Russian anti-pattern pass before returning the revised draft.

## Readiness Gate

Before writing a public output, verify:

- there is a clear research question;
- the research optic is explicit or safely inferred;
- the requested output type is clear;
- the core mechanism is understandable;
- a shallow explanation or limit is visible;
- the principle is connected to the artifact;
- the audience is clear;
- the draft would not hide missing evidence.

If readiness is weak, propose a `working_note`, `unfinished_research`, or short
research pass instead of a confident public post.

## Output Plan

Before drafting, produce or mentally verify:

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

`Requested output type` is what the user asked for.
`Actual output decision` is what the system believes is justified.

They may differ.

## Writing Rules

When drafting:

- write public-facing outputs in Russian by default;
- use intelligent conversational Russian;
- preserve uncertainty, limits, and counterarguments;
- keep the humanized product voice visible when useful;
- use JTBD naturally, not as a forced template;
- avoid generic AI tone and LinkedIn theater;
- avoid repetitive bullet-question patterns;
- avoid overusing short dramatic sentences;
- avoid English-calque contrast patterns in Russian;
- replace contrast templates with concrete causal explanation;
- avoid abstract placeholder product examples when a real product situation can
  make the point;
- do not polish weak reasoning into confident prose.

Use `communication/RUSSIAN_ANTI_PATTERNS.md` as the detailed reference.

## Russian Anti-Pattern Pass

Before returning a public-facing draft or humanized text, scan for:

- `это не просто`;
- `это не про`;
- `проблема не в том`;
- `когда/если ..., это`;
- `может привести к`;
- unnecessary `не только, но и`;
- participial adverb phrases that blur the main action;
- abstract placeholder product examples.

Rewrite using:

- concrete situation;
- direct Russian syntax;
- causal explanation;
- visible product context;
- simple verb clauses;
- normal `и` instead of fake contrast.

Bad pattern:

```text
Проблема не в том, что проверка слишком строгая.
Проблема в том, что риск стал видимым слишком поздно.
```

Better:

```text
Со стороны кажется, что безопасность просто тормозит релиз. Но к этому моменту
команда уже выбрала решение, написала код, договорилась о сроках и почти дошла
до выкатки. Любой найденный риск теперь стоит дорого, потому что он появился в
разговоре слишком поздно.
```

Smoke rewrites:

```text
Bad: Это не просто инструмент, это новая культура работы.
Better: Инструмент стал важен, когда изменил повседневную работу команды:
появился общий способ пробовать, ошибаться и возвращаться назад без большой
цены.

Bad: Когда команда поздно пишет релиз-ноты, это может привести к слабой
коммуникации.
Better: Если команда впервые формулирует пользу для клиента во время
релиз-нотов, коммуникация почти неизбежно получается внутренней.

Bad: Это не про скорость, это про качество решений.
Better: Скорость здесь вторична. Главный вопрос в том, насколько рано команда
видит риск и может изменить решение без большой политической цены.

Bad: Фича не только помогает пользователям, но и улучшает удержание.
Better: Фича помогает пользователям быстрее закончить настройку и чаще
вернуться к сценарию на следующий день.

Bad: Команда писала релиз-ноты, стараясь объяснить ценность.
Better: Команда писала релиз-ноты и пыталась объяснить ценность для клиента.
```

## Knowledge Updates

After producing a plan, outline, or draft, recommend updates to:

- `knowledge/TOPICS.md`
- `knowledge/RESEARCH_NOTES.md`
- `knowledge/FRAMEWORKS.md`
- `knowledge/ANALOGIES.md`
- `knowledge/FAILURES.md`
- `knowledge/OUTPUTS.md`

Real draft files should live in `outputs/`.

Do not update files unless the user asked for implementation in the current
turn.

## Examples

User: "Сделай Telegram-пост про почему SQL жив 50 лет."

Expected behavior:

- infer `telegram_note`;
- infer archaeology of engineering decisions;
- run at least a light research pass;
- produce an output plan and Russian draft only if readiness is sufficient;
- run the Russian anti-pattern pass before returning the draft.

User: "Хочу LinkedIn-пост про KPI, но через инженерное управление."

Expected behavior:

- infer `linkedin_post`;
- infer engineering of management;
- preserve professional tone without thought-leadership theater;
- remove English-calque Russian syntax.

User: "Давай незавершённое исследование: я неделю думаю про AI agents."

Expected behavior:

- infer `unfinished_research`;
- preserve open questions and uncertainty;
- avoid pretending the conclusion is mature.

User: "Сделай failure analysis про продукт, который умер."

Expected behavior:

- infer `failure_analysis`;
- search for mechanism, constraints, and weak explanations;
- avoid moralizing.

User: "Вот draft, гуманизируй под мой продуктовый стиль."

Expected behavior:

- run humanizer pass;
- reduce generic AI rhythm;
- apply `RUSSIAN_ANTI_PATTERNS.md`;
- add product/JTBD lens where useful;
- do not invent missing research.
