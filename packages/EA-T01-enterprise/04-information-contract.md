---
id: EA-T01-IC
package: EA-T01
name: Enterprise
document: Information Contract
version: 4.1.0
status: Publication Candidate
authority: Normative
---

# EA-T01 — Information Contract

## 1. Purpose

This contract defines which governed EA‑T01 knowledge must participate in the transformation, when it is conditional or not applicable, and how semantic completeness is determined. Knowledge meaning and applicability are owned by EA‑T01-KA.

## 2. Contract Principles

| ID | Requirement |
|---|---|
| IC-P-001 | The contract SHALL reference Knowledge Unit identifiers from EA‑T01-KA. |
| IC-P-002 | It SHALL NOT redefine Knowledge Units, types or taxonomies. |
| IC-P-003 | Participation SHALL be resolved progressively from Legal Form. |
| IC-P-004 | Not Applicable SHALL NOT be treated as Missing. |
| IC-P-005 | Completeness SHALL be evaluated only over the applicable information set. |

## 3. Participation States

| State | Meaning |
|---|---|
| Required | Must be established for the applicable branch. |
| Conditional | Becomes Required when its governed condition is met. |
| Optional | May be present but does not determine completeness. |
| Not Applicable | Is outside the resolved semantic branch and is excluded from completeness. |

## 4. Core Participation Contract

| Knowledge reference | Participation | Condition |
|---|---|---|
| KF-EI-NAME | Required | At least one authoritative Enterprise name. |
| KF-EI-ID | Conditional | As specified by identifier applicability in EA‑T01-KA. |
| KF-EI-EXIST | Required | Existence state must be established. |
| KU-LC-FORM-001 | Required | Resolves the applicable branch. |
| KF-LS-POWER | Conditional/Required | Per KA-AR-001–007. |
| KU-LS-ROLE-001 | Conditional/Required | Per KA-AR-001–007 and structural role taxonomy. |
| KU-LS-DECISION-001 | Conditional/Required | Per KA-AR-001–007. |

## 5. Progressive Resolution

```text
Enterprise Identity available
        ↓
KU-LC-FORM-001 established
        ↓
KA-AR applicability rules resolved
        ↓
Applicable Knowledge Unit set established
        ↓
Required information acquired
        ↓
Semantic completeness evaluated
```

This is semantic progression, not a prescribed user journey.

## 6. Branch Contract

| Legal Form | Required structural participation |
|---|---|
| Body Corporate | Applicable Governing Powers; subtype-appropriate Structural Role Relationships; Governing Responsibility Relationship |
| Trust or Foreign Equivalent | Governing Powers; Trustee Relationship; Governing Responsibility Relationship |
| Partnership | Governing Powers; Partner Relationship; Governing Responsibility Relationship |
| Individual Acting as Sole Trader | Individual responsibility; other structural knowledge only where legally applicable |
| Unincorporated Association | Governing Powers; Committee Member or Office Holder Relationships; Governing Responsibility Relationship |
| Government Body | Governing Powers; Government Office Relationships; Governing Responsibility Relationship |
| Other | Information required by the resolved legal characteristics under KA-AR-007 |

## 7. Completeness Rules

| ID | Rule |
|---|---|
| IC-SC-001 | Enterprise Identity is complete when the required applicable Knowledge Units in KF-EI-NAME and KF-EI-EXIST are established and applicable identifiers are resolved. |
| IC-SC-002 | Legal Constitution is complete when KU-LC-FORM-001 is established. |
| IC-SC-003 | Legal Structure is complete when all Knowledge Units required by the resolved KA-AR rule are established. |
| IC-SC-004 | Conditional information becomes Required only when its condition is true. |
| IC-SC-005 | Not Applicable information is excluded from the denominator of completeness. |
| IC-SC-006 | Missing required information results in an Incomplete contract state. |
| IC-SC-007 | Conflicting governed assertions result in an Invalid contract state. |

## 8. Dependency Contract

| Information state | Depends on |
|---|---|
| Applicable identifier set | Legal Form, subtype and jurisdiction where relevant |
| Applicable Legal Structure | KU-LC-FORM-001 and KA-AR rule resolution |
| Complete Information Contract | Complete Enterprise Identity, Legal Constitution and applicable Legal Structure |

## 9. Lineage Requirements

Each supplied Knowledge Unit SHALL retain:

- its Knowledge Unit identifier;
- its semantic value or relationship assertion;
- applicable temporal state where required;
- source lineage sufficient for downstream traceability;
- its participation state and applicability basis.

Source evidence is not part of Enterprise meaning; it is linked lineage.

## 10. Transformation Preconditions

EA‑T01-TS may begin canonical construction only when:

1. the applicable branch is resolved;
2. all Required Knowledge Units for that branch are established;
3. no unresolved semantic conflict remains; and
4. the Information Contract state is Complete.

## 11. Boundary

This contract does not define Knowledge Unit meaning, acquisition channels, UI fields, workflow, evidence sufficiency, storage or transformation execution.

## 12. Conformance

A conforming implementation SHALL construct the applicable information set from EA‑T01-KA, preserve participation states and lineage, and evaluate completeness using IC-SC-001–007.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
