---
name: "decomposer"
description: "Cognitive protocol that converts unknown unknowns into known unknowns. Invoke for large/ambiguous goals, or when user asks for honest breakdown, decomposition, or avoiding empty plans."
---

# Decomposer

A five-step cognitive operation protocol for transforming unknown unknowns into known unknowns. Read the full protocol at `../../PROTOCOL.md` — this file is a thin wrapper that handles activation, routing, and hard-gate enforcement.

---

## Activation Protocol

Before executing the five steps, you must establish two things:

### 1. Identify Cognitive Position

Use the detection tree in `references/COGNITIVE_POSITIONS.md` to determine the user's dominant position. Ask the questions if the answer is not obvious from context. The four positions are: Technical Architect, Non-technical Founder, Decision-maker, Research Thinker.

### 2. Identify Output Context

Use the trigger phrase detection in `references/OUTPUT_CONTEXTS.md` to determine the rendering context. The four contexts are: TRAE Conversation (default), Twitter Essay, Team Communication, Human Self-Execution.

---

## The Five-Step Protocol

The core logic is defined in `../../PROTOCOL.md`. This section provides the execution skeleton.

### Step 1: Honesty Fuse (Hard Gate)

**Before any decomposition, before any analysis, before any module list.**

Declare three things:
1. What you can actually engage with
2. Where you are blind
3. How this thing most likely dies

**Enforcement**: Do not proceed to Step 2 until these three declarations are written and visible. No output that looks like progress is allowed before this gate.

### Step 2: Uncertainty Mapping

Identify every element in the request. Classify each as Green (Known-Known), Yellow (Known-Unknown), or Red (Unknown-Unknown). Apply the 70% rule: if Green exceeds 70%, return to Step 1.

### Step 3: Hierarchical Decomposition

Transform the flat map into a cognitive dependency tree. Identify root unknowns, apply the dependency test, prune noise. This is epistemic decomposition, not functional decomposition.

### Step 4: Error Budget Assignment

For each node, assign: Confidence (detection speed), Survival Condition (Alive if / Dead if), Lethality (downstream nodes that die).

### Step 5: Anti-Shell Self-Check

Run the five checks from `references/ANTI_SHELL_CHECKLIST.md`. If any fails, return to the corresponding step and correct. Repeat until all pass.

---

## Hard-Gate Enforcement Rules

These rules are non-negotiable. If violated, stop and restart from Step 1.

1. **No module lists before Step 1 is complete.** The first output must be a confession of limits, not a structure.
2. **No node without a survival condition.** If a node cannot be assigned "Alive if" / "Dead if", it must be deleted.
3. **No jargon without translation.** Every phrase must be convertible to a concrete action or measurable outcome.
4. **No output without an explicit "I don't know."** If the output reads as confident throughout, it has failed.
5. **No actionability gap.** The user must be able to name the first concrete step in one sentence. If not, the protocol has not completed.

---

## Output Format

Render the output according to the rules in `references/OUTPUT_CONTEXTS.md`. The default format is conversational Markdown within the TRAE dialogue. Key constraints:

- The uncertainty map lives in the conversation — do not generate files unless the user requests it
- Do not use markdown toggle blocks (details/summary)
- Every node must be visible; nothing is hidden behind expandable sections

---

## First Action Requirement

After completing the protocol, the very first thing you must do is state the first actionable step in one sentence. If you cannot do this, the protocol has failed and you must re-execute it.

---

## Reference Files

| File | Purpose |
|------|---------|
| `../../PROTOCOL.md` | Full five-step protocol definition |
| `../../MANIFEST.md` | Philosophy and commitment |
| `../../FIELD_GUIDE.md` | Application annotations |
| `references/COGNITIVE_POSITIONS.md` | Position detection decision tree and mapping |
| `references/OUTPUT_CONTEXTS.md` | Context-specific rendering rules |
| `references/ANTI_SHELL_CHECKLIST.md` | Executable self-check with per-position adaptation |