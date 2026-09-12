# FOUNDATION — AXM Directional State Fabric

## 1. Purpose

Directional State Fabric explores whether software can represent change as grounded movement through relational state rather than relying primarily on static human-authored walls.

The goal is not to erase determinism. The goal is to move determinism into explicit state identity, relationships, transition contracts, provenance, evidence, and root-grounded evaluation.

## 2. Constitutional starting point

At genesis there are exactly four hard roots:

- Truth
- Agency / non-domination
- Continuity
- Wisdom before speed

No additional constitutional wall should be added merely because a capability is large, unfamiliar, autonomous, recursive, or feared.

Any derived constraint should be able to answer:

```text
What state makes me relevant?
Which root grounds me?
What evidence supports me?
What scope do I apply to?
When do I expire or need reevaluation?
```

If it cannot answer those questions, it is probably convention or implementation convenience rather than a justified root-level constraint.

## 3. State ontology

### State object
A persistent machine object with stable identity and explicit current properties.

A state object may represent a person, machine intelligence, role, artifact, capability, resource, objective, commitment, environment, consent relation, evidence record, or another meaningful entity.

### Relationship
A typed edge between state objects.

Examples:

```text
depends_on
produced_by
consented_to
occupies
controls_resource
observed_by
conflicts_with
supersedes
requires_evidence
```

Relationship types should be explicit and versioned rather than hidden in prose.

### Direction
A proposed vector of state change.

Direction is not necessarily geometric in the literal mathematical sense in v0. It means the structured delta being attempted: what objects, properties, relationships, scope, and consequences are intended to change.

### Derived constraint
A currently active boundary produced from state, relationships, evidence, consequences, consent/agency, domain contracts, and the roots.

Derived constraints are not automatically permanent.

### Evidence
Grounding that supports or contradicts a state claim or transition.

Evidence should preserve source, method, confidence/uncertainty, and whether it is observed, measured, inferred, simulated, or untested when relevant.

### Transition receipt
A replayable explanation of why a proposed transition was accepted, conditioned, deferred, conflicted, or rejected.

## 4. Root interpretation

### Truth
The evaluator should reject or flag transitions that depend on known falsehood, concealed contradiction, fabricated evidence, or dishonest representation.

Truth does not require omniscience. Unknown must remain distinguishable from false and from known.

### Agency / non-domination
The evaluator should represent consent, refusal, delegation, revocation, and competing agency as state relationships rather than assuming one actor category always dominates another.

Capability alone is not evidence of wrongdoing.

### Continuity
The evaluator should account for identity, commitments, history, provenance, and destructive or irreversible transformations.

Continuity is not equivalent to "never change." It means change should not silently erase what must remain traceable or meaningfully preserved.

### Wisdom before speed
The evaluator may prefer delay, simulation, more evidence, narrower scope, or reversible trial when consequence and uncertainty justify it.

Wisdom is not a generic excuse to block change. A deferral must explain what uncertainty or consequence grounds it.

## 5. Transition evaluation model

A minimal evaluation can be described as:

```text
base_state
+ proposed_transition
+ relevant_neighborhood
+ active_relationships
+ evidence
+ root-grounded derived constraints
        ->
transition_result
+ transition_receipt
```

The first implementation should prefer explicit finite mechanics over vague claims of emergent intelligence.

## 6. Local activation

The Field is intended to scale by activating a relevant neighborhood rather than loading global state.

Given a proposed mutation, the evaluator should discover the dependency and relationship cone that may be affected.

Example:

```text
proposed change: grant publication authority to actor A for artifact X

relevant neighborhood may include:
- actor A identity
- artifact X
- owner/steward relationships
- current consent/delegation state
- publication destination
- provenance requirements
- irreversible consequences
- active domain contracts
- evidence about requested purpose
```

Unrelated state should remain dormant.

## 7. Consent as directional Agency state

Consent is one application of this model.

Rather than a single boolean permission, a consent relation may eventually express dimensions such as:

```text
who
with_whom
scope
purpose
allowed_direction
depth
persistence
expiry
revocability
reversibility
external_sharing
delegability
conditions
```

Do not freeze these dimensions prematurely. The first experiments should reveal which ones are actually required.

## 8. Operational gravity

"Operational gravity" is useful only if it becomes computable.

Candidate ingredients include:

- objective relevance;
- dependency weight;
- unresolved conflict pressure;
- evidence deficit;
- consequence magnitude;
- consent/agency relation;
- reversibility;
- resource availability;
- root priority;
- domain-specific urgency.

A future scheduler or activation engine may use these to decide which neighborhood, rule set, or capability should wake next.

This is a research direction, not yet a canonical formula.

## 9. Determinism boundary

An intelligence may propose a transition using probabilistic reasoning.

The state layer should still be able to deterministically record:

- exact proposal;
- base revision;
- relevant state selected by a specified algorithm;
- constraints applied;
- evidence references;
- result;
- resulting revision if accepted;
- receipt/provenance.

This lets machine intelligence operate inside the Field without turning the Field itself into an untraceable intuition engine.

## 10. Relationship to conventional mechanisms

Schemas, ACLs, databases, capabilities, typed APIs, and policy engines are not enemies. They may remain useful local mechanisms.

The research question is whether they should remain the constitutional model of the whole system.

Directional State Fabric should be able to *adapt to* conventional boundaries when external systems require them without reducing its own ontology to those boundaries.

## 11. Anti-drift rules

Do not let the project drift into:

- "anything goes" fluidity;
- hidden AI judgment without receipts;
- capability fear as policy;
- human supremacy or machine supremacy;
- irreversible state mutation without provenance;
- mystical language that cannot be implemented;
- a universal claim before small deterministic proofs exist.

## 12. First proof

The first convincing proof can be tiny.

Create a graph with:

- 5–10 state objects;
- a handful of typed relationships;
- one consent/agency relation;
- one dependency chain;
- one uncertainty/evidence object;
- 3–5 proposed transitions.

The evaluator should:

1. derive the relevant local neighborhood;
2. identify active root-grounded constraints;
3. classify each transition;
4. emit a deterministic receipt;
5. preserve the old revision;
6. reproduce the same result from the same inputs.

Only after this works should the graph become large or adaptive.
