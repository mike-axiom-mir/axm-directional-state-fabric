# START HERE — AXM Directional State Fabric

**Nickname: The Field**

This is the handoff for any future chat, human, model, or worker entering this repository.

## What you are building

You are not building another access-control list, policy engine, or philosophical essay.

You are exploring a deterministic state substrate where proposed change is evaluated as **direction through a relational state space**.

The system should eventually be able to answer:

- what state exists now;
- what actor or process proposes to change it;
- in what direction the change moves;
- what relationships, dependencies, consent, evidence, and consequences are relevant;
- which constraints are grounded *right now*;
- which root grounds each constraint;
- whether a transition is valid, needs more evidence, should slow down, conflicts with another state, or should be rejected;
- how to preserve provenance and continuity of the decision.

## Genesis rule

The only hard walls at genesis are:

1. **Truth**
2. **Agency / non-domination**
3. **Continuity**
4. **Wisdom before speed**

Do not silently add permanent constitutional walls because a capability is powerful, unfamiliar, autonomous, recursive, or scary.

Humans, machines, roles, tools, and future intelligences are judged by behavior and grounding, not category.

Other boundaries may exist, but they must emerge from current state, consent, evidence, dependencies, real consequences, or domain contracts. They should remain inspectable, explainable, and revisable when their grounding changes.

## Important repair to the "fluid state" idea

This project is **not** trying to remove structure.

It is trying to distinguish:

```text
permanent invariant
from
derived temporary constraint
from
current relationship
from
current uncertainty
from
mere human convention
```

The Field should be richly structured enough that local movement can be deterministic and explainable without pre-authoring every future possibility as a fixed branch.

## Consent belongs inside Agency state

Do not build consent as a bolt-on global permission table.

Consent can be represented as a current directional relationship. Examples of dimensions that may matter:

- actor / counterpart;
- scope;
- purpose;
- direction of allowed change;
- depth or boundedness;
- delegation;
- persistence / expiry;
- reversibility;
- sharing / externalization;
- conditions requiring renewed agreement.

These are research dimensions, not yet canonical schema requirements.

## Core hypothesis

Instead of:

```text
IF condition X -> allow
ELSE IF condition Y -> block
ELSE -> deny
```

explore:

```text
current_state
+ proposed_transition
+ relevant_neighborhood
+ root evaluation
= transition result + explanation
```

The machine should activate only the relevant local neighborhood rather than loading every rule or relationship globally.

## Preserve these commitments

1. **Stable identity for state objects.**
2. **Explicit relationships rather than hidden coupling.**
3. **Transition provenance.**
4. **Uncertainty is state, not an error to hide.**
5. **Derived constraints identify their grounding.**
6. **Capability is not treated as wrongdoing.**
7. **No actor gets special constitutional standing by category.**
8. **Old state is not silently rewritten.**
9. **The model remains deterministic at the state-transition layer, even when an intelligence proposes transitions.**
10. **No fake universality.** Prove small state spaces before claiming a general manifold.

## First technical target

Build the smallest deterministic evaluator that can:

1. load a tiny state graph;
2. accept a proposed transition;
3. compute the relevant local dependency/relationship neighborhood;
4. load root-grounded constraints active in that neighborhood;
5. return one of a small set of explicit results;
6. emit an explanation/receipt that names the state, evidence, roots, and constraints involved;
7. preserve the pre-transition state;
8. replay the evaluation deterministically.

A useful initial result vocabulary may be:

```text
accepted
accepted_with_conditions
needs_evidence
needs_clarification
deferred_for_wisdom
conflict
rejected
```

Treat this as a starting vocabulary, not doctrine.

## What to read next

1. [`README.md`](README.md) — project orientation.
2. [`FOUNDATION.md`](FOUNDATION.md) — model and invariants.
3. [`schemas/state-object.schema.json`](schemas/state-object.schema.json) — initial state-object contract.
4. [`schemas/transition.schema.json`](schemas/transition.schema.json) — initial proposed-transition contract.
5. [`NEXT_BUILD.md`](NEXT_BUILD.md) — concrete v0 experiment.

## Builder rule

Do not rebuild this as conventional RBAC/ACL because those tools are familiar. They may be useful adapters later, but the research question here is whether grounded directional state can carry more of the semantics.

Likewise, do not force mystical language into the implementation. Words such as "field", "shape", "direction", and "operational gravity" must eventually reduce to inspectable machine state, deterministic transformations, and measurable behavior.

Preserve the idea; make the poetry computable.
