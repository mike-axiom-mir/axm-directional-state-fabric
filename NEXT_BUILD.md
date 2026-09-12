# NEXT BUILD — AXM Directional State Fabric

This is the recommended first implementation sequence for a dedicated builder chat.

## v0 objective

Prove that a small set of state transitions can be evaluated deterministically from explicit relational state and four-root grounding without collapsing the project back into a static permission table.

## Phase 1 — revisioned state graph

Implement a tiny local graph store or deterministic in-memory representation containing:

- state objects;
- typed relationships;
- evidence references;
- explicit uncertainty;
- immutable revision ids.

Acceptance condition: the same input graph serializes canonically and produces the same revision hash.

## Phase 2 — proposed transition

Load and validate [`schemas/transition.schema.json`](schemas/transition.schema.json).

A transition should identify:

- actor;
- base revision;
- intent;
- scope;
- mutations;
- evidence;
- declared uncertainty;
- reversibility.

Acceptance condition: malformed or stale-base proposals fail explicitly.

## Phase 3 — relevant-neighborhood resolver

Given a proposal, compute the smallest inspectable neighborhood that could materially affect the transition.

Start with deterministic graph traversal rules such as:

```text
mutation targets
+ direct relationships
+ dependency edges
+ consent/agency edges
+ evidence edges
+ one configured consequence depth
```

Do not call this universal relevance. Record the algorithm and depth used in every receipt.

Acceptance condition: unrelated state remains dormant and the same graph/proposal selects the same neighborhood.

## Phase 4 — four-root evaluator

Implement the roots as explicit evaluation interfaces, not prose-only ideals.

Each root evaluator should be able to return:

```text
no_objection
supports
needs_evidence
needs_clarification
derives_condition
derives_constraint
conflict
```

Each response must include machine-readable reasons and evidence/state references.

Do not assume a root must block an action. Roots may support a transition as well as constrain it.

Acceptance condition: every nontrivial condition or rejection in v0 names at least one root plus the exact state/evidence that grounds it.

## Phase 5 — result + receipt

Aggregate root evaluations and derived constraints into one explicit result vocabulary, initially:

```text
accepted
accepted_with_conditions
needs_evidence
needs_clarification
deferred_for_wisdom
conflict
rejected
```

Emit a transition receipt containing:

- proposal id;
- base revision;
- neighborhood selection method;
- state objects considered;
- root evaluations;
- derived constraints;
- evidence references;
- unresolved uncertainty;
- final result;
- resulting revision if applied.

Acceptance condition: evaluation is replayable from stored inputs.

## Phase 6 — genesis fixture

Create a deliberately small fixture with 5–10 objects, for example:

```text
human-A
machine-B
project-X
artifact-Y
external-destination-Z
consent-relation-1
evidence-1
objective-1
```

Add typed relationships covering:

- participation;
- dependency;
- consent/delegation;
- provenance;
- external publication;
- uncertainty.

Then test several transitions such as:

1. machine-B edits artifact-Y inside project-X within current delegation;
2. machine-B publishes artifact-Y externally without publication consent;
3. human-A revokes a delegation;
4. machine-B requests a broader direction rather than silently taking it;
5. an irreversible mutation is proposed while relevant evidence is unknown.

The point is not to predetermine "human wins" or "machine wins." The point is to see whether the current state and roots produce a grounded result.

## Phase 7 — shapeable consent experiment

Only after the evaluator works, model consent as directional Agency state with a small number of dimensions discovered from the fixture.

Compare it against a boolean permission representation.

Measure:

- number of special cases required;
- clarity of receipts;
- ability to represent partial delegation;
- revocation;
- expiry;
- direction changes;
- whether derived constraints remain understandable.

Do not claim superiority until the comparison exists.

## Tests to require early

- same state + same proposal -> same result and receipt;
- unknown actor rejected as malformed state, not morally classified;
- capability size does not automatically alter standing;
- stale base revision detected;
- uncertainty survives rather than becoming false certainty;
- rejected transition does not mutate base state;
- accepted transition creates a new revision;
- old revision remains readable;
- each derived constraint includes grounding references;
- a changed consent relationship can change a later evaluation without editing a global permission table.

## Explicit non-goals for v0

Do not start with:

- millions of rules;
- neural state embeddings as authority;
- self-modifying runtime code;
- universal mathematical manifold claims;
- autonomous recursive capability growth;
- replacing operating-system security;
- pretending four-root evaluation has already solved ethics or alignment.

## Stop condition

v0 is complete when a small revisioned state graph can evaluate several materially different proposed transitions, derive constraints from explicit current state and the four roots, preserve uncertainty and provenance, and reproduce every result deterministically.

At that point The Field is a working research object rather than only an idea.
