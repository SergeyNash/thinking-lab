# RESEARCH NOTES

This document defines how working investigations are stored.

Research notes are the main bridge between the Research Method and the Knowledge
Layer.

---

## 1. Purpose

`RESEARCH_NOTES.md` keeps active and archived investigations traceable.

A research note should preserve:

- the original question;
- system boundary;
- context;
- competing hypotheses;
- evidence;
- objections;
- candidate principle;
- transfer tests;
- output decision.

---

## 2. What Belongs Here

Use research notes for:

- active investigations;
- paused investigations;
- unpublished research memos;
- archived failed investigations;
- source-backed explorations;
- topics that have moved beyond a short backlog entry.

---

## 3. What Does Not Belong Here

Do not use research notes for:

- polished posts;
- raw link dumps;
- generic notes without a research question;
- reusable frameworks that belong in `FRAMEWORKS.md`;
- analogies that belong in `ANALOGIES.md`;
- rejected hypotheses without enough research context, which may belong in
  `FAILURES.md`.

---

## 4. Minimal Research Note Template

This template follows `reasoning/RESEARCH_METHOD.md`.

```markdown
# Research: <artifact or question>

Status:
Started:
Last updated:
Related topic:
Potential output:

## 1. Initial Question

## 2. Why This Is Interesting

## 3. System Boundary

## 4. Context

## 5. Competing Hypotheses

## 6. Cost Structure

## 7. Evidence

## 8. Counterexamples and Objections

## 9. Candidate Principle

## 10. Transfer

## 11. Output Decision

## 12. Open Questions
```

The template may be shortened for small investigations.

It should not be expanded into bureaucracy unless the research needs it.

---

## 5. Evidence Handling

Evidence in research notes should follow `reasoning/EVIDENCE.md`.

When possible, mark evidence as:

- observation;
- illustration;
- example;
- case;
- source;
- counterexample;
- pattern.

Do not treat all notes as equal evidence.

---

## 6. Research Runs

This section stores compact research runs.

## Research: Why did Git win?

Status: completed manual v0.1 run  
Started: 2026-06-29  
Last updated: 2026-06-29  
Related topic: Why did Git win?  
Potential output: Telegram note first; LinkedIn post later; essay possible after
source-backed research.

### 1. Initial Question

What made Git fit the real behavior of software development so well?

### 2. Why This Is Interesting

Git became a durable standard, but common explanations such as speed, Linus
Torvalds, or GitHub are incomplete. The deeper question is why Git's model fit
the structure of development work.

### 3. System Boundary

Focus first on Git as version control model and collaboration primitive. Treat
GitHub as an adoption amplifier, not as the whole explanation.

### 4. Context

Git appeared in a world with existing version control systems: CVS, Subversion,
Perforce, BitKeeper, Mercurial, Bazaar, Monotone, and others.

The initial pressure came from Linux kernel development: distributed
contributors, high change volume, trust boundaries, need for speed, local work,
and history integrity.

### 5. Competing Hypotheses

- Git won because it was fast.
- Git won because Linus created it.
- Git won because GitHub made it popular.
- Git won because distributed version control is better.
- Git won because its model matched the real behavior of software development.

### 6. Cost Structure

Git made several important behaviors cheaper:

- branching;
- local commits;
- parallel work;
- inspecting history;
- comparing changes;
- throwing away experiments;
- recovery after mistakes;
- asynchronous coordination.

### 7. Evidence

Current evidence level: conceptual and historical sketch, not yet
source-backed.

Evidence still needed:

- timeline of Git after the BitKeeper/Linux conflict;
- design goals and constraints from early Git history;
- comparison with Mercurial, Bazaar, Monotone, SVN, CVS, and BitKeeper;
- GitHub's role in adoption and workflow standardization.

### 8. Counterexamples and Objections

Important objections:

- GitHub may explain more adoption than architectural-fit framing admits.
- Git is not easy at the UX or beginner mental-model level.
- Other DVCS tools also lowered experimentation cost.
- Small centralized teams may not need Git's complexity.
- Speed and integrity may be historically more central than experimentation.

### 9. Candidate Principle

Behavior changes when trying, failing, learning, and recovering become cheaper
than avoiding uncertainty or making large upfront commitments.

Narrower Git version:

Git lowered the cost of experimentation and recovery in an environment where
parallel work, mistakes, and partial trust are normal.

### 10. Transfer

Strong transfer:

- product experiments with clear feedback;
- security paved roads and secure defaults;
- AI workflows with evaluation and review.

Moderate transfer:

- organizational process experiments;
- personal thinking and writing systems.

Transfer limits:

- irreversible decisions;
- weak feedback;
- high verification cost;
- political or social rollback;
- cheap experimentation becoming noise.

### 11. Output Decision

Successful manual run.

Create two draft candidates from the same research:

1. Telegram note first.
2. LinkedIn post later.

Do not create essay yet.
Essay remains possible after stronger historical and source-backed research.

### 12. Open Questions

- Which alternatives should be compared?
- How much of Git's success belongs to Git itself versus GitHub?
- Which historical sources best describe early Git design constraints?
- How should the LinkedIn version avoid thought-leadership tone?
