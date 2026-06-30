# MODULES

This document defines the Reasoning Modules of Thinking Lab.

Reasoning Modules are cognitive functions.
They are not personalities, agents, or the architecture itself.

Each module performs one kind of thinking and produces traceable intermediate
artifacts.

---

## 1. Purpose

The Modules Layer turns the research method into reusable reasoning
responsibilities.

It helps Thinking Lab move from:

```text
topic -> question -> context -> critique -> transfer -> synthesis -> output
```

without turning the system into a content factory or a multi-agent toy project.

---

## 2. Shared Rules

All modules inherit from:

- `identity/PHILOSOPHY.md`;
- `reasoning/EPISTEMOLOGY.md`;
- `reasoning/SYSTEMS.md`;
- `reasoning/RESEARCH_METHOD.md`;
- `reasoning/EVIDENCE.md`;
- `DESIGN_PRINCIPLES.md`.

When producing public-facing output, modules also inherit from:

- `communication/WRITING.md`;
- `communication/STYLE.md`;
- `communication/FORMATS.md`.

Prompts are implementation details.

A module may be executed by:

- a human;
- an AI model;
- a checklist;
- a script;
- a future tool.

The responsibility should remain stable even when implementation changes.

---

## 3. Standard Pipeline

The default pipeline is:

```text
Archaeologist
  -> Historian
    -> Opponent
      -> Transfer
        -> Synthesizer
          -> Editor
```

The pipeline is allowed to loop.

Examples:

- If Historian finds that the initial question is historically wrong, return to
  Archaeologist.
- If Opponent breaks the main hypothesis, return to Historian or Archaeologist.
- If Transfer fails, return to Synthesizer and narrow the principle.
- If Editor cannot preserve the idea without flattening it, return to
  Synthesizer.

---

## 4. Module Handoff Model

Each module should produce a handoff note:

```markdown
## Module Handoff

Module:
Input used:
Output produced:
Confidence:
Open questions:
Recommended next module:
What the next module should challenge:
```

Handoffs should be short.

They exist to keep reasoning traceable.

---

## 5. Shared Output Rules

Module outputs may be stored in:

- `knowledge/RESEARCH_NOTES.md`;
- `knowledge/FAILURES.md`;
- `knowledge/ANALOGIES.md`;
- `knowledge/FRAMEWORKS.md`;
- `knowledge/OUTPUTS.md`.

Outputs should distinguish:

- observation;
- hypothesis;
- evidence;
- counterexample;
- analogy;
- principle;
- output decision.

Do not present module output as stable knowledge until it survives critique.

---

## 6. Module Contract Template

Each module document should include:

- Purpose
- What It Does
- What It Does Not Do
- Inputs
- Outputs
- Procedure
- Quality Checks
- Handoff to Next Module
- Failure Modes

This is a contract, not a personality description.

---

## 7. Modules

The v0.1 modules are:

- `archaeologist.md`: turns artifacts into research questions and tensions.
- `historian.md`: reconstructs context, alternatives, and constraints.
- `opponent.md`: attacks weak explanations, evidence, and transfer.
- `transfer.md`: tests whether principles travel across domains.
- `synthesizer.md`: builds a working explanation with mechanism, limits, and
  confidence.
- `editor.md`: prepares a Russian output plan or draft through the
  Communication Layer.

---

## 8. Smoke Test: Why Did Git Win?

Expected module flow:

- Archaeologist identifies the tension: Git is not only a tool, but a system
  that made experimentation cheap.
- Historian asks what existed before Git and which alternatives should be
  compared.
- Opponent attacks "Git won because of GitHub" as incomplete.
- Transfer tests the principle in organizations, product systems, and security.
- Synthesizer formulates a working explanation with limits.
- Editor chooses whether the idea should become a Telegram note, LinkedIn post,
  or essay in Russian.

---

## 9. Summary

Reasoning Modules are replaceable cognitive functions.

The short version:

> Modules do not think instead of the system.
> They isolate responsibilities so the system can think more clearly.
