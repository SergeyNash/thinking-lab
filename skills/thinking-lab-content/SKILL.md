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
- `communication/HUMANIZER_RULES.md`
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
draft -> STYLE.md -> RUSSIAN_ANTI_PATTERNS.md -> HUMANIZER_RULES.md -> product/JTBD voice check -> revised draft
```

Do not invent research during humanization. If the reasoning is weak, say so.

Always run the Russian anti-pattern pass and the adapted humanizer pass before
returning the revised draft.

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
- avoid bureaucratic Russian and promotional product gloss;
- avoid abstract placeholder product examples when a real product situation can
  make the point;
- do not polish weak reasoning into confident prose.

Use `communication/RUSSIAN_ANTI_PATTERNS.md` as the high-priority reference.
Use `communication/HUMANIZER_RULES.md` as the broader adapted humanizer
reference.

## Drafting and Humanization Pipeline

Use this pipeline for public-facing Russian drafts:

```text
draft -> Russian anti-pattern pass -> humanizer pass -> product/JTBD voice check -> final readiness check
```

The pipeline must preserve:

- research question;
- mechanism;
- evidence level;
- uncertainty;
- limit;
- product/JTBD lens;
- Thinking Lab voice.

The pipeline must not:

- invent missing research;
- strengthen claims without evidence;
- add intentional mistakes;
- break punctuation to sound human;
- turn the text into LinkedIn theater.

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

## Humanizer Pass

After the anti-pattern pass, apply `communication/HUMANIZER_RULES.md`.

Scan for:

- era cliches: "в современном мире", "в эпоху цифровой трансформации";
- inflated claims: "меняет правила игры", "революция", "важный урок для всех";
- promotional gloss: "бесшовный опыт", "на одной странице";
- false universality: "каждая команда", "любой лидер";
- bureaucratic Russian: "является", "данный", "осуществление",
  "реализация";
- passive voice that hides responsibility;
- AI signposting: "важно отметить", "стоит подчеркнуть";
- generic rule-of-three phrases: "быстро, удобно и надёжно";
- filler words: repeated "в целом", "по сути", "на самом деле";
- typographic habits: dash overload, semicolons, inline headers with colons;
- assistant artifacts: "Надеюсь, это помогло", sycophancy, invitations to
  continue.

Rewrite toward:

```text
concrete situation -> visible friction -> mechanism -> product/user consequence -> principle
```

Do not use the humanizer as an AI detector. Use it as an editing pass for more
specific, causal, author-like Russian.

## Smoke Rewrites

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
Better: Скорость здесь вторична. Команде важнее увидеть риск достаточно рано,
пока решение ещё можно изменить без большой политической цены.

Bad: Фича не только помогает пользователям, но и улучшает удержание.
Better: Фича помогает пользователям быстрее закончить настройку и чаще
вернуться к сценарию на следующий день.

Bad: Команда писала релиз-ноты, стараясь объяснить ценность.
Better: Команда писала релиз-ноты и пыталась объяснить ценность для клиента.

Bad: В современном мире технологии не стоят на месте.
Better: Git интересен как система, которая сделала промежуточное состояние
нормальной частью работы.

Bad: Данный подход является эффективным.
Better: Этот подход работает, если команда видит риск до разработки.

Bad: Решение простое; код сразу заработает.
Better: Решение простое, и код сразу заработает.

Bad: Скорость: продукт работает быстро.
Better: Скорость важна только тогда, когда пользователь быстрее завершает свою
работу.

Bad: Надеюсь, это помогло.
Better: [remove]
```

## Output-Type Adaptation

Apply humanizer rules differently by output type:

- `telegram_note`: allow more spoken rhythm and mild roughness, but no
  intentional mistakes;
- `linkedin_post`: keep professional clarity, remove LinkedIn theater;
- `essay`: prefer cleaner structure and calmer transitions;
- `working_note`: allow visible uncertainty and unfinished thought;
- `unfinished_research`: preserve open questions;
- `failure_analysis`: stay precise and non-moralizing.

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
- run the Russian anti-pattern pass and humanizer pass before returning the
  draft.

User: "Хочу LinkedIn-пост про KPI, но через инженерное управление."

Expected behavior:

- infer `linkedin_post`;
- infer engineering of management;
- preserve professional tone without thought-leadership theater;
- remove English-calque Russian syntax and humanizer markers.

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
- apply `HUMANIZER_RULES.md`;
- add product/JTBD lens where useful;
- do not invent missing research.
