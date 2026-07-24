---
id: SA-SCS
name: Semantic Compilation Standard
document: Standard
version: 1.2.0
status: Publication Candidate
authority: Normative
---

# Semantic Compilation Standard

## 1. Purpose

This standard defines the reusable execution language for semantic compilation. It does not define domain knowledge or package-specific rules.

## 2. Compiler Phases

| ID | Phase | Required output |
|---|---|---|
| CP-001 | Resolve applicability | Applicable semantic branch |
| CP-002 | Resolve applicable knowledge | Applicable Knowledge Unit set |
| CP-003 | Evaluate completeness | Complete, Incomplete or Invalid state |
| CP-004 | Execute transformation rules | Transformed semantic state |
| CP-005 | Construct canonical output | Canonical semantic object |
| CP-006 | Assert semantic guarantees | Guaranteed semantic object |

## 3. Rule Categories

| Prefix | Category | Responsibility |
|---|---|---|
| AR | Applicability Rule | Resolve governed applicability. |
| SC | Semantic Completeness Rule | Determine whether applicable knowledge is complete. |
| TR | Transformation Rule | Produce or transition semantic state. |
| SG | Semantic Guarantee | State what downstream consumers may rely on. |
| SS | Semantic State | Define a governed compiler state. |

## 4. Normative Rule Schema

Every package-specific rule SHALL define:

| Element | Requirement |
|---|---|
| Identifier | Unique and stable. |
| Purpose | Single semantic responsibility. |
| Preconditions | Required input state. |
| Consumes | Authoritative knowledge references. |
| Evaluation | Declarative semantic test or operation. |
| Produces | Output state or canonical component. |
| Failure state | Governed failure outcome. |
| Guarantees | Assertions established on success. |
| Traceability | Upstream and downstream lineage. |

## 5. Generic Semantic States

| ID | State | Meaning |
|---|---|---|
| SS-CANDIDATE | Candidate | Initial governed information exists. |
| SS-APPLICABLE | Applicable | Applicable semantic branch is resolved. |
| SS-COMPLETE | Complete | Required applicable knowledge is established. |
| SS-ESTABLISHED | Established | Canonical output is constructed. |
| SS-INCOMPLETE | Incomplete | Required applicable knowledge is missing. |
| SS-INVALID | Invalid | Governed assertions are contradictory or fail invariants. |
| SS-GUARANTEED | Guaranteed | Required semantic guarantees are asserted. |

## 6. Execution Requirements

- Applicability SHALL resolve before completeness.
- Completeness SHALL evaluate only applicable knowledge.
- Transformation SHALL be deterministic for identical governed inputs.
- A package SHALL NOT redefine knowledge owned by its Knowledge Architecture.
- Guarantee assertion SHALL follow canonical construction.
- State transitions and rule lineage SHALL be observable.

## 7. Conformance

A compiler conforms when it executes the phases in order, supports the normative rule schema, preserves deterministic semantics and does not import domain meaning into the standard.
