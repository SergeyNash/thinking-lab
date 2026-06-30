# ARCHITECTURE

> Thinking Lab is not a content project.
> It is a reasoning system.

This document describes the architecture of Thinking Lab.

Thinking Lab is designed to transform observations about technologies,
organizations, products, AI, security, markets, processes, and other complex
systems into transferable principles.

Publications are outputs of the system.
Understanding is the goal.

---

## 1. Purpose

Thinking Lab exists to make deep thinking reproducible.

Its purpose is not to produce frequent posts, maintain a channel, or perform a
personal brand routine. Its purpose is to create the conditions under which
useful understanding can happen repeatedly.

The core question is:

> What simple idea is hidden behind a durable technology, organization, or
> system?

The system starts with concrete artifacts:

- a technology;
- an organization;
- a product;
- a process;
- a failure;
- a recurring pattern;
- a surprising success;
- an uncomfortable question.

It then investigates:

- why the artifact exists;
- what constraints shaped it;
- what alternatives failed or disappeared;
- what behavior it enables or suppresses;
- what principle can be transferred elsewhere.

The final artifact may be an article, post, talk, note, diagram, or unfinished
research memo.

But the primary artifact is understanding.

---

## 2. Scope

Thinking Lab studies systems and the ideas behind them.

The system may investigate:

- engineering systems;
- software architecture;
- organizations;
- product management;
- cybersecurity;
- AI and agentic systems;
- economics;
- science;
- sports;
- social and institutional processes.

These are domains of observation, not the identity of the project.

Thinking Lab should not become tied to one domain, platform, or format. Product
management, cybersecurity, AI, and engineering are useful lenses, but none of
them is the foundation.

The stable subject is:

> ideas that survive technologies.

---

## 3. Level 1: Context

At the context level, Thinking Lab is a personal research operating system.

It receives observations, questions, sources, examples, experiences, and
external feedback. It produces research artifacts and, when appropriate,
public-facing communication.

### External Actors

The system interacts with:

- **Author / Researcher**: initiates questions, evaluates outputs, provides
  taste, judgment, lived experience, and final decisions.
- **AI Models**: assist with search, analysis, critique, synthesis, drafting,
  and transformation of materials.
- **Knowledge Sources**: books, papers, documentation, historical records,
  talks, codebases, incidents, case studies, interviews, and personal notes.
- **Audience**: reads, challenges, shares, ignores, misunderstands, or improves
  the work.
- **Publishing Platforms**: Telegram, LinkedIn, blogs, talks, podcasts, books,
  websites, and other surfaces.
- **Future Collaborators**: humans or systems that may reuse, extend, audit, or
  challenge the research process.

### Inputs

Typical inputs include:

- topic ideas;
- rough intuitions;
- surprising facts;
- historical examples;
- failures and post-mortems;
- analogies between domains;
- questions from readers or peers;
- unresolved disagreements;
- new technologies or organizational patterns;
- personal experience from product, engineering, security, and AI work.

### Outputs

Typical outputs include:

- research notes;
- hypotheses;
- evidence maps;
- principle statements;
- drafts;
- essays;
- LinkedIn posts;
- Telegram posts;
- talks;
- diagrams;
- reusable frameworks;
- rejected explanations;
- archived failed investigations.

Not every investigation should become a publication.

---

## 4. Level 2: Containers

Thinking Lab is composed of five major containers.

```text
Thinking Lab
|
+-- Identity System
+-- Reasoning System
+-- Knowledge System
+-- Reasoning Modules
+-- Communication System
```

### 4.1. Identity System

The Identity System defines what Thinking Lab is and what it is not.

It owns:

- purpose;
- North Star;
- core beliefs;
- long-term constraints;
- non-goals;
- project boundaries.

It answers:

- Why does Thinking Lab exist?
- What kind of understanding is worth pursuing?
- What should the system avoid becoming?
- What must remain stable even when tools and formats change?

### 4.2. Reasoning System

The Reasoning System defines how Thinking Lab thinks.

It owns:

- epistemology;
- systems thinking;
- research method;
- evidence rules;
- handling of analogies;
- treatment of uncertainty;
- quality criteria for explanations.

It answers:

- What counts as knowledge?
- What counts as evidence?
- When is an explanation too shallow?
- How are hypotheses challenged?
- How do we distinguish a useful analogy from a seductive story?

### 4.3. Knowledge System

The Knowledge System stores the memory of Thinking Lab.

It owns:

- research notes;
- topic backlog;
- examples;
- frameworks;
- analogies;
- failures;
- prior outputs;
- rejected hypotheses;
- reusable concepts.

It answers:

- What do we already know?
- What have we tried before?
- Which ideas recur across domains?
- Which explanations failed?
- Which questions deserve deeper work?

### 4.4. Reasoning Modules

Reasoning Modules perform isolated cognitive functions.

They are not personalities.
They are not the architecture itself.
They are replaceable implementations of reasoning responsibilities.

Possible modules include:

- **Archaeologist**: finds what is strange, durable, or worth investigating.
- **Historian**: reconstructs origin, context, constraints, and alternatives.
- **Opponent**: attacks explanations and searches for weak points.
- **Transfer**: tests whether a principle works across domains.
- **Synthesizer**: integrates competing explanations into a coherent model.
- **Editor**: turns understanding into clear, human writing.

The same module may be implemented by a prompt, an AI model, a human process, a
script, or a future tool.

The module responsibility should remain stable even when implementation changes.

### 4.5. Communication System

The Communication System turns understanding into communicable artifacts.

It owns:

- writing principles;
- style rules;
- language policy;
- publication formats;
- adaptation to platforms;
- article templates;
- talk structures;
- voice preservation.

It answers:

- When is something worth publishing?
- What format fits the idea?
- How should a deep investigation become a short post?
- What language should the output use?
- How do we avoid sounding like generic AI-generated thought leadership?
- How do we preserve unfinished but honest thinking?

---

## 5. Level 3: Components

The component level describes the internal responsibilities of each container.

This section is intentionally architectural. It does not yet define the final
file structure.

### 5.1. Identity Components

The Identity System should contain:

- **Project Definition**: the short explanation of what Thinking Lab is.
- **North Star**: the durable direction of the project.
- **Philosophy**: core beliefs about technology, systems, ideas, and thinking.
- **Non-goals**: explicit boundaries that protect the project from drift.
- **Decision Record**: major architectural and conceptual decisions.

### 5.2. Reasoning Components

The Reasoning System should contain:

- **Epistemology**: what counts as knowledge and explanation.
- **Systems Model**: how Thinking Lab thinks about complex systems.
- **Research Method**: repeatable investigation process.
- **Evidence Model**: evidence strength, counterexamples, and uncertainty.
- **Analogy Rules**: how cross-domain transfer is used and limited.
- **Quality Gates**: checks before a conclusion or publication is accepted.

### 5.3. Knowledge Components

The Knowledge System should contain:

- **Topic Backlog**: candidate investigations.
- **Research Notes**: active, paused, and archived investigations.
- **Frameworks Library**: reusable conceptual models.
- **Analogy Library**: cross-domain comparisons treated as hypotheses.
- **Failure Library**: rejected explanations and failed hypotheses.
- **Output Archive**: published and unpublished artifacts.

### 5.4. Module Components

The Reasoning Modules should contain:

- **Module Contract**: responsibility, inputs, outputs, and constraints.
- **Prompt or Procedure**: current implementation of the module.
- **Evaluation Criteria**: how to judge whether the module did useful work.
- **Artifacts**: intermediate outputs produced by the module.

Each module should have one cognitive responsibility.

If a module needs shared knowledge, that knowledge should move upward into the
Reasoning System or Identity System.

### 5.5. Communication Components

The Communication System should contain:

- **Writing Principles**: how research becomes text.
- **Style Guide**: voice, rhythm, tone, and forbidden patterns.
- **Language Policy**: Russian is the default language for public-facing
  outputs unless a specific artifact requires another language.
- **Format Library**: Telegram post, LinkedIn post, essay, talk, memo.
- **Publishing Criteria**: when something is worth sharing.
- **Adaptation Rules**: how one idea changes across platforms without becoming
  shallow.

---

## 6. Level 4: Implementation

The implementation level describes current technical choices.

These choices are allowed to change more often than the architecture.

### 6.1. Current Implementation Medium

The initial implementation is a local Markdown-based repository.

Markdown is used because it is:

- readable by humans;
- easy to diff;
- easy to reorganize;
- compatible with AI context;
- portable across tools and platforms.

### 6.2. Current Documentation Structure

The current v0.1 documentation structure is:

```text
README.md
ARCHITECTURE.md
DESIGN_PRINCIPLES.md

identity/
  PHILOSOPHY.md

reasoning/
  EPISTEMOLOGY.md
  SYSTEMS.md
  RESEARCH_METHOD.md
  EVIDENCE.md

knowledge/
  KNOWLEDGE_BASE.md
  TOPICS.md
  RESEARCH_NOTES.md
  FRAMEWORKS.md
  ANALOGIES.md
  FAILURES.md
  OUTPUTS.md

communication/
  WRITING.md
  STYLE.md
  FORMATS.md

modules/
  MODULES.md
  archaeologist.md
  historian.md
  opponent.md
  transfer.md
  synthesizer.md
  editor.md

archive/
  exploratory drafts
```

This structure is intentionally lightweight.
It should evolve only when real usage shows that more structure is needed.

### 6.3. Prompts

Prompts are implementation details.

They should implement Reasoning Modules, not define the architecture.

This means:

- a prompt may change without changing the module's responsibility;
- a module may be implemented without an AI prompt;
- multiple prompts may support one module;
- shared principles should not be duplicated across prompts.

### 6.4. Automation

Automation may be added later for:

- topic intake;
- source collection;
- research note normalization;
- module execution;
- draft generation;
- evidence checks;
- publication adaptation;
- archive management.

Automation should not be added before the reasoning process is understood.

---

## 7. Knowledge Flow

Knowledge flows downward.

Higher layers define stable constraints for lower layers.

```text
Identity
  -> Reasoning
    -> Knowledge
      -> Reasoning Modules
        -> Communication
          -> Artifacts
```

Examples:

- Philosophy constrains research method.
- Epistemology constrains evidence evaluation.
- Research method constrains module behavior.
- Writing principles constrain platform adaptation.
- Non-goals constrain publication decisions.

Lower layers should not silently redefine higher-layer principles.

If the same rule is needed in many places, it belongs higher in the system.

---

## 8. Feedback Flow

Feedback flows upward.

Outputs, failures, audience response, rejected hypotheses, and unclear drafts
can improve the system.

```text
Artifacts
  -> Communication
    -> Reasoning Modules
      -> Knowledge
        -> Reasoning
          -> Identity
```

Feedback may change:

- examples;
- topic selection;
- module prompts;
- writing formats;
- research method;
- evidence rules;
- even philosophy, rarely.

The higher the layer, the more carefully it should change.

This gives the system both learning and stability.

---

## 9. Key Architectural Decisions

### Decision 1: Thinking Lab Is Not a Channel

Telegram, LinkedIn, blogs, talks, and books are output interfaces.

They should not define the project.

### Decision 2: Optimize for Understanding

The system optimizes for understanding, not output volume.

Publishing often is not a success metric by itself.

### Decision 3: Use Domains as Lenses, Not Foundations

Engineering, product management, cybersecurity, AI, and organizations are
domains of observation.

The foundation is the search for transferable principles.

### Decision 4: Architecture Before Documentation

Documentation should describe the system.
It should not substitute for the system.

### Decision 5: Modules Are Cognitive Functions

Reasoning Modules are not agents or personalities.

They are isolated reasoning responsibilities that can be implemented in
different ways.

### Decision 6: Prompts Are Implementation Details

Prompts are replaceable.

They should inherit from architecture, not become architecture.

### Decision 7: Preserve Traceability

Important conclusions should be traceable to:

- question;
- context;
- assumptions;
- evidence;
- counterarguments;
- uncertainty;
- final principle.

---

## 10. Non-goals

Thinking Lab should not become:

- a generic product-management channel;
- a cybersecurity-only channel;
- a LinkedIn content machine;
- a news digest;
- an AI prompt collection;
- a multi-agent toy project;
- a set of disconnected essays;
- a productivity blog;
- a personal brand performance;
- a place for shallow summaries;
- a system that rewards frequency over depth.

The system should remain a research engine.

---

## 11. Evolution Model

Thinking Lab should evolve by layers.

The principle is:

> Stability above, flexibility below.

### Stable Layers

The Identity System should change rarely.

Changes here affect the meaning of the whole project.

### Semi-stable Layers

The Reasoning System should change when repeated research exposes weaknesses in
the method, evidence model, or epistemology.

### Flexible Layers

The Knowledge System, Reasoning Modules, Communication formats, prompts, and
automation can change more freely.

They should adapt as the project learns.

### Evolution Rule

Before changing a higher layer, ask:

- Is this a local implementation problem?
- Is this a module problem?
- Is this a method problem?
- Or does it reveal a deeper identity problem?

Most changes should happen low in the system.

High-level changes should be rare, explicit, and documented.

---

## 12. Current Status

This is the current v0.1 architecture.

The initial system layers have been created:

- foundation;
- identity;
- reasoning;
- knowledge;
- communication;
- modules.

The architecture is still expected to evolve through feedback from real use.

Open questions:

- Does the module pipeline stay lightweight during real research?
- Should the Decision Record live inside this document or in a separate ADR
  structure?
- Which parts of the system should be automated after manual use proves the
  method?

The next step is a practical end-to-end test on one research topic.
