# TOPICS

This document stores candidate investigations for Thinking Lab.

Topics are not content ideas by default.
They are research opportunities.

---

## 1. Purpose

`TOPICS.md` helps Thinking Lab track questions worth investigating.

A topic belongs here when it may reveal a transferable principle behind a
concrete artifact, system, process, failure, or recurring pattern.

---

## 2. What Belongs Here

Add a topic when it has:

- a concrete artifact or phenomenon;
- a reason it is interesting;
- an explanatory question;
- potential for transfer across domains.

Examples of valid topic forms:

- Why did a system survive?
- Why did a process degrade?
- Why did a tool change behavior?
- Why did a metric start lying?
- Why did an organization become slow?
- Why did a practice keep reappearing?

Topics may be approached through one or more research optics:

- archaeology of engineering decisions;
- engineering of management;
- cross-domain analogies;
- mental models;
- future of engineering;
- unfinished investigations;
- failure analysis;
- principle extraction.

These are not content categories. They are ways to investigate the same
underlying question from different angles.

---

## 3. What Does Not Belong Here

Do not add:

- generic content ideas;
- news reactions without a research question;
- topics whose only purpose is posting frequency;
- shallow "tips" formats;
- items with no concrete artifact or phenomenon;
- ideas that belong directly in `OUTPUTS.md`.

---

## 4. Topic Template

Use this lightweight format:

```markdown
## <Title>

Status:
Artifact / domain:
Research optics:
Why interesting:
Initial question:
Possible principle:
Related frameworks:
Related analogies:
Next action:
```

Keep entries short.

Detailed work belongs in `RESEARCH_NOTES.md`.

---

## 5. Status Values

- `candidate`: worth considering;
- `active`: currently being researched;
- `paused`: useful but not current;
- `rejected`: not worth pursuing now;
- `published`: produced an output;
- `archived`: kept for context.

---

## 6. Relationship to Reasoning

Topics should follow `reasoning/RESEARCH_METHOD.md`.

A good topic should become a research question, not only a title.

When a topic becomes active, create or update a research note using
`RESEARCH_NOTES.md`.

---

## 7. Seed Examples

These examples are placeholders for future research, not completed work.

## Why did Git win?

Status: active  
Artifact / domain: version control, software engineering  
Research optics: archaeology of engineering decisions, cross-domain analogy,
mental model, principle extraction
Why interesting: Git became a durable standard, but obvious explanations such as
"because GitHub" are incomplete.  
Initial question: Why did Git fit the real behavior of software development so
well?  
Possible principle: Behavior changes when trying, failing, learning, and
recovering become cheaper than avoiding uncertainty or making large upfront
commitments.  
Related frameworks: cost structures, cost of reversible experimentation,
reversibility, feedback loops  
Related analogies: organizational processes, product experimentation, security
paved roads, AI workflows  
Next action: draft Telegram note first; LinkedIn post later.
