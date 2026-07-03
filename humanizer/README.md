# Portable Russian Humanizer

This layer defines reusable Russian editing rules that can be used outside
Thinking Lab.

It is not a research system, content strategy, or platform workflow. It is a
portable layer for making Russian text more natural, specific, and human while
preserving the author's meaning.

---

## What It Does

The humanizer helps edit:

- articles;
- posts;
- book chapters;
- business texts;
- essays;
- chat replies;
- drafts that sound too generic or AI-like.

It removes common problems:

- bureaucratic wording;
- English-calque syntax;
- empty intensifiers;
- over-polished rhythm;
- artificial contrast;
- unnecessary lists and headings;
- assistant-like endings;
- typographic habits that make prose feel generated.

---

## What It Does Not Do

The humanizer does not:

- invent missing arguments;
- replace editing judgment;
- add intentional mistakes;
- break grammar to sound human;
- define a product voice;
- run Thinking Lab research;
- decide whether a text should be published.

Project-specific rules belong in voice adapters.

---

## Core Documents

- `HUMANIZER_CORE.md` contains reusable Russian editing rules.
- `MODES.md` explains how to apply those rules to different kinds of text.
- `VOICE_ADAPTERS.md` explains how to layer a project or author voice on top.

Thinking Lab uses this layer through `communication/HUMANIZER_RULES.md`, which
adds research-first and product/JTBD constraints.

---

## Use As Codex Skill

For Codex usage outside Thinking Lab, use the self-contained skill bundle:

```text
skills/russian-humanizer/
  SKILL.md
  agents/openai.yaml
  references/HUMANIZER_CORE.md
  references/MODES.md
  references/VOICE_ADAPTERS.md
```

To install it globally, copy the whole folder to:

```text
%USERPROFILE%\.codex\skills\russian-humanizer
```

After opening a new Codex thread, you can ask:

```text
Use russian-humanizer.
Mode: fiction.
Humanize this chapter while preserving plot, atmosphere, and author voice.
```

For business text:

```text
Use russian-humanizer.
Mode: business.
Make this memo clearer and more human, remove канцелярит, and preserve facts.
```

For essays:

```text
Use russian-humanizer.
Mode: essay.
Make this article less AI-like, preserve the argument, and keep the author's
position.
```

This does not require Thinking Lab. Thinking Lab is needed only for research
flow, content orchestration, product/JTBD voice, and output decisions.

---

## Basic Use

1. Identify the text mode: `general`, `product_content`, `fiction`,
   `business`, `essay`, or `chat_reply`.
2. Preserve the original meaning and author intent.
3. Apply `HUMANIZER_CORE.md`.
4. Apply a project-specific voice adapter, if one exists.
5. Return the revised text and mention any meaning-level weaknesses.

The default principle:

> Make the text more specific, more causal, and more author-like.
> Do not make it messy for the sake of sounding human.
