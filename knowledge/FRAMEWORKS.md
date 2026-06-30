# FRAMEWORKS

This document stores reusable frameworks for Thinking Lab.

Frameworks are not finished articles.
They are thinking tools that help analyze multiple systems.

---

## 1. Purpose

`FRAMEWORKS.md` keeps reusable models, distinctions, and system lenses.

A framework belongs here when it can help more than one investigation.

---

## 2. What Belongs Here

Add:

- system lenses;
- causal distinctions;
- recurring mechanisms;
- reusable checklists;
- principle candidates;
- analysis patterns;
- vocabulary that helps future research.

Examples:

- cost structures;
- feedback loops;
- local vs global optimization;
- degradation;
- resilience;
- reversibility;
- interface boundaries;
- path dependence.

---

## 3. What Does Not Belong Here

Do not add:

- finished posts;
- isolated examples;
- raw evidence;
- frameworks copied without adaptation;
- vague concepts that do not help analysis;
- rules that belong in `reasoning/`.

---

## 4. Framework Template

```markdown
## <Framework Name>

Status:
Short definition:
Useful for:
Core question:
Mechanism:
Example cases:
Where it fails:
Related frameworks:
```

---

## 5. Relationship to Reasoning

Frameworks should remain consistent with:

- `reasoning/SYSTEMS.md`;
- `reasoning/EPISTEMOLOGY.md`;
- `reasoning/RESEARCH_METHOD.md`.

If a framework becomes a general rule for how Thinking Lab reasons, consider
moving it upward into `reasoning/`.

---

## 6. Seed Frameworks

## Cost Structures

Status: active  
Short definition: Systems shape behavior by making some actions cheaper and
others more expensive.  
Useful for: technologies, organizations, product systems, security controls,
AI workflows.  
Core question: What does this system make cheap or expensive?  
Mechanism: Changes in cost change incentives and behavior.  
Example cases: Git lowering the cost of experimentation; security review
processes increasing or decreasing the cost of safe changes.  
Where it fails: Cost is not always monetary or obvious; cultural and political
costs may dominate.  
Related frameworks: feedback loops, reversibility, local vs global optimization.

## Cost of Reversible Experimentation

Status: active  
Short definition: Systems change behavior when trying, failing, learning, and
recovering become cheap enough compared to avoiding uncertainty or making large
upfront commitments.  
Useful for: software development, product discovery, security paved roads, AI
workflows, organizational process experiments, personal thinking systems.  
Core question: What does this system make safe to try, reverse, compare, or
recover from?  
Mechanism: When reversible experimentation becomes cheaper, participants explore
more alternatives, recover from mistakes faster, and coordinate through smaller
steps instead of large commitments.  
Example cases: Git lowering the cost of branching, local experimentation, and
recovery; feature flags lowering the cost of product experiments; security paved
roads lowering the cost of safe behavior.  
Where it fails: irreversible decisions, weak feedback, high verification cost,
externalized harm, political rollback, or experiments that create noise instead
of learning.  
Related frameworks: cost structures, reversibility, feedback loops, local vs
global optimization.

## Feedback Loops

Status: active  
Short definition: Systems learn, stabilize, amplify, or degrade through
feedback.  
Useful for: product metrics, engineering workflows, incident response,
organizational processes.  
Core question: What feedback exists, who sees it, and how fast can they act?  
Mechanism: Feedback changes future behavior when it is visible, trusted, and
actionable.  
Example cases: CI feedback, customer feedback, incident post-mortems.  
Where it fails: Feedback may be delayed, distorted, ignored, or optimized
against.  
Related frameworks: degradation, incentives, evidence quality.
