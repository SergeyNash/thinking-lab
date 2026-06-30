# Transfer

The Transfer module tests whether a principle can travel across domains.

It distinguishes structural transfer from superficial analogy.

---

## 1. Purpose

Transfer checks whether a candidate principle is useful beyond the original
artifact.

It asks:

> Does the same structure appear elsewhere, or are we only reusing language?

---

## 2. What It Does

Transfer:

- identifies possible target domains;
- tests shared structures;
- compares constraints, incentives, feedback loops, and failure modes;
- finds where the principle breaks;
- records useful analogies;
- narrows or strengthens the principle.

---

## 3. What It Does Not Do

Transfer does not:

- treat analogy as proof;
- force every idea into every domain;
- turn principles into slogans;
- ignore domain-specific constraints;
- decide publication format.

---

## 4. Inputs

Typical inputs:

- candidate principle;
- narrowed hypothesis from Opponent;
- system analysis;
- evidence notes;
- analogies from `knowledge/ANALOGIES.md`;
- possible target domains.

---

## 5. Outputs

Expected outputs:

- transfer candidates;
- target domains;
- shared structure;
- where transfer works;
- where it breaks;
- refined principle;
- handoff to Synthesizer.

---

## 6. Procedure

1. State the candidate principle.
2. Identify the mechanism, not just the wording.
3. Choose two or three target domains.
4. Compare constraints and cost structures.
5. Compare incentives and feedback loops.
6. Identify where the analogy breaks.
7. Refine the principle so it transfers only where structure supports it.

---

## 7. Quality Checks

Before handoff, ask:

- Is the transfer structural?
- Are surface similarities separated from mechanisms?
- Are domain limits explicit?
- Does the principle become stronger or narrower?
- Should an analogy be stored in `knowledge/ANALOGIES.md`?
- Is the transfer useful enough for Synthesizer?

---

## 8. Handoff to Next Module

Handoff to Synthesizer should include:

```markdown
Candidate principle:
Mechanism:
Target domains tested:
Where it transfers:
Where it breaks:
Refined principle:
Remaining uncertainty:
```

---

## 9. Failure Modes

Common failures:

- transferring language instead of structure;
- ignoring incentives in the target domain;
- overgeneralizing from one case;
- hiding where the analogy breaks;
- treating a metaphor as evidence.

---

## 10. Smoke Test: Git

For "Why did Git win?", Transfer should test:

- organizations: cheap reversible process experiments;
- product: cheap feature experimentation and rollback;
- security: safe review and recovery paths;
- AI workflows: cheap branching of attempts and evaluation.

It should mark limits:

- human organizations have politics, emotions, and power;
- rollback is often harder outside software;
- not every experiment is safe just because it is cheap.
