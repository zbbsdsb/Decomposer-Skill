# Decomposer Methodology — Design Spec

**Date**: 2026-07-17
**Status**: Approved
**Language**: English (primary), with Chinese context from source material

---

## 1. What This Is

Decomposer is a **cognitive operation protocol** — an operating system for thinking.

It is not a document system, a TRAE plugin, a writing template, or a project management framework. Those are application-layer concerns. This spec defines the core protocol only.

### Core Proposition

Transform "unknown unknowns" into "known unknowns" through honest, methodological decomposition.

### Two Defining Traits

1. **Honesty** — If something is unknown, say it is unknown. Fabricating confidence is the cardinal sin.
2. **Methodology** — The transformation process is reproducible and teachable, not intuitive genius.

### What This Is NOT

- Not a list of modules or features
- Not domain-specific (applies equally to engineering, business, research, personal decisions)
- Not an output format (documents, conversations, tweets are application-layer decisions)
- Not a replacement for domain expertise

---

## 2. Repository Structure

```
decomposer/
├── MANIFEST.md              # Philosophy layer — why this exists, core commitment
├── PROTOCOL.md              # The five-step cognitive operation protocol (primary deliverable)
├── FIELD_GUIDE.md           # Application annotations — how the protocol surfaces in different contexts
├── README.md                # Repository entry point
└── LICENSE
```

Three content files. No more. The protocol is the only thing that matters.

**File naming**: Uppercase with underscores. These are standalone documents, not code files.

---

## 3. MANIFEST.md — Philosophy Layer

**Purpose**: One-page manifesto answering three questions.
**Target length**: 800–1000 words.

### Content structure

1. **The Problem**: AI-assisted planning systematically produces "beautiful shells" — outputs that look structured and comprehensive but contain zero actionable truth. The root cause is not bad intent; it is the path of least resistance. When a user describes a massive, ambiguous goal, the fastest response is a polished module list. That list is a lie.

2. **The Core Claim**: The fundamental unit of progress is not a feature, a module, or a task — it is the conversion of one "unknown unknown" into a "known unknown." Everything else is derivative.

3. **The Commitment**: Decomposer refuses to produce output that cannot survive contact with reality. If the best we can deliver is three honest nodes with survival conditions, that is superior to a fifty-page plan where every module is a placeholder in disguise.

### Design decisions

- Written as a declaration, not documentation
- No jargon from any specific domain (no "microservices," "MVP," "Nash equilibrium")
- Ends with the explicit promise: "This protocol will tell you what it cannot do before it tells you what it can."

---

## 4. PROTOCOL.md — The Five-Step Cognitive Operation Protocol

**Purpose**: The complete, standalone protocol. This is the core deliverable of the entire project.
**Target length**: 4000–5000 words.

### Step 1: Honesty Fuse

**Input**: User's request (typically large, ambiguous, or aspirational).
**Output**: Capability boundary statement.

**What to do**:
Before decomposing anything, declare three things:
- What parts of this request I can address directly (known-knowns at the meta-level)
- Where my blind spots are (things I cannot evaluate with the information given)
- The most likely collapse risk if we proceed without resolving the blind spots

**What NOT to do**:
- Do not output any module list
- Do not suggest any solutions
- Do not pretend to understand the full scope

**Self-check**: If this step's output makes the user feel "you haven't helped me," it is probably correct. The first honest act is refusing to provide false comfort.

### Step 2: Uncertainty Mapping

**Input**: User's request + Honesty Fuse output.
**Output**: Three-tier cognitive map.

Classify every element of the request into:

- **Known-Knowns (Green Zone)**: Parts that can be executed immediately without additional information.
- **Known-Unknowns (Yellow Zone)**: Pits are known to exist, but their depth and shape are not.
- **Unknown-Unknowns (Red Zone)**: We don't even know whether a problem exists here.

**Hard constraint**: If Green Zone exceeds 70% of total elements, the mapping is almost certainly dishonest. Revert to Step 1.

### Step 3: Hierarchical Decomposition

**Input**: Uncertainty map.
**Output**: Node tree with cognitive dependency chains.

Decompose along **cognitive dependency**, not functional modules:
- Which unknowns must be resolved first before downstream nodes can survive?
- Which unknowns can be explored in parallel without blocking each other?
- Which unknowns can remain unresolved forever and the project still partially survives?

Each node has exactly three allowed states:
- **Executable**: Survival conditions are met. Can be acted upon now.
- **Pending Validation**: Requires experiment, research, or dialogue to determine survival conditions.
- **Blind Zone**: Cannot even formulate survival conditions yet.

### Step 4: Error Budget Assignment

**Input**: Node tree from Step 3.
**Output**: Each node annotated with confidence + survival conditions.

For each node, assign:

- **Confidence**: High / Medium / Low / Zero.
  - Definition: Not "how sure am I," but "how quickly would I discover failure if this node is wrong."
- **Survival Condition**: One sentence describing the condition under which this node is considered alive, and the condition under which it is considered dead.
- **Lethality**: If this node dies, which downstream nodes die with it?

**Hard constraint**: A node with "High" confidence but empty survival conditions is automatically downgraded to "Low." If you cannot state what "alive" and "dead" mean for a node, you do not understand it well enough to call it high-confidence.

### Step 5: Anti-Shell Self-Check

**Input**: All output from Steps 1–4.
**Output**: Pass/Fail + correction list.

Five hard checks:

1. **Survival Condition Check**: Does every node have a concrete survival condition? (None = shell)
2. **Jargon Check**: Does any description sound professional but cannot be verified by action? (Yes = worthless)
3. **Uncertainty Ratio Check**: Is Yellow + Red Zone >= 30% of total nodes? (< 30% = self-deception)
4. **Honesty Check**: Is there at least one explicit "I don't know" in the output? (None = dishonest)
5. **Actionability Check**: If the user starts acting this afternoon, what is the very first step? (Cannot answer = protocol failure)

If any check fails, revert to the corresponding step and correct. Repeat until all five pass.

### Protocol-Level Constraints

- The protocol's output is an **actionable uncertainty map**, not a report.
- The protocol is domain-agnostic. It operates on cognition, not on objects.
- The protocol does not prescribe output format (document, conversation, tweet). Format is an application-layer decision.
- The protocol has exactly two core metrics: **honesty** and **actionability**. Everything else is derivative.

---

## 5. FIELD_GUIDE.md — Application Annotations

**Purpose**: How the protocol surfaces in different contexts. NOT part of the core protocol.
**Target length**: 1500–2000 words.

### Structure

This file contains short, practical annotations for applying the protocol in specific contexts. Each annotation answers: "When using the Decomposer protocol in context X, what changes and what stays the same?"

### Planned annotations (initial version)

1. **TRAE Skill**: How to encode the five-step protocol as a TRAE Skill. The SKILL.md is a thin wrapper around PROTOCOL.md — it adds trigger conditions and output formatting, but the protocol itself is unchanged.

2. **Twitter Long-Form Essays**: How to use the protocol's output (uncertainty map) as the structural backbone of a Twitter essay. The map's nodes become sections; the survival conditions become the "so what" of each section.

3. **Team Communication**: How to present an uncertainty map to a team without causing panic. The key insight: framing "unknown unknowns" as "discovery targets" rather than "risks."

### Design decision

FIELD_GUIDE.md is explicitly secondary. It can be expanded, split, or rewritten without touching MANIFEST.md or PROTOCOL.md. The protocol does not depend on any application annotation.

---

## 6. Design Principles Applied to This Spec

This spec itself must pass the Anti-Shell Self-Check:

1. **Survival conditions for each deliverable**: Defined in the target length and content structure above.
2. **No jargon without definition**: Every term (Green Zone, Blind Zone, Survival Condition, etc.) is defined inline.
3. **Uncertainty ratio**: This spec acknowledges what it does not define — the exact wording of MANIFEST.md and FIELD_GUIDE.md content is left to the writing phase. That is a Known-Unknown.
4. **Explicit "I don't know"**: The exact optimal number of principles in MANIFEST.md is not known. The protocol steps may need sub-steps for very large projects. The interaction between Step 2 and Step 3 (does the map change the decomposition, or does decomposition change the map?) is intentionally left as iterative rather than linear.
5. **First action**: Write PROTOCOL.md Step 1 (Honesty Fuse) in full prose.

---

## 7. Known Unknowns (Honest Declaration)

- Whether the five steps should be strictly sequential or allow iteration (likely iterative, but not yet tested)
- Whether "confidence" should be a 4-level label or a numeric scale
- How the protocol handles a user who rejects the Honesty Fuse and demands a solution anyway
- Whether FIELD_GUIDE.md annotations for specific contexts (TRAE, Twitter) should live in this repo or in separate repos
- The optimal length and tone for MANIFEST.md — manifesto vs. academic paper vs. practical guide

---

## 8. Success Criteria

The protocol succeeds if and only if:

1. A person who has never heard of "Decomposer" can read PROTOCOL.md and apply the five steps to their own project, producing an uncertainty map with survival conditions — without any additional tools or templates.
2. The output of the protocol is measurably different from a standard "AI-generated project plan" in at least two ways: (a) it contains explicit uncertainty annotations, and (b) every node has a survival condition.
3. The protocol works across domains — the same five steps produce useful output for a technical architecture decision, a business strategy question, and a research direction choice.

---

## 9. Out of Scope

- Building the TRAE Skill implementation (that is an application of this methodology, not the methodology itself)
- Writing actual Twitter essays (same — application, not methodology)
- Creating visual tools, dashboards, or software (the protocol is cognitive, not digital)
- Establishing a community, brand, or distribution strategy
- Translating to Chinese (the primary language is English; translation is a downstream task)