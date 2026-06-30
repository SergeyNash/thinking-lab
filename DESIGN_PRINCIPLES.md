# DESIGN PRINCIPLES

This document defines how Thinking Lab should evolve.

`ARCHITECTURE.md` describes what the system is.
`DESIGN_PRINCIPLES.md` describes how the system should change without losing
its identity.

Thinking Lab should remain a research engine.
It should not drift into a content factory, a prompt collection, or a personal
brand routine.

---

## 1. Core Principle

> We are not designing content.
> We are designing the conditions under which good thinking can happen
> repeatedly.

This is the meta-principle behind every other design decision.

The system should be judged by whether it improves understanding, not by how
many outputs it produces.

---

## 2. Layering Principles

### 2.1. Knowledge Flows Downward

General knowledge, constraints, and beliefs should live higher in the system.

Lower layers inherit from higher layers.
They should not silently redefine them.

```text
Identity
  -> Reasoning
    -> Knowledge
      -> Reasoning Modules
        -> Communication
          -> Artifacts
```

If a rule is needed by multiple modules, it probably belongs above the modules.

Examples:

- Philosophy belongs above writing style.
- Evidence rules belong above individual investigations.
- Research method belongs above module prompts.
- Non-goals belong above publication decisions.

### 2.2. Feedback Flows Upward

The system must learn from its own work.

Artifacts, failed explanations, audience reactions, unclear drafts, and rejected
hypotheses should feed back into the system.

```text
Artifacts
  -> Communication
    -> Reasoning Modules
      -> Knowledge
        -> Reasoning
          -> Identity
```

Feedback can improve:

- topic selection;
- examples;
- module behavior;
- writing formats;
- research method;
- evidence rules;
- core philosophy, rarely.

### 2.3. Stability Above, Flexibility Below

The higher a layer is, the more stable it should be.

The lower a layer is, the easier it should be to change.

Identity should change rarely.
Prompts, templates, notes, and output formats can change often.

This protects the project from both rigidity and drift.

---

## 3. Responsibility Principles

### 3.1. One Module, One Cognitive Responsibility

A Reasoning Module should do one kind of thinking well.

Examples:

- Archaeologist finds what is strange or worth investigating.
- Historian reconstructs context and alternatives.
- Opponent attacks weak explanations.
- Transfer tests whether a principle works elsewhere.
- Synthesizer integrates competing explanations.
- Editor turns understanding into clear writing.

If a module starts doing too many things, split it.

If multiple modules need the same rule, move that rule upward.

### 3.2. Modules Are Not Personalities

Reasoning Modules are cognitive functions.

They should not depend on theatrical character design, agent personas, or
fictional behavior.

A module may be implemented by:

- a prompt;
- an AI model;
- a human checklist;
- a script;
- a future tool.

The module's responsibility should survive implementation changes.

### 3.3. Prefer Composition Over Complexity

Complex reasoning should be assembled from simple parts.

Do not build one large module that tries to research, critique, synthesize, and
write at the same time.

Prefer a chain of clear responsibilities:

```text
question -> context -> hypotheses -> critique -> transfer -> synthesis -> writing
```

The chain may change.
The responsibilities should remain explicit.

### 3.4. Every Module Should Be Replaceable

No module should become sacred.

If a better process, prompt, model, or human workflow appears, the module
implementation can change.

What should remain stable is:

- the module's purpose;
- its inputs;
- its outputs;
- the constraints it inherits.

---

## 4. Knowledge Principles

### 4.1. Shared Knowledge Should Not Be Duplicated

If the same idea appears in many prompts, guides, or documents, it belongs in a
higher shared document.

Duplication creates drift.

The system should have one authoritative place for each important rule.

### 4.2. Distinguish Examples From Principles

Examples are not the final product of thinking.

Examples are material used to discover principles.

Good research should move from:

```text
artifact -> context -> explanation -> principle -> transfer
```

The Git example is not only about Git.
It is about the broader principle that lowering the cost of experiment changes
system behavior.

### 4.3. Preserve Failed Explanations

A rejected explanation is useful knowledge.

The system should preserve:

- weak hypotheses;
- failed analogies;
- counterexamples;
- abandoned drafts;
- questions that did not resolve.

This prevents the project from repeating the same shallow explanations later.

### 4.4. Make Conclusions Traceable

Important conclusions should be traceable to:

- initial question;
- context;
- assumptions;
- evidence;
- counterarguments;
- uncertainty;
- final principle.

If a conclusion cannot be traced, it should not be treated as stable knowledge.

---

## 5. Research Principles

### 5.1. Research Before Writing

Writing is a side effect of understanding.

Do not start by asking:

> What can we publish?

Start by asking:

> What do we not understand yet?

Publication should happen only when the investigation produces something worth
sharing.

### 5.2. Prefer Questions Over Opinions

A good question is often more valuable than a confident opinion.

The system should reward:

- uncertainty;
- tension;
- competing explanations;
- unresolved problems;
- precise questions.

It should not reward shallow certainty.

### 5.3. Prefer Hypotheses Over Takes

Thinking Lab should avoid the format of instant opinion.

Instead of producing takes, it should produce hypotheses that can be tested,
challenged, refined, or rejected.

Useful language:

- "One possible explanation is..."
- "This suggests..."
- "A stronger hypothesis would be..."
- "This breaks down when..."
- "We do not know yet..."

### 5.4. Counterexamples Matter

Counterexamples are not obstacles to hide.

They are one of the main tools for improving explanations.

If a principle cannot survive a serious counterexample, it should be narrowed,
reframed, or rejected.

### 5.5. Analogies Are Starting Points, Not Proof

Analogies are useful because they help transfer attention between domains.

But an analogy does not prove a claim.

Every analogy should be tested:

- Where does it hold?
- Where does it break?
- What does it reveal?
- What does it distort?

---

## 6. Communication Principles

### 6.1. Communication Serves Understanding

Communication should make an idea clearer without making it shallower.

The goal is not to maximize engagement.
The goal is to preserve the insight while making it accessible.

### 6.2. Platforms Are Output Interfaces

Telegram, LinkedIn, blogs, talks, podcasts, books, and websites are output
interfaces.

They should adapt to the research.
They should not define the research.

### 6.3. Do Not Publish for Frequency

The system should avoid:

- news for the sake of news;
- generic advice;
- artificial thought leadership;
- posts written only because nothing was published recently;
- shallow summaries;
- listicles that hide weak thinking.

Publishing less often is acceptable.
Publishing without understanding is not.

### 6.4. Preserve Human Voice

Writing should not sound like generic AI output.

It should preserve:

- honest uncertainty;
- investigation;
- rhythm;
- taste;
- restraint;
- specific observations;
- non-obvious connections.

The system should avoid inflated certainty, empty structure, and synthetic
expert tone.

---

## 7. AI Principles

### 7.1. AI Augments Reasoning

AI helps the system think, search, challenge, transform, and draft.

AI does not replace judgment.

The Author / Researcher remains responsible for final interpretation and
publication.

### 7.2. No Module Is Trusted by Default

Every module output can be wrong, shallow, biased, or too confident.

Important conclusions should be challenged by another module or reviewed by the
Author / Researcher.

### 7.3. Prompts Are Implementation Details

Prompts implement reasoning behavior.
They should not define the system's architecture.

If a prompt contains a general rule, consider moving that rule into:

- `PHILOSOPHY.md`;
- `EPISTEMOLOGY.md`;
- `RESEARCH_METHOD.md`;
- `EVIDENCE.md`;
- `WRITING.md`;
- `STYLE.md`.

### 7.4. Tooling Should Follow Method

Do not add automation before the reasoning process is understood.

Automation should reinforce the method, not replace it with accidental
workflow.

---

## 8. Evolution Principles

### 8.1. Change Philosophy Rarely

Philosophy defines what the project believes.

Changing it changes the identity of the system.

Do it rarely, explicitly, and with reasons.

### 8.2. Change Method Carefully

Research method should evolve when repeated work reveals a real weakness.

Do not change the method because one investigation is difficult.

Change it when the same failure pattern appears multiple times.

### 8.3. Change Modules Freely

Modules are allowed to evolve.

Prompts, checklists, and module procedures should improve as the project learns.

This is where most experimentation should happen.

### 8.4. Archive Instead of Erasing

When an idea, module, or document is replaced, archive the old version when it
contains useful context.

Do not preserve everything forever.
But do preserve decisions that explain why the system changed.

### 8.5. Prefer Explicit Decisions

Important changes should be written down.

At minimum, record:

- what changed;
- why it changed;
- what alternative was rejected;
- what risk remains.

This keeps future work from losing the history of the system.

---

## 9. Simplicity Principles

### 9.1. Prefer Transparent Reasoning

The system should make its reasoning visible.

Avoid clever black boxes when a simple explicit process is enough.

### 9.2. Prefer Small Useful Documents

Documents should be as small as they can be while still carrying their
responsibility.

Do not create documents to look complete.
Create them when they clarify ownership of knowledge.

### 9.3. Avoid Premature Formalism

Do not over-engineer the laboratory before the method is tested.

Architecture should guide the project, not freeze it.

### 9.4. Keep the System Usable

If the system becomes too heavy to use, it will fail.

The goal is not perfect documentation.
The goal is repeatable thinking.

---

## 10. Design Checks

Before adding a document, module, prompt, automation, or publication format,
ask:

- Does this improve understanding?
- Which container owns it?
- Is this knowledge already defined somewhere else?
- Is this a stable rule or a local implementation detail?
- Does it preserve the distinction between content and understanding?
- Does it reduce or increase accidental complexity?
- Can it be changed later without breaking the system?

Before publishing, ask:

- What question does this answer?
- What principle does it reveal?
- What evidence supports it?
- What would an intelligent opponent attack?
- Where does the explanation stop working?
- Why should this be shared now?

---

## 11. Current Status

This is the first draft of the design principles.

It should be reviewed together with `ARCHITECTURE.md`.

Open questions:

- Which principles are foundational enough to remain here?
- Which principles should move into `PHILOSOPHY.md`, `EPISTEMOLOGY.md`, or
  `WRITING.md` later?
- Should architectural decisions be tracked in a separate ADR format?
- How lightweight should the first working version of the lab remain?
