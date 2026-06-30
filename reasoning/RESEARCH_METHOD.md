# RESEARCH METHOD

This document defines the repeatable research method of Thinking Lab.

The method turns concrete artifacts into transferable principles.

It does not guarantee truth.
It creates a disciplined path from observation to understanding.

---

## 1. Method Shape

The basic movement is:

```text
artifact -> question -> context -> hypotheses -> evidence -> opposition -> principle -> transfer -> output
```

This movement is not always linear.

Research may move backward when a hypothesis fails, a boundary changes, or a
counterexample appears.

The method should be repeatable, but not mechanical.

---

## 2. Stage 1: Start With a Concrete Artifact

Research starts with something specific.

The artifact may be:

- a technology;
- a tool;
- a protocol;
- a product;
- an organization;
- a process;
- a standard;
- a failure;
- a habit;
- a recurring pattern.

The first task is not to explain everything.

The first task is to identify what makes the artifact worth investigating.

Ask:

- What is strange here?
- What survived longer than expected?
- What failed despite looking reasonable?
- What keeps reappearing?
- What behavior changed because this exists?
- What obvious explanation feels incomplete?

Output of this stage:

- research candidate;
- initial question;
- reason why it matters.

---

## 3. Stage 2: Formulate the Research Question

A good research question points toward explanation, not description.

Weak questions:

- What is Git?
- How does SQL work?
- What is Kubernetes?
- What is a KPI?

Stronger questions:

- Why did Git become such a durable system?
- Why has SQL survived multiple generations of databases?
- Why is Kubernetes both hated and successful?
- Why do KPIs start lying?

The question should create tension.

It should suggest that the obvious answer is not enough.

Output of this stage:

- primary research question;
- secondary questions;
- first list of obvious explanations to challenge.

---

## 4. Stage 3: Define the System Boundary

Before explaining a system, define what is being studied.

Ask:

- What is inside the system?
- What is outside?
- What is treated as environment?
- What level are we analyzing?
- What boundary would produce a different explanation?

Example:

Git can be studied as:

- a tool;
- a data model;
- a workflow system;
- a collaboration primitive;
- part of a broader software ecosystem.

Each boundary changes the explanation.

Output of this stage:

- explicit system boundary;
- excluded scope;
- possible alternative boundaries.

---

## 5. Stage 4: Reconstruct Context

Context prevents hindsight.

Research should reconstruct the world in which the artifact appeared or
persisted.

Ask:

- What existed before?
- What alternatives were available?
- What constraints mattered at the time?
- What failures or frustrations created demand?
- What assumptions did people have?
- What trade-offs looked acceptable then?
- What was scarce, expensive, risky, or slow?

Output of this stage:

- historical context;
- constraints;
- alternatives;
- environmental conditions.

---

## 6. Stage 5: Generate Competing Hypotheses

Do not start with one favored explanation.

Generate multiple possible explanations.

Examples:

- It won because it was technically better.
- It won because of timing.
- It won because of ecosystem effects.
- It won because alternatives had worse trade-offs.
- It won because it matched the real behavior of users.
- It survived because switching costs became too high.

The goal is not to list everything.

The goal is to avoid falling in love with the first elegant explanation.

Output of this stage:

- competing hypotheses;
- expected evidence for each;
- possible weaknesses of each.

---

## 7. Stage 6: Examine Cost Structures

Many systems become understandable when we ask what they make cheap or
expensive.

Ask:

- What behavior did this system make cheaper?
- What behavior did it make more expensive?
- What mistakes became easier to recover from?
- What coordination became easier?
- What behavior became discouraged?
- What hidden cost did it introduce?

This stage often reveals the transferable principle.

Example:

Git lowered the cost of experimentation and recovery.

That changed developer behavior.

Output of this stage:

- cost structure map;
- behavior changes;
- possible principle candidates.

---

## 8. Stage 7: Collect and Classify Evidence

Evidence should be classified by strength and role.

Use categories from `EPISTEMOLOGY.md`:

- observation;
- example;
- case;
- source;
- counterexample;
- pattern;
- principle.

Ask:

- What supports the hypothesis?
- What weakens it?
- What is only illustrative?
- What is actual evidence?
- What is missing?
- What would change our mind?

Output of this stage:

- evidence notes;
- source list;
- counterexamples;
- evidence gaps.

---

## 9. Stage 8: Attack the Explanation

Every important explanation should be attacked.

Ask:

- Is this explanation too convenient?
- Is it just hindsight?
- Does it confuse correlation with cause?
- Does it depend too much on one example?
- What would an intelligent opponent say?
- What alternative explanation is stronger?
- Where does this explanation fail?

This stage should make the explanation narrower, stronger, or rejected.

Output of this stage:

- critique notes;
- rejected explanations;
- narrowed hypothesis;
- unresolved objections.

---

## 10. Stage 9: Extract the Principle

The principle is the compressed insight that may travel beyond the original
artifact.

A weak principle is just a summary.

Example of a weak principle:

> Git is useful because branching is useful.

A stronger principle:

> Lowering the cost of experimentation changes how a system behaves.

Good principles are:

- abstract enough to transfer;
- concrete enough to be tested;
- linked to evidence;
- limited by context;
- useful outside the original case.

Output of this stage:

- candidate principle;
- supporting mechanism;
- known limits.

---

## 11. Stage 10: Test Transfer

A principle becomes more valuable when it transfers across domains.

Ask:

- Where else does this principle appear?
- Does it work in organizations?
- Does it work in product systems?
- Does it work in security?
- Does it work in AI systems?
- Does it work in markets or sports?
- What changes across domains?
- What remains structurally similar?

Transfer should test structure, not language.

Output of this stage:

- transfer examples;
- transfer limits;
- refined principle.

---

## 12. Stage 11: Decide the Output

Not every research should become a public artifact.

Possible outputs:

- private note;
- research memo;
- unfinished thought;
- Telegram post;
- LinkedIn post;
- essay;
- talk;
- diagram;
- framework;
- archived failed investigation.

Ask:

- Is there something worth sharing?
- Who would benefit from this?
- What format fits the idea?
- Is the explanation mature enough?
- What uncertainty should remain visible?
- Should this stay private for now?

Public-facing outputs should be in Russian by default unless a specific artifact
requires another language.

Output of this stage:

- output decision;
- selected format;
- publication constraints.

---

## 13. Stage 12: Archive Learning

Research should improve the system even when it does not produce publication.

Archive:

- useful notes;
- rejected hypotheses;
- counterexamples;
- source lists;
- reusable frameworks;
- principles;
- open questions;
- reasons not to publish.

Ask:

- What should future research reuse?
- What should future research avoid repeating?
- Did this reveal a method weakness?
- Should any rule move upward into a shared document?

Output of this stage:

- updated knowledge base;
- archived research artifacts;
- method feedback.

---

## 14. Minimal Research Template

Use this when starting an investigation:

```markdown
# Research: <artifact or question>

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

The template is a starting point.

It may be shortened for small investigations or expanded for larger ones.

---

## 15. Method Quality Checks

Before treating research as mature, ask:

- Did we start from a concrete artifact?
- Is the research question explanatory?
- Is the system boundary explicit?
- Did we reconstruct context?
- Did we consider alternatives?
- Did we generate competing hypotheses?
- Did we examine cost structures?
- Did we classify evidence?
- Did we search for counterexamples?
- Did we attack the explanation?
- Did we extract a transferable principle?
- Did we test the transfer?
- Did we decide whether publication is justified?
- Did we archive what was learned?

If several answers are no, the research is probably still early.

---

## 16. Summary

The Thinking Lab research method moves from artifact to principle.

It protects against:

- shallow description;
- hindsight;
- single-cause explanations;
- overconfident analogies;
- publishing before understanding.

The short version:

> Start concrete.
> Reconstruct context.
> Challenge the obvious explanation.
> Find the cost structure.
> Extract the principle.
> Test whether it travels.
