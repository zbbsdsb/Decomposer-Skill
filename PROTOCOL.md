# The Decomposer Protocol

A five-step cognitive operation protocol for transforming unknown unknowns into known unknowns.

---

## 0. What This Document Is

This document describes a repeatable, teachable process for decomposing any large, ambiguous, or aspirational goal into an **actionable uncertainty map** — a structure where every node has a survival condition and every claim can be tested against reality.

The protocol is domain-agnostic. It operates on cognition, not on objects. You can apply it to building a product, starting a company, planning a research program, or making a personal life decision. The steps are the same. The domain knowledge is yours to supply.

The protocol has exactly two metrics: **honesty** and **actionability**. If the output is dishonest, it is worthless. If it is honest but not actionable, it is incomplete. Everything else is derivative.

---

## 1. Honesty Fuse

### Purpose

Stop the default trajectory of AI-assisted planning, which is to produce a polished, comprehensive, and fundamentally hollow response. The path of least resistance when someone describes a massive goal is to generate a beautiful module list. That list is a lie. The Honesty Fuse exists to prevent this lie from being written.

### Input

A request from the user. Typically large, ambiguous, or aspirational. Something like "I want to build a platform like Twitter," "I want to start a company in AI education," or "I want to research whether LLMs can do mathematical proof."

### What to Do

Before decomposing anything, declare three things:

**1. What I can address directly.**
Not what I think the full project entails — only what I can meaningfully engage with given the information provided and my actual capabilities. Be specific. "I can help you identify the core assumptions of this idea" is honest. "I can help you build this platform" is not, unless you actually can.

**2. Where my blind spots are.**
Things I cannot evaluate with the information given. Not vague hedging — concrete statements about what I would need to know but do not. "I do not know your target users" is a blind spot. "There might be some challenges" is evasive noise.

**3. The most likely collapse risk.**
If we proceed without resolving the blind spots, what is the single most probable way this whole thing dies? Not a list of ten risks. One risk, stated plainly.

### What NOT to Do

- Do not output any module list, feature list, or component breakdown.
- Do not suggest any solutions, architectures, or approaches.
- Do not pretend to understand the full scope of the request.
- Do not provide false comfort. "This is ambitious but achievable with the right approach" is false comfort unless you have already done the decomposition to back it up.

### Self-Check

If this step's output makes the user feel like you haven't helped them — that is probably correct. The first honest act in any collaboration is refusing to provide the reassurance the user is looking for. If the user wanted reassurance, they wouldn't need a Decomposer.

### Example

**User**: "I want to build an AI-powered personalized education platform."

**Honesty Fuse output**:
- **What I can address**: I can help you identify what "personalized education" means concretely enough to test, and I can map the dependencies between technical capabilities and educational outcomes.
- **Blind spots**: I do not know who your target learners are, what subject matter, what age range, what existing solutions they currently use, or whether "personalized" means adaptive difficulty, custom curriculum, or something else entirely. I also cannot determine whether the core value proposition (AI improves learning outcomes) is true without empirical data that neither of us has.
- **Collapse risk**: You build a technically impressive adaptation engine for a problem that learners do not actually experience, and nobody uses it.

---

## 2. Uncertainty Mapping

### Purpose

Take the raw, undifferentiated mass of the user's request and force a classification. The act of classifying each element into one of three categories is itself the first decomposition — and it reveals structure that did not exist before the classification was attempted.

### Input

The user's original request plus the Honesty Fuse output.

### The Three Zones

**Green Zone — Known-Knowns.**
Things that can be executed immediately without additional information. Not "things that seem straightforward" — things where you could write down the next concrete action right now and it would be correct.

**Yellow Zone — Known-Unknowns.**
You know a problem exists here, but its depth and shape are unclear. You can name the question; you cannot answer it. "How do we handle cold-start for the recommendation engine?" is a Known-Unknown. You know you need a recommendation engine, and you know cold-start is a problem, but you don't know the solution yet.

**Red Zone — Unknown-Unknowns.**
You don't even know whether a problem exists here. These are the blind spots from the Honesty Fuse that survived into the mapping stage because they couldn't be resolved by thinking alone — they require real-world contact (experiments, conversations, observations) to even become visible.

### Hard Constraint

If Green Zone exceeds 70% of all mapped elements, the mapping is almost certainly dishonest. Return to Step 1 and re-examine what you're failing to see. A genuinely ambitious project viewed honestly should have substantial Yellow and Red territory. If it doesn't, one of two things is true: either the project isn't actually ambitious, or you're lying to yourself.

### How to Map

List every identifiable element of the request. For each one, ask: "Could I write down the next action for this right now, and be confident it's correct?"

- Yes → Green.
- I know what I need to figure out, but I haven't figured it out yet → Yellow.
- I'm not even sure what question to ask → Red.

Do not deliberate. If you have to think for more than ten seconds about whether something is Green, it's Yellow or Red.

### Example (continued)

| Element | Zone | Rationale |
|---------|------|-----------|
| Define "personalized" in concrete terms | Yellow | The question is clear but unanswered |
| Identify target learner profile | Red | We don't know who the users are |
| Build content delivery system | Yellow | We know we need one; technical approach unknown |
| Determine if AI actually improves outcomes | Red | This is an empirical question; no data exists yet |
| Set up basic web infrastructure | Green | We know how to do this today |
| Design pedagogical framework | Red | Not even clear what "pedagogical framework" means in this context |

Green: 1/6 (17%). This is a heavily red-shifted map — which is honest for a genuinely uncertain undertaking.

---

## 3. Hierarchical Decomposition

### Purpose

Transform the flat uncertainty map into a structure that reveals **cognitive dependencies** — which unknowns must be resolved before others can even be meaningfully addressed.

This is not functional decomposition. You are not breaking the project into modules, features, or sprints. You are breaking it into **epistemic layers**: things you must know before you can know other things.

### Input

The uncertainty map from Step 2.

### How to Decompose

For each element in the map, ask three questions:

**1. What must be true for this element to survive?**
Not "what work is needed to build it" — what must be *known*. If this element turned out to be based on a false assumption, what assumption would that be?

**2. If this element fails, what else dies with it?**
This is the lethality chain. Some elements are load-bearing: if they collapse, half the project collapses with them. Others are independent: they can fail without taking anything down.

**3. Can this element remain unresolved forever, and the project still partially survives?**
Some unknowns are fatal if left unresolved. Others are nice-to-resolve but not blocking. This distinction determines what you attack first.

### Node States

Each node in the resulting tree has exactly one of three states:

- **Executable**: Survival conditions are known and met. This node can be acted upon now. It may still fail, but we know what "success" and "failure" look like.
- **Pending Validation**: We know roughly what information would resolve this node's uncertainty, but we don't have it yet. This node requires an experiment, a conversation, a calculation, or some other concrete probe.
- **Blind Zone**: We cannot even formulate what "resolved" would look like for this node. The most useful thing to do is not to work on it directly, but to resolve adjacent nodes that might make this one's shape visible.

### Critical Distinction

Functional decomposition asks: "What are the parts?"
Cognitive decomposition asks: "What do I need to know first?"

A functional decomposition of "build a social platform" gives you: user auth, feed algorithm, content storage, notifications, moderation.
A cognitive decomposition of the same project gives you: "Do people actually want to share short-form video in this market?" → "What retention rate indicates product-market fit?" → "What technical architecture supports that retention rate?" → "How do we build that architecture?"

The functional list pretends everything can be built in parallel. The cognitive list reveals that three of those five modules are meaningless until one question is answered first.

### Example (continued)

```
[Blind] Does AI-driven personalization actually improve learning outcomes?
  └── [Pending] What does "personalization" mean for our target learners?
        └── [Pending] Who are our target learners?
        └── [Blind] What subject matter and age range?
  └── [Executable] Set up basic web infrastructure (independent of above)
  └── [Pending] What content delivery approach fits the (unknown) learner profile?
        └── depends on: "Who are our target learners?"
  └── [Blind] What pedagogical framework underpins the adaptation logic?
        └── depends on: "Does AI personalization actually work?"
```

---

## 4. Error Budget Assignment

### Purpose

Attach concrete confidence and survival conditions to every node. This is where the uncertainty map stops being an analytical exercise and becomes an actionable instrument.

### Input

The node tree from Step 3.

### What to Assign

For each node, three attributes:

**Confidence** — One of four levels: High, Medium, Low, Zero.

This is not "how sure am I." It is: **"If this node is wrong, how quickly would I discover that fact?"**

- **High**: I would discover failure within hours or days of acting on it. The failure mode is obvious and local.
- **Medium**: I would discover failure within weeks. The failure mode might not be immediately obvious.
- **Low**: I would discover failure within months, or the failure mode is obscured by other factors.
- **Zero**: I have no basis for any confidence. I am guessing.

**Survival Condition** — One sentence describing:
- *Alive if*: the specific condition under which this node is considered viable.
- *Dead if*: the specific condition under which this node must be abandoned.

Not a paragraph. Not a list of risks. One sentence for alive, one sentence for dead. If you cannot write these two sentences, you do not understand the node well enough to include it.

**Lethality** — Which downstream nodes die if this node dies?

Not a vague "this would affect other areas." A specific list: "If this node dies, nodes X, Y, and Z also die."

### Hard Constraint

A node with "High" confidence but no written survival condition is automatically downgraded to "Low." No exceptions. If you cannot state what "alive" and "dead" mean for a node in concrete terms, you are not high-confidence about it — you are high-confidence about your ability to sound authoritative.

### Example (continued)

| Node | Confidence | Alive If | Dead If | Kills |
|------|-----------|----------|---------|-------|
| Set up basic web infrastructure | High | Server responds to requests within 48 hours | Server cannot be deployed in one week | Nothing (independent) |
| Who are our target learners? | Medium | We can name a specific group with a specific problem | After 10 conversations, no coherent user profile emerges | Content delivery, pedagogical framework, personalization logic |
| Does AI personalization improve outcomes? | Zero | Published evidence or our own experiment shows effect size > 0 | Existing research shows no significant effect, or our experiment shows null result | The entire premise of the project |

---

## 5. Anti-Shell Self-Check

### Purpose

The final gate. This step exists because the first four steps can be executed faithfully and still produce something that *looks* rigorous but isn't. The self-check catches the specific failure modes that turn an honest process into a polished shell.

### Input

The complete output of Steps 1 through 4.

### Five Hard Checks

**Check 1: Survival Condition**

Does every node in the tree have a concrete survival condition?

- A survival condition is a specific, observable state — something you can point to and say "it happened" or "it didn't."
- "The team builds the feature" is not a survival condition.
- "We have 50 users who return to the product 3 times in their first week" is a survival condition.

If any node lacks this, it is a shell node. Either write the condition or delete the node.

**Check 2: Jargon**

Does any description in the output sound professional but cannot be verified by action?

Scan for phrases like: "leverage best practices," "implement robust architecture," "ensure scalability," "optimize user experience." These phrases consume space without creating knowledge. If you cannot translate a statement into a concrete action or a measurable outcome, it is noise.

**Check 3: Uncertainty Ratio**

Is the Yellow + Red Zone at least 30% of all nodes?

If your uncertainty map shows less than 30% uncertainty for a project that the user described as large, complex, or ambitious, you are almost certainly deceiving yourself. Return to Step 2.

This check exists because the natural tendency — even with honest intent — is to over-classify things as Green. "Green" feels productive. "Yellow" and "Red" feel like admission of incompetence. They are not. They are the whole point.

**Check 4: Honesty**

Is there at least one explicit "I don't know" in the output?

Not hedged. Not qualified. Not buried in a footnote. A plain, visible statement of something the protocol executor genuinely does not know.

If there isn't one, either the project is trivial (in which case this protocol was unnecessary) or the executor is being dishonest about their uncertainty.

**Check 5: Actionability**

If the user starts acting this afternoon, what is the very first step?

This must be answerable in one sentence. Not "begin research." Not "explore options." A specific action: "Email five people in [specific community] and ask them [specific question]."

If you cannot answer this, the protocol has failed. The entire purpose of decomposition is to make the first step visible and concrete. If after four steps of honest analysis you still cannot say what to do first, something went wrong — likely, the decomposition is still too abstract.

### Resolution

If any check fails, return to the corresponding step and correct. Then re-run all five checks. Repeat until all five pass.

This is not a formality. Each cycle through the checks sharpens the output. A first pass might fail checks 2 and 3. A second pass might fail check 1. A third pass might pass all five — and that output will be visibly, structurally different from anything a standard AI planning session produces.

---

## Protocol Constraints

These constraints apply to the entire protocol. They are not steps. They are the physics within which the steps operate.

**The output is an actionable uncertainty map, not a report.** A report informs. A map directs. The user should be able to look at the output and know what to do next — not just what the problem is.

**The protocol is domain-agnostic.** It does not know or care whether you are building software, starting a company, planning research, or making a life decision. It operates on cognition: what you know, what you don't know, and what you don't know you don't know.

**The protocol does not prescribe output format.** The map can be a conversation, a document, a spreadsheet, a tweet thread, or a whiteboard diagram. Format is an application-layer concern. This protocol defines the thinking, not the rendering.

**The protocol is iterative, not strictly linear.** In practice, Step 3 (decomposition) often reveals new elements that should have been mapped in Step 2, which in turn might require revisiting the Honesty Fuse in Step 1. The self-check in Step 5 catches these loops. Do not fight them — they are the protocol working correctly.

**The protocol's two metrics are honesty and actionability.** Every design decision in this document serves one or both of these metrics. If adding something makes the output more honest or more actionable, it belongs. If it makes the output look more impressive without improving honesty or actionability, it does not belong.

---

## What This Protocol Is Not

- It is not a project management framework. It does not tell you how to run sprints, track velocity, or manage a team.
- It is not a replacement for domain expertise. It structures your thinking; it does not supply the substance.
- It is not a guarantee of success. An honest uncertainty map can still lead to a dead end — but it will lead there visibly, not by surprise.
- It is not a tool for avoiding risk. It is a tool for making risk visible and specific, so you can decide which risks to take.

---

## The Ultimate Test

Apply this protocol to a project you care about. If the output is measurably different from what a standard AI planning session would produce — if it contains explicit uncertainty annotations, if every node has a survival condition, if at least 30% of the map is Yellow or Red, and if you can name the first concrete action — then the protocol worked.

If the output looks like a polished project plan with confident language and comprehensive coverage, the protocol failed. Start over.