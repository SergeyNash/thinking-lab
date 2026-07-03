# RUSSIAN ANTI-PATTERNS

This document defines high-priority Russian writing patterns that Thinking Lab
avoids by default.

These are not grammar rules. They are style and voice rules for public-facing
Russian writing.

This document has priority over the portable humanizer core in
`humanizer/HUMANIZER_CORE.md`. If a rule conflicts, preserve the Thinking Lab
anti-pattern rule first.

---

## 1. Purpose

`RUSSIAN_ANTI_PATTERNS.md` protects Thinking Lab from the specific Russian
patterns discovered during real draft work with the author.

Use it when drafting, editing, or humanizing public-facing outputs.

The default rule:

> Avoid these patterns unless there is a clear rhetorical reason to keep them.

If a sentence can be rewritten as normal Russian prose, rewrite it.

---

## 2. Pattern: "Это не просто A, это B"

Avoid:

```text
Это не просто инструмент, это новая культура работы.
```

Why it is weak:

- it often inflates a normal idea;
- it creates cheap drama;
- it sounds like a translated marketing line;
- it lets the writer avoid explaining the mechanism.

Rare exception:

- the first part really is a common underestimation;
- the second part reveals a genuinely unexpected layer;
- the sentence has enough concrete follow-up to justify the contrast.

Prefer:

```text
Git стал важен не из-за красивой идеи контроля версий. Он хорошо попал в
повседневную работу разработки: сохранить промежуточное состояние, попробовать
вариант, откатиться и не превращать ошибку в событие для всей команды.
```

Rewrite rule:

- name the concrete situation;
- show what changes in behavior;
- explain the mechanism instead of announcing importance.

---

## 3. Pattern: "Когда/если A, это может привести к B"

Avoid:

```text
Когда команда поздно пишет релиз-ноты, это может привести к слабой
коммуникации.
```

Why it is weak:

- it copies English "when/if A, it can lead to B" syntax;
- Russian does not need the extra "это";
- "может привести" often hides the real cause;
- the sentence sounds bureaucratic and distant.

Prefer:

```text
Если команда впервые формулирует пользу для клиента во время релиз-нотов,
коммуникация почти неизбежно получается внутренней: люди помнят, что сделали,
но не могут коротко объяснить, какую пользовательскую работу улучшили.
```

Rewrite rule:

- remove the empty "это";
- replace "может привести" with the actual causal chain;
- use a direct Russian sentence.

---

## 4. Pattern: "Это не про A, это про B"

Avoid:

```text
Это не про скорость, это про качество решений.
```

Why it is weak:

- it is a calque of English "it's all about";
- it often sounds like a coaching slogan;
- it replaces explanation with a label;
- it makes the author sound generic.

Rare exception:

- a short spoken emphasis may be acceptable in dialogue;
- the text immediately explains the mechanism in concrete terms.

Prefer:

```text
Скорость здесь вторична. Главный вопрос в том, насколько рано команда видит
риск, понимает пользователя и может изменить решение без большой политической
цены.
```

Another acceptable Russian construction:

```text
Дело не в скорости, а в качестве решений.
```

Use it sparingly. Even this construction needs concrete explanation after it.

---

## 5. Pattern: Unnecessary "не только, но и"

Avoid:

```text
Фича не только помогает пользователям, но и улучшает удержание.
```

Why it is weak:

- it creates fake contrast where there is none;
- it makes ordinary addition sound artificially dramatic;
- it is overused in AI-generated Russian.

Use simple coordination when there is no paradox:

```text
Фича помогает пользователям быстрее закончить настройку и чаще вернуться к
сценарию на следующий день.
```

Rare exception:

- the second part genuinely surprises or reverses expectation;
- the sentence needs a real rhetorical lift.

Example of acceptable use:

```text
Этот формат заинтересовал не только инженеров, но и людей из продаж, потому
что впервые связал техническое ограничение с потерянными сделками.
```

---

## 6. Pattern: Misused Participial Adverb Phrases

Avoid random participial adverb phrases when they blur the main action:

```text
Команда писала релиз-ноты, стараясь объяснить ценность.
```

Why it may be weak:

- it can hide which action is primary;
- it often copies loose English sentence structure;
- it adds decorative complexity without improving thought.

Prefer a direct verb structure:

```text
Команда писала релиз-ноты и пыталась объяснить ценность для клиента.
```

When cause or sequence matters, make it explicit:

```text
Команда начала писать релиз-ноты и только тогда заметила, что ценность решения
сформулирована на внутреннем языке.
```

Accept participial adverb phrases only when:

- the added action is truly secondary;
- it adds atmosphere or precision;
- the main action remains clear.

---

## 7. Product Example Rule

Avoid abstract placeholder examples:

```text
добавили настройку
улучшили экран
ускорили сценарий
```

They sound generic unless the text gives real context.

Prefer concrete product situations:

```text
Были запросы от клиентов, обсуждения с продажами, боль в поддержке,
технические ограничения и спор про объём работ. Внутри команда помнит, почему
это делала. Но в релиз-нотах всё ещё трудно объяснить, какую пользовательскую
работу решение улучшило.
```

The reader should recognize a real work situation, not a placeholder.

---

## 8. Anti-Pattern Pass

Before publishing or handing off a draft, scan for:

- "это не просто";
- "это не про";
- "проблема не в том";
- "когда/если ..., это";
- "может привести к";
- unnecessary "не только, но и";
- decorative participial adverb phrases;
- abstract placeholder product examples.

For each match, ask:

- Is this real Russian, or an English-calque explanation?
- Does the contrast reveal something concrete?
- Can this become a direct causal paragraph?
- Can a real product situation replace the placeholder?
- Is the sentence doing thinking, or only sounding polished?

The preferred rewrite is usually:

```text
concrete situation -> what became visible -> why it matters -> what changed
```

After this pass, run the portable humanizer pass from
`humanizer/HUMANIZER_CORE.md`, then apply the Thinking Lab adapter from
`communication/HUMANIZER_RULES.md`.

---

## 9. Summary

The short version:

> Do not announce depth through templates.
> Show the mechanism in normal Russian.
