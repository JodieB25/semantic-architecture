---
id: SA-EMS
name: Experience Model Standard
document: Standard
version: 1.1.0-rc1
status: Candidate
authority: Normative
---

# Experience Model Standard

## 1. Purpose

Defines how a Canonical Semantic Model is projected into an enterprise-facing interaction model. An Experience Model is informative, introduces no semantic authority, and remains implementation independent.

## 2. Required Structure

Every Experience Model SHALL use the following section order:

| Order | Section | Required content |
|---:|---|---|
| 1 | Document Identity | Package, version, status, authority, source model and audience |
| 2 | Prototype Objective | What the prototype slice proves |
| 3 | Transformation Boundary | Explicit start state and end state |
| 4 | Prototype Boundary | Included and deferred scope |
| 5 | Starting Context | Canonical upstream state and enterprise action required |
| 6 | End-to-End Journey | Table-led stages showing enterprise, system and compiler behaviour |
| 7 | Experience Principles | Interaction principles that remain invariant |
| 8 | Enterprise Interaction | Controlled selections, review, correction and confirmation behaviour |
| 9 | Compiler Behaviour | Runtime consequences visible through the experience |
| 10 | Canonical Output | Minimum output and lineage guarantees |
| 11 | State Model | Enterprise-facing and system states |
| 12 | Product/UX Latitude | What may vary and what must remain invariant |
| 13 | Acceptance Criteria | Testable prototype conditions |
| 14 | Source Alignment | Governing semantic authority for each concern |
| 15 | Downstream Handover | Consumer, guarantee and transition statement |
| 16 | Completion Boundary | Exact point at which the prototype slice is complete |

## 3. Transformation Boundary

Every Experience Model SHALL prominently identify its boundary:

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | Authoritative state consumed by the experience |
| **End State** | Authoritative canonical state produced or confirmed |

A root transformation MAY begin from governed enterprise facts, declarations and evidence rather than an upstream Canonical Semantic Model.

## 4. Table-Led Presentation

The following content SHALL be expressed as tables wherever applicable:

- transformation boundary;
- prototype scope;
- starting context;
- end-to-end journey;
- enterprise interactions;
- compiler behaviour;
- canonical outputs;
- state model;
- acceptance criteria;
- source alignment; and
- downstream handover.

The end-to-end journey SHALL use:

| Stage | Enterprise Experience | System Behaviour | Compiler Behaviour | Exit Condition |
|---:|---|---|---|---|

## 5. Principles

- Enterprise Recognition
- Progressive Disclosure
- Compiler Ownership
- Enterprise Confirmation
- Deterministic Recomposition
- Correction Through Source Facts
- Explainability
- Canonical Continuity
- Implementation Independence

## 6. Authority Boundaries

The Experience Model SHALL NOT:

- introduce canonical concepts;
- redefine regulatory knowledge;
- replace compiler-owned conclusions with user selections;
- reacquire established upstream facts without an explicit correction path; or
- prescribe implementation technology.

## 7. Prototype Slices

A Prototype Slice MAY defer production branches and exception states. Deferred scope SHALL be explicit. A Prototype Slice SHALL still provide a complete end-to-end demonstration of its bounded transformation.

## 8. Validation

Validate:

| Requirement | Validation question |
|---|---|
| Journey completeness | Does the bounded journey reach the stated end state? |
| Canonical alignment | Does the journey consume and produce the stated canonical states? |
| Enterprise readability | Can a non-specialist recognise and confirm the recomposed meaning? |
| Compiler ownership | Are canonical conclusions compiler-owned? |
| Deterministic correction | Do changes invalidate and recompose dependent state? |
| Explainability | Can results be traced to source facts and semantic authority? |
| Implementation independence | Is visual and technical implementation left open? |
| Downstream readiness | Is the handover guarantee explicit and sufficient? |

The Canonical Semantic Model remains the Single Semantic Authority.
