# STYLE

This document defines the default public voice of Thinking Lab.

The default public language is Russian.

The default voice is intelligent conversational Russian: clear, alive,
investigative, and human.

Detailed Russian anti-patterns live in
`communication/RUSSIAN_ANTI_PATTERNS.md`.

Portable humanizer rules live in `humanizer/HUMANIZER_CORE.md`.

Register-safe AI-marker removal lives in `skills/humanize-ru/`.

Thinking Lab humanizer overrides live in `communication/HUMANIZER_RULES.md`.

---

## 1. Purpose

`STYLE.md` protects the voice of Thinking Lab.

It helps public writing avoid:

- generic AI tone;
- corporate thought leadership;
- academic fog;
- motivational performance;
- empty structure;
- overconfident expertise;
- English-calque Russian syntax;
- bureaucratic or promotional Russian.

The style should make thinking easier to follow, not make weak ideas look
stronger.

---

## 2. What Belongs Here

This document owns:

- voice;
- tone;
- rhythm;
- Russian language preferences;
- forbidden patterns;
- use of English terms;
- sentence and paragraph feel;
- stylistic quality checks;
- integration order for anti-pattern, humanize-ru, portable humanizer, and
  Thinking Lab adapter passes.

Detailed rewrite rules for high-priority Russian anti-patterns belong in
`RUSSIAN_ANTI_PATTERNS.md`.

Portable humanizer rules belong in `humanizer/HUMANIZER_CORE.md`.

AI-marker diagnosis by register belongs in `skills/humanize-ru/`.

Thinking Lab-specific humanizer rules belong in `HUMANIZER_RULES.md`.

---

## 3. What Does Not Belong Here

Do not use this document for:

- research method;
- evidence rules;
- publication formats;
- platform strategy;
- content calendar;
- topic selection.

---

## 4. Style Priority

Apply writing rules in this order:

1. preserve meaning, evidence, uncertainty, and limits;
2. preserve Thinking Lab product/JTBD voice;
3. apply `RUSSIAN_ANTI_PATTERNS.md`;
4. apply `skills/humanize-ru` (register + AI markers);
5. apply `humanizer/HUMANIZER_CORE.md`;
6. apply `communication/HUMANIZER_RULES.md` as the Thinking Lab adapter;
7. adapt to the selected platform format.

Style must never outrun understanding.

If the idea is weak, return to reasoning instead of polishing the text.

---

## 5. Default Voice

The default voice:

- smart but not pompous;
- conversational but not sloppy;
- precise but not academic;
- curious but not naive;
- confident only where confidence is earned;
- alive, but not theatrical.

It should feel like a person thinking clearly in public.

Not a brand.
Not a guru.
Not a corporate page.
Not a generic AI assistant.

---

## 6. Humanized Product Voice

Public writing should sound like it is written by a product-minded engineer or
product leader who is trying to understand how systems affect real work.

This does not mean adding product jargon everywhere. It means keeping the
reader close to the job, friction, tradeoff, behavior change, and decision
context behind the artifact being studied.

Useful product lenses:

- what job the artifact is hired to do;
- what anxiety, risk, delay, or coordination cost it reduces;
- what behavior it makes cheaper or more expensive;
- what old workaround it replaces;
- what it changes in the team's decision-making;
- where the product or system succeeds despite rough edges;
- where the same principle transfers to product teams, engineering teams,
  security teams, or organizational design.

JTBD is a preferred lens, especially when the artifact can be read as a tool
that helps people make progress under constraints. Use it naturally, not as a
template pasted onto every text.

The reader should feel addressed as a peer: someone who builds products,
makes tradeoffs, works with teams, and understands that tools change behavior
by changing the cost of actions.

---

## 7. Russian Language Policy

Public-facing outputs should be in Russian by default.

English terms are acceptable when they are natural in the domain:

- product;
- security;
- engineering;
- roadmap;
- feedback;
- incident;
- framework;
- agent;
- prompt;
- architecture.

Do not translate terms mechanically if the Russian version sounds artificial.

Do not use English to sound more sophisticated.

Do not keep English corporate slogans when Russian already names the same
thing. Prefer Russian over `customer-centricity`, `stakeholder`, `alignment`,
`churn` as decoration. Domain words stay if they are how the audience actually
speaks (`security`, `комплаенс`, `ЛПР`).

Use the term that makes the thought clearer.

When writing in Russian, do not copy English explanatory syntax. Check
`RUSSIAN_ANTI_PATTERNS.md`, `skills/humanize-ru`, `humanizer/HUMANIZER_CORE.md`,
and `HUMANIZER_RULES.md` before finalizing a public draft.

---

## 8. Rhythm

Prefer readable rhythm:

- short and medium sentences;
- one idea per paragraph when needed;
- enough air between steps of reasoning;
- no dense blocks that hide the point;
- no endless bullet lists when prose would be better.

Lists are useful for structure.

They should not replace thinking.

Avoid overusing very short standalone sentences such as:

- "Это правда.";
- "Особенно GitHub.";
- "Он не простой.";

They can create artificial drama and make the text sound generated. When the
thought is continuous, keep it in a normal paragraph.

Avoid repeated question patterns when prose would sound more human. Do not
stack several lines that all begin with the same phrase if the same idea can be
said as one clear paragraph.

Also avoid common AI-calque patterns in Russian:

- "это не просто A, это B";
- "когда/если A, это может привести к B";
- "это не про A, это про B";
- unnecessary "не только, но и";
- decorative participial adverb phrases.

Detailed examples and rewrite rules live in `RUSSIAN_ANTI_PATTERNS.md`.

---

## 9. Openings

Good openings may begin with:

- a question;
- a contradiction;
- a strange observation;
- an incomplete common explanation;
- a concrete artifact;
- a system behavior;
- a recognizable product situation.

Avoid openings like:

- "В современном мире...";
- "Сегодня поговорим о...";
- "Ни для кого не секрет...";
- "В эпоху цифровой трансформации...";
- "Каждый продуктовый менеджер должен...";
- "Это не просто...";
- "В слайдах это...";
- "На слайде мы...";

These phrases usually signal that the text has not found its real tension yet.
Do not frame Russian work as if decisions live in presentations. Use the real
arena: совещание, защита перед руководством, договор, бэклог, переписка.

---

## 10. Avoid Generic AI Tone

Avoid:

- inflated summaries;
- symmetrical lists everywhere;
- motivational endings;
- obvious conclusions;
- excessive signposting;
- phrases that sound polished but empty;
- fake neutrality;
- confident claims without friction;
- English-calque Russian syntax.

Bad signal:

```text
Это важный урок для всех команд, которые хотят быть эффективнее.
```

Better:

```text
Если система снижает цену ошибки, люди начинают пробовать чаще. Иногда это
важнее, чем сама функция.
```

Before finalizing Russian drafts, run the anti-pattern pass from
`RUSSIAN_ANTI_PATTERNS.md`, then `skills/humanize-ru`, then the portable
humanizer pass from `humanizer/HUMANIZER_CORE.md`, then the Thinking Lab
adapter from `HUMANIZER_RULES.md`.

---

## 11. Avoid LinkedIn Theater

Thinking Lab should not sound like performative thought leadership.

Avoid:

- personal-brand drama;
- artificial vulnerability;
- "I learned 5 things";
- "Here is what every leader should know";
- engagement bait;
- heroic founder tone;
- moralizing.

Professional does not mean staged.

Clear thinking is enough.

---

## 12. Avoid Mechanical Contrast Patterns

Contrast is useful, but it should not become a tic.

Avoid overusing patterns like:

- "not X, but Y";
- "it is not simple";
- "the interesting part is not...";
- "this is true, but...";
- "the problem is not A, the problem is B";
- "not because A, but because B";
- "это не просто A, это B";
- "это не про A, это про B".

These moves can be useful once in a text, especially when they clarify a weak
common explanation. If they appear repeatedly, rewrite the passage as ordinary
reasoning in paragraphs.

The preferred feeling is not a sequence of punchlines. It is a person
explaining how they arrived at a sharper view.

In Russian product writing, avoid translated patterns such as:

```text
Проблема не в том, что A.
Проблема в том, что B.
```

Prefer a causal, concrete explanation:

```text
Со стороны кажется, что безопасность просто тормозит релиз. Но к этому моменту
команда уже выбрала решение, написала код, договорилась о сроках и почти дошла
до выкатки. Любой найденный риск теперь стоит дорого, потому что он появился в
разговоре слишком поздно.
```

The same rule applies to product examples. Do not use abstract placeholder
examples such as "добавили настройку", "улучшили экран", or "ускорили
сценарий" when a concrete product situation would be more human.

See `RUSSIAN_ANTI_PATTERNS.md` for the highest-priority rules,
`skills/humanize-ru` for register-safe AI-marker cleanup, and
`humanizer/HUMANIZER_CORE.md` for the broader portable humanizer pass.
Use `HUMANIZER_RULES.md` only for Thinking Lab-specific overrides.

---

## 13. Do Not Hide Weak Thought Behind Style

If the idea is weak, do not make the prose stronger.

Fix the idea.

Style should clarify:

- the question;
- the mechanism;
- the uncertainty;
- the principle;
- the limit.

Style should not compensate for missing evidence or shallow reasoning.

---

## 14. Useful Moves

Useful stylistic moves are ways of preserving live thinking, not templates to
repeat mechanically.

Prefer moves that:

- name the common explanation before making it more precise;
- show why an artifact matters to a real user or team;
- connect a mechanism to behavior change;
- keep limits visible without turning the text into disclaimers;
- move from concrete work to a transferable principle;
- let the reader follow the reasoning, not just receive a polished conclusion.

If a move starts to sound like a reusable phrase, rewrite it in plainer prose.

---

## 15. Humanizer Pass

First run `skills/humanize-ru` for register-safe AI-marker diagnosis and
cleanup. For Thinking Lab articles and essays, default register is
Публицистический when unsure. Load its references before transforming.

Then the portable humanizer pass removes remaining markers that make Russian
text sound generated or generic.

Use `humanizer/HUMANIZER_CORE.md` to check:

- era cliches;
- inflated importance;
- promotional product language;
- false universality;
- bureaucratic nouns;
- "является", "данный", passive voice;
- AI signposting;
- rule-of-three slogans;
- filler words;
- typographic habits;
- assistant-style closings.

For source-based LinkedIn notes or compact technical reviews, prefer
`dry_overview` mode from `humanizer/MODES.md`: source, case, concrete result,
practical implication. Do not force personal storytelling, product lessons, or
large philosophical framing when the user asks for a dry overview.

Do not intentionally add mistakes.

Do not break punctuation to sound human.

Then use `communication/HUMANIZER_RULES.md` to re-apply Thinking Lab-specific
constraints: research quality, product/JTBD voice, platform behavior, and
anti-LinkedIn theater.

---

## 16. Future Voice Passport

Thinking Lab may later support a local author voice passport, but it is not
part of v0.1.

Future fields may include:

- default form of address;
- default formality level;
- preferred rhythm;
- recurring author phrases;
- banned phrases;
- channel defaults;
- English term tolerance;
- product examples that sound like the author.

Do not create `.humanizer/`, `voice.json`, sessions, or auto-logs until that
layer is explicitly designed.

---

## 17. Minimal Style Checklist

Before publishing, ask:

- Does this sound like a person?
- Is the Russian natural?
- Is the tone calm and alive?
- Does the text sound like a product-minded peer, not a generic narrator?
- Is there a visible job, friction, tradeoff, or behavior change?
- Is there unnecessary expert performance?
- Are English terms used because they clarify?
- Are lists helping the thought?
- Are repeated rhetorical patterns removed or justified?
- Did we run the Russian anti-pattern pass?
- Did we run the humanize-ru AI-marker pass?
- Did we run the portable humanizer pass?
- Did we apply the Thinking Lab humanizer adapter?
- Is uncertainty visible where needed?
- Does the ending avoid motivational packaging?

---

## 18. Summary

The style of Thinking Lab should serve thought.

The short version:

> Write in Russian like a smart person thinking aloud carefully.
> Keep the product/JTBD lens visible when it helps the reader.
> Do not perform expertise.
> Do not let style outrun understanding.
> Do not announce depth through templates.
