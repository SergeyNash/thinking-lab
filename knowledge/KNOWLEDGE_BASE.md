# KNOWLEDGE BASE

This document defines the memory model of Thinking Lab.

The Knowledge Layer stores research memory, not content inventory.

It keeps the questions, notes, frameworks, analogies, failures, and outputs that
allow future investigations to build on previous thinking.

---

## 1. Purpose

The Knowledge Layer exists so Thinking Lab does not start from zero every time.

It should preserve:

- candidate topics;
- working research notes;
- reusable frameworks;
- cross-domain analogies;
- rejected hypotheses;
- failed explanations;
- published and unpublished outputs;
- open questions;
- method feedback.

It should help future work answer:

- What have we already considered?
- What explanations were rejected?
- Which patterns keep appearing?
- Which frameworks are reusable?
- Which topics are ready for research?
- Which outputs came from which investigations?

---

## 2. What Belongs Here

The Knowledge Layer stores materials that may be reused by future research.

It includes:

- research questions;
- evidence notes;
- source references;
- examples and cases;
- patterns;
- principles;
- reusable distinctions;
- analogies;
- counterexamples;
- abandoned drafts;
- publication records.

The layer should preserve thinking context, not only polished conclusions.

---

## 3. What Does Not Belong Here

The Knowledge Layer should not become:

- a dump of random links;
- a publication queue only;
- a folder of finished articles;
- a database of facts without interpretation;
- a replacement for `RESEARCH_METHOD.md`;
- a second copy of philosophy or epistemology;
- a place for rules that belong in higher layers.

If a note defines how Thinking Lab should think, it probably belongs in
`reasoning/`.

If it defines what Thinking Lab believes, it probably belongs in `identity/`.

If it describes how to write, it probably belongs in `communication/`.

---

## 4. Documents in This Layer

The v0.1 Knowledge Layer contains:

- `TOPICS.md`: candidate investigations and their status.
- `RESEARCH_NOTES.md`: working research note format.
- `FRAMEWORKS.md`: reusable models and conceptual tools.
- `ANALOGIES.md`: cross-domain analogies treated as hypotheses.
- `FAILURES.md`: rejected hypotheses and failed investigations.
- `OUTPUTS.md`: published and unpublished artifacts.

These documents are intentionally lightweight.

They define where memory lives before any automation exists.

---

## 5. Relationship to Reasoning

The Knowledge Layer inherits from the Reasoning Layer.

It should follow:

- `reasoning/EPISTEMOLOGY.md` for confidence and explanation quality.
- `reasoning/SYSTEMS.md` for system concepts and analysis vocabulary.
- `reasoning/RESEARCH_METHOD.md` for investigation flow.
- `reasoning/EVIDENCE.md` for evidence classification.

Knowledge should not silently redefine these rules.

If repeated knowledge work reveals a weakness in the method, the feedback should
move upward into the Reasoning Layer.

---

## 6. Minimal Knowledge Item

Any reusable knowledge item should preserve at least:

```markdown
## <Title>

Type:
Status:
Source or origin:
Related question:
Why it matters:
Current confidence:
Links:
Next action:
```

This is not a universal schema.

It is a minimum reminder that knowledge should remain traceable.

---

## 7. Status Values

Use simple status values:

- `candidate`: worth considering later;
- `active`: currently being worked on;
- `paused`: useful but not moving now;
- `rejected`: considered and intentionally set aside;
- `published`: turned into public output;
- `archived`: preserved for context, not active.

Avoid complex workflow states until real usage demands them.

---

## 8. Summary

The Knowledge Layer is the memory of Thinking Lab.

It stores reusable thinking, not just finished content.

The short version:

> If future research should remember it, the Knowledge Layer should know where
> it lives.
