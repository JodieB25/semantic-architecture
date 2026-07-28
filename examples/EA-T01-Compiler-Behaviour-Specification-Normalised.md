---
id: EA-T01-CBS
name: Enterprise Compiler Behaviour Specification
document: Compiler Behaviour Specification
version: 1.0.0-rc1
status: Draft
authority: Informative
semantic_object: EA-T01 Enterprise
governing_standard: SA-CBS Compiler Behaviour Specification Standard v1.0.0-rc1
---

# EA-T01 Enterprise Compiler Behaviour Specification

## 1. Document Identity

| Property | Value |
|---|---|
| Artefact ID | EA-T01-CBS |
| Canonical Name | EA-T01 Enterprise Compiler Behaviour Specification |
| Semantic Object | EA-T01 Enterprise |
| Version | 1.0.0-rc1 |
| Authority | Informative |
| Status | Draft |
| Governing Standard | SA-CBS v1.0.0-rc1 |

## 2. Purpose

Define the deterministic runtime behaviour required to establish and compile the EA-T01 Canonical Enterprise Model.

EA-T01 is the root semantic transformation. This specification introduces no new semantic authority.

## 3. Compiler Objective

Compile confirmed enterprise facts, declarations and evidence into the Canonical Enterprise Model.

## 4. Transformation Boundary

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | **Confirmed enterprise facts, declarations and evidence** |
| **End State** | **Canonical Enterprise Model** |

## 5. Runtime Context

| Property | Value |
|---|---|
| Current Semantic Object | EA-T01 Enterprise |
| Transformation Type | Root semantic transformation |
| Upstream Input | None — root transformation |
| Downstream Consumer | EA-T02 Business Operating Model |

## 6. Runtime Inputs

Required inputs:

- Enterprise facts
- Enterprise declarations
- Enterprise evidence
- Governing legislative knowledge, referenced but not owned

Compilation SHALL NOT commence until the mandatory enterprise identity inputs are available.

## 7. Dependency Graph

```text
Confirmed Enterprise Facts, Declarations and Evidence
        ↓
Enterprise Identity
        ↓
Legal Constitution
        ↓
Legal Structure
        ↓
Enterprise Reference
        ↓
Canonical Enterprise Model
        ↓
EA-T02 Business Operating Model
```

## 8. Runtime Stages

| Stage | Runtime Stage | Consumes | Compiler Behaviour | Produces |
|---:|---|---|---|---|
| 1 | **Load Enterprise Inputs** | Enterprise facts<br>Enterprise declarations<br>Enterprise evidence | Validate that mandatory root inputs are available.<br>Establish the runtime context for EA-T01. | Validated Enterprise input set<br>Runtime context |
| 2 | **Resolve Enterprise Identity** | Validated Enterprise input set | Resolve Enterprise identity deterministically.<br>Assign or preserve the stable Enterprise identifier. | Enterprise identity |
| 3 | **Establish Legal Constitution** | Enterprise identity<br>Relevant enterprise declarations and evidence | Establish the confirmed legal constitution. | Legal Constitution |
| 4 | **Establish Legal Structure** | Enterprise identity<br>Legal Constitution<br>Relevant enterprise facts and evidence | Establish the confirmed legal structure. | Legal Structure |
| 5 | **Assign Enterprise Reference** | Enterprise identity<br>Legal Constitution<br>Legal Structure | Assign the canonical Enterprise reference.<br>Preserve stable identity and lineage. | Enterprise Reference |
| 6 | **Assemble Canonical Enterprise Model** | Enterprise identity<br>Legal Constitution<br>Legal Structure<br>Enterprise Reference | Compose the canonical Enterprise objects.<br>Attach canonical lineage. | Canonical Enterprise Model |
| 7 | **Publish Canonical Enterprise Model** | Validated Canonical Enterprise Model | Publish the canonical output for downstream consumption. | EA-T02-ready Canonical Enterprise Model |

## 9. Compiler Actions

The compiler SHALL:

- load and validate authoritative Enterprise inputs;
- resolve Enterprise identity deterministically;
- establish legal constitution and legal structure;
- assign stable canonical identifiers;
- preserve identity and lineage;
- assemble the Canonical Enterprise Model; and
- publish the model downstream.

The compiler SHALL NOT:

- redefine legislative meaning;
- invent enterprise facts;
- replace enterprise declarations;
- perform organisational judgement; or
- define downstream business-operating semantics.

## 10. Invalidation Behaviour

| Changed State | Recompile From | Dependent State Invalidated |
|---|---:|---|
| Enterprise input set | Stage 1 | All affected EA-T01 canonical state |
| Enterprise identity | Stage 2 | Legal Constitution, Legal Structure, Enterprise Reference and Canonical Enterprise Model |
| Legal Constitution | Stage 3 | Legal Structure, Enterprise Reference and Canonical Enterprise Model |
| Legal Structure | Stage 4 | Enterprise Reference and Canonical Enterprise Model |
| Enterprise Reference | Stage 5 | Canonical Enterprise Model |

Affected downstream semantic states SHALL be invalidated. Unchanged authoritative inputs SHALL be preserved.

## 11. Recompilation Behaviour

Recompilation SHALL:

- begin from the earliest affected stage;
- preserve stable identifiers where identity is unchanged;
- preserve unchanged canonical objects;
- update affected lineage;
- republish the Canonical Enterprise Model; and
- notify downstream semantic dependencies.

## 12. Canonical Outputs

- Enterprise
- Enterprise Identity
- Legal Constitution
- Legal Structure
- Enterprise Reference
- Canonical Lineage
- Canonical Enterprise Model

## 13. Explainability Behaviour

The compiler SHALL expose:

- source enterprise fact, declaration and evidence references;
- stage outcomes;
- canonical identifiers;
- identity resolution outcome;
- lineage;
- invalidation and recompilation events; and
- reasons for the established Enterprise state.

## 14. Downstream Handover

| Property | Value |
|---|---|
| Consumer | EA-T02 Business Operating Model |
| Handover State | Canonical Enterprise Model |
| Guarantee | Enterprise identity, constitution, structure, reference and lineage are established and validated. |

## 15. Runtime Validation

The compiler SHALL validate:

- deterministic execution;
- mandatory root-input completeness;
- canonical object completeness;
- stable identity;
- complete lineage;
- invalidation correctness;
- recompilation correctness; and
- downstream readiness.

Compilation SHALL fail where mandatory Canonical Enterprise state cannot be established.

## 16. Standards Conformance

| Requirement | Result |
|---|:---:|
| Start and End States explicit | PASS |
| Deterministic runtime | PASS |
| Canonical authority preserved | PASS |
| Dependency graph defined | PASS |
| Runtime stages normalised | PASS |
| Invalidation behaviour defined | PASS |
| Incremental recompilation defined | PASS |
| Explainability preserved | PASS |
| Canonical outputs complete | PASS |
| Downstream handover defined | PASS |
| Implementation independence preserved | PASS |

## 17. Architectural Principle

The compiler establishes the Canonical Enterprise Model.

It does not define business-operating semantics. Those are owned by EA-T02.

## 18. Document Status

| Property | Value |
|---|---|
| Status | Draft |
| Standards Conformance | PASS |
| Ready for Prototype Use | Yes |
| Ready for Freeze | Pending package review |
