---
id: EA-T01-SS
package: EA-T01
name: Enterprise
document: Semantic Specification
version: 2.1.0
status: Frozen
authority: Normative
---

# EA-T01 — Semantic Specification

## 1. Purpose

This specification is the authoritative semantic contract for Enterprise. It defines what Enterprise means. Governed knowledge is defined in the Knowledge Architecture; input participation, compiler behaviour and output construction are defined downstream.

## 2. Canonical Question

> **What Enterprise exists?**

No other semantic question forms part of EA‑T01 Enterprise.

## 3. Definition

Enterprise is the root Semantic Object within the Enterprise domain. It establishes the minimum semantic meaning necessary to distinguish, constitutionally classify and structurally express an Enterprise.

## 4. Semantic Responsibility

| Enterprise SHALL establish | Enterprise SHALL NOT establish |
|---|---|
| Enterprise Identity | Ownership, Control or Beneficial Ownership |
| Legal Constitution | Business Operating Model or operating behaviour |
| Legal Structure | Regulatory or assessment conclusions |
| Enterprise Subject | Governance decisions or AML/CTF Program content |

## 5. Semantic Grammar

```text
Enterprise
├── Enterprise Identity
├── Legal Constitution
└── Legal Structure
```

## 6. Constituent Semantic Components

| Component | Canonical question | Semantic responsibility |
|---|---|---|
| Enterprise Identity | Which Enterprise is this? | Establish identity, existence and continuity. |
| Legal Constitution | What legally recognised form does it take? | Establish the legal form through which it exists. |
| Legal Structure | Through what legally recognised structure is it constituted? | Establish governing powers and structural relationships. |

The authoritative Knowledge Families and Knowledge Units expressing these components are defined by **EA‑T01-KA**.

## 7. Composition

```text
Enterprise Identity
        +
Legal Constitution
        +
Applicable Legal Structure
        ↓
Enterprise Subject
```

| ID | Composition rule |
|---|---|
| SS-CR-001 | Enterprise Identity SHALL participate. |
| SS-CR-002 | Legal Constitution SHALL participate. |
| SS-CR-003 | Legal Structure SHALL be interpreted according to Legal Constitution and the applicability model owned by EA‑T01-KA. |
| SS-CR-004 | Composition SHALL preserve semantic lineage. |
| SS-CR-005 | Composition SHALL NOT introduce downstream domain or assessment meaning. |

## 8. Semantic Dependencies

Legal Constitution determines which Legal Structure knowledge is applicable. This is a semantic dependency, not an implementation sequence.

## 9. Boundaries

| Inside EA‑T01 Enterprise | Outside EA‑T01 Enterprise |
|---|---|
| Identity and existence | Ownership and control |
| Legal form | Business operations and services |
| Governing powers and structural relationships | Regulatory classification and risk assessment |
| Enterprise Subject | Organisational decisions and governance execution |

## 10. Semantic Invariants

| ID | Invariant |
|---|---|
| SS-INV-001 | Enterprise is the root Semantic Object for the Enterprise domain. |
| SS-INV-002 | Enterprise Identity, Legal Constitution and Legal Structure remain semantically distinct. |
| SS-INV-003 | Legal Structure is relationship-centric. |
| SS-INV-004 | Assessment conclusions are excluded. |
| SS-INV-005 | Missing semantic meaning SHALL NOT be inferred. |
| SS-INV-006 | Enterprise SHALL remain a thin semantic slice. |

## 11. Output

The semantic output is **Enterprise Subject**. Its output contract is defined by **EA‑T01-CO**.

## 12. Conformance

A conforming artefact or implementation SHALL preserve the canonical question, grammar, composition, boundaries and invariants in this specification and SHALL use EA‑T01-KA as the sole authority for governed Enterprise knowledge.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
