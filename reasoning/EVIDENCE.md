# EVIDENCE

This document defines how Thinking Lab works with evidence.

Evidence does not eliminate uncertainty.
It helps the system decide how much confidence an explanation deserves.

Thinking Lab should use evidence to improve explanations, not to decorate
opinions.

---

## 1. Evidence Roles

Different materials play different roles.

Do not treat all of them as proof.

### Observation

Something noticed in a system.

Example:

> Teams often create workarounds when a security process is too slow.

An observation can start research.
It does not prove a principle.

### Illustration

An example used to make an idea easier to understand.

Illustrations are useful for communication.
They are weak as evidence.

### Example

A concrete instance of a pattern.

One example can generate a hypothesis.
It rarely proves it.

### Case

A richer example with context, constraints, decisions, and consequences.

Cases are stronger than isolated examples because they preserve more of the
system around the event.

### Source

External material that supports, challenges, or contextualizes a claim.

Sources may include:

- documentation;
- historical records;
- books;
- papers;
- talks;
- post-mortems;
- interviews;
- public data;
- code;
- official statements.

### Counterexample

A case that weakens, narrows, or breaks a hypothesis.

Counterexamples are high-value evidence.

### Pattern

A repeated structure across multiple examples or cases.

Patterns are stronger when they appear across different contexts.

### Principle

A compressed explanation that transfers across domains and has known limits.

A principle should be supported by patterns, cases, mechanisms, and
counterexample checks.

---

## 2. Evidence Strength

Evidence can be weak, moderate, or strong.

### Weak Evidence

Weak evidence includes:

- one anecdote;
- one personal experience;
- one convenient example;
- a metaphor;
- a popular opinion;
- a single success story;
- a quote without context;
- a correlation without mechanism.

Weak evidence can be useful for generating hypotheses.

It should not carry strong conclusions.

### Moderate Evidence

Moderate evidence includes:

- multiple examples in one domain;
- a detailed case study;
- a post-mortem with context;
- a well-documented historical account;
- repeated personal observations;
- a clear mechanism supported by examples.

Moderate evidence can support a working hypothesis.

It should still be challenged.

### Strong Evidence

Strong evidence includes:

- repeated patterns across domains;
- independent sources pointing to the same mechanism;
- counterexamples that were considered and survived;
- historical context plus mechanism plus consequences;
- data that matches a plausible causal explanation;
- cases where alternative explanations were tested.

Strong evidence does not create certainty.

It earns higher confidence.

---

## 3. Personal Experience

Personal experience is valuable.

It provides:

- concrete observations;
- tacit knowledge;
- pattern recognition;
- real constraints;
- lived consequences;
- questions worth asking.

But personal experience is not proof.

It is shaped by:

- role;
- domain;
- organization;
- time period;
- incentives;
- memory;
- selection bias;
- limited visibility.

Use personal experience to generate hypotheses and identify mechanisms.

Do not present it as universal evidence unless supported by other sources or
cases.

---

## 4. Case Studies

Case studies are useful when they include context.

A useful case should answer:

- What happened?
- Who was involved?
- What constraints mattered?
- What alternatives existed?
- What decision was made?
- What changed after the decision?
- What failed?
- What survived?
- What evidence is missing?

A weak case study only says:

> Company X did Y and succeeded.

A stronger case study explains:

> Company X faced constraints A and B, chose Y over Z, changed behavior C, and
> produced outcome D under conditions E.

Thinking Lab should prefer cases with constraints and consequences.

---

## 5. Historical Evidence

Historical evidence is essential for avoiding hindsight.

When using history, ask:

- What was known at the time?
- What was uncertain?
- What alternatives were available?
- What constraints shaped decisions?
- What did later success make look inevitable?
- Which sources were written after the winner was known?

History should restore uncertainty.

If a historical explanation makes the outcome look obvious from the start, it is
probably too clean.

---

## 6. Data

Data can strengthen evidence.

But data does not explain itself.

When using data, ask:

- What exactly is being measured?
- What is not being measured?
- Who collected the data?
- For what purpose?
- What incentives shaped the data?
- What changed over time?
- Is there a plausible mechanism?
- Are there alternative explanations?

Data without mechanism can mislead.

Mechanism without data can overreach.

The strongest explanations often combine both.

---

## 7. Expert Claims

Expert claims can be useful, but they are not automatically evidence.

Ask:

- What is the expert's domain?
- Are they speaking from evidence or opinion?
- Do they have incentives?
- Are they describing a case, a pattern, or a belief?
- Do other sources agree?
- What would a critic say?

Expertise helps.

It does not remove the need for reasoning.

---

## 8. Official Documentation and Statements

Official sources are useful for understanding intended design, public rationale,
constraints, and declared goals.

But official sources often describe:

- what a system claims to do;
- why creators say it exists;
- how it wants to be understood;
- what it chooses to reveal.

They may hide:

- failed alternatives;
- internal politics;
- accidental decisions;
- trade-offs;
- consequences;
- user workarounds.

Use official sources as evidence of stated intent and design.

Do not treat them as complete explanations of real behavior.

---

## 9. Counterexamples

Counterexamples are one of the strongest tools in Thinking Lab.

They can:

- disprove a claim;
- narrow a principle;
- reveal missing constraints;
- show domain limits;
- expose hidden assumptions;
- force better explanation.

When a counterexample appears, do not ignore it.

Ask:

- Does it break the hypothesis?
- Does it narrow the hypothesis?
- Does it reveal a boundary condition?
- Is it actually a different system?
- Does it show that the mechanism was wrong?

A principle that survives counterexamples with clearer limits becomes stronger.

---

## 10. Negative Evidence

Absence of evidence can matter.

Examples:

- no clear examples outside one domain;
- no historical support for a popular explanation;
- no signs that users behave as the theory predicts;
- no counterfactual where the principle seems to work;
- no independent sources confirming the mechanism.

Negative evidence should not automatically reject a hypothesis.

But it should lower confidence.

---

## 11. Evidence and Confidence Levels

Evidence should map to confidence.

### Question

Supported by curiosity, tension, or observation.

No conclusion yet.

### Intuition

Supported by personal experience or a small number of examples.

Useful, but weak.

### Hypothesis

Supported by a structured explanation and some evidence.

Needs critique.

### Working Theory

Supported by multiple cases, plausible mechanism, and counterexample checks.

Still provisional.

### Principle

Supported by repeated patterns, transfer across domains, and known limits.

Strong, but not universal.

---

## 12. Evidence Notes Format

When collecting evidence, use a simple format:

```markdown
## Evidence Item

Type:
Source:
Claim supported:
Claim weakened:
Context:
Strength:
Limitations:
Open questions:
```

The goal is not bureaucracy.

The goal is to make evidence reusable and challengeable.

---

## 13. Evidence Quality Checks

Before using evidence to support a claim, ask:

- Is this evidence or only an illustration?
- What claim does it support?
- What claim does it not support?
- What context is missing?
- Is the source independent?
- Is there a plausible mechanism?
- Are there alternative explanations?
- What would weaken this evidence?
- Is there a counterexample?
- Does this evidence justify the confidence level?

If evidence cannot answer these questions, use it carefully.

---

## 14. Common Evidence Failure Modes

Avoid:

- using one example as proof;
- treating analogy as evidence;
- quoting experts without context;
- using data without mechanism;
- using mechanism without evidence;
- ignoring counterexamples;
- selecting only cases that fit the thesis;
- confusing popularity with correctness;
- confusing survival with quality;
- confusing official intent with real behavior;
- presenting personal experience as universal law.

These failure modes are especially dangerous because they often produce
convincing writing.

---

## 15. Summary

Thinking Lab uses evidence to calibrate confidence.

Evidence should clarify:

- what is known;
- what is plausible;
- what is uncertain;
- what is contradicted;
- what transfers;
- what remains only a story.

The short version:

> Evidence does not exist to make an idea look strong.
> Evidence exists to show how strong the idea actually is.
