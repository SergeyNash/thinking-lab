# HUMANIZER RULES

This document is the Thinking Lab adapter for the portable humanizer layer.

Universal Russian humanizer rules live in:

- `humanizer/HUMANIZER_CORE.md`
- `humanizer/MODES.md`
- `humanizer/VOICE_ADAPTERS.md`

This file keeps the old `communication/HUMANIZER_RULES.md` path stable for
Thinking Lab and adds only project-specific overrides.

---

## 1. Purpose

Thinking Lab uses the portable humanizer to make Russian drafts sound more
human, specific, and natural.

Thinking Lab-specific writing still has extra constraints:

- research quality comes before style;
- evidence and uncertainty must survive editing;
- product/JTBD voice should remain visible when useful;
- public outputs default to Russian;
- Telegram, LinkedIn, essay, working note, unfinished research, and failure
  analysis each have their own communication constraints;
- LinkedIn theater is forbidden.

This adapter does not replace the portable humanizer. It layers Thinking Lab
rules on top of it.

---

## 2. Priority Order

Apply rules in this order:

1. preserve reasoning, evidence, uncertainty, and limits;
2. preserve Thinking Lab voice;
3. apply `communication/RUSSIAN_ANTI_PATTERNS.md`;
4. apply `skills/humanize-ru` (register + AI-marker diagnosis and cleanup);
5. apply `humanizer/HUMANIZER_CORE.md`;
6. apply this Thinking Lab adapter;
7. adapt to the selected output format from `communication/FORMATS.md`.

If a humanizer rule would remove important uncertainty or make a weak idea
sound stronger than it is, return to reasoning instead of polishing.

---

## 3. Thinking Lab Overrides

### Research Before Style

Do not use the humanizer to compensate for missing reasoning.

If the draft has no clear question, mechanism, limit, or rejected weak
explanation, mark the gap and route the work back to modules or research notes.

### Product/JTBD Voice

Thinking Lab public writing should often sound like a product-minded engineer
or product leader thinking in public.

Keep the reader close to:

- user job;
- friction;
- cost of action;
- risk;
- coordination;
- tradeoff;
- behavior change.

Do not paste JTBD vocabulary mechanically. Use it only when it clarifies the
text.

### Platform Behavior

Use portable humanizer modes as a base, then apply Thinking Lab formats:

- `telegram_note`: use `general` or `product_content`, allow more spoken rhythm;
- `linkedin_post`: use `product_content`, keep professional clarity, remove
  performance and self-branding;
- source-based LinkedIn overview: use `dry_overview`, keep the source, case,
  result, and final implication visible;
- `essay`: use `essay`, preserve continuity and evidence;
- `working_note`: use `general`, keep uncertainty visible;
- `unfinished_research`: use `general`, do not force closure;
- `failure_analysis`: use `business` or `essay`, stay precise and non-moralizing.

### Anti-LinkedIn Theater

Remove:

- artificial vulnerability;
- personal-brand drama;
- "I learned 5 things";
- "every leader should know";
- engagement bait;
- motivational packaging.

Professional does not mean staged.

---

## 4. Thinking Lab Humanizer Pass

Before returning a public-facing Thinking Lab draft:

1. Check readiness: question, mechanism, evidence level, limit.
2. Run `communication/RUSSIAN_ANTI_PATTERNS.md`.
3. Run `skills/humanize-ru` for register-safe AI-marker removal (default
   register for articles: Публицистический).
4. Run `humanizer/HUMANIZER_CORE.md` with the closest mode from
   `humanizer/MODES.md`.
5. Apply this adapter: product/JTBD voice, output format, anti-LinkedIn theater.
6. Confirm that the draft still sounds like Thinking Lab, not generic prose.

Preferred Thinking Lab rewrite shape:

```text
artifact or situation -> tension -> mechanism -> product/system consequence -> principle
```

---

## 5. Summary

The short version:

> `humanize-ru` removes AI markers without breaking register.
> Portable humanizer makes the Russian alive.
> Thinking Lab adapter keeps the research, product lens, and output discipline.
