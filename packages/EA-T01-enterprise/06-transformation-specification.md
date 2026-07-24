---
id: EA-T01-TS
package: EA-T01
name: Enterprise
document: Transformation Specification
version: 7.2.0
status: Publication Candidate
authority: Normative
conforms_to: Semantic Compilation Standard v1.2
---

# EA-T01 — Transformation Specification

## 1. Purpose

This specification defines the EA‑T01 rules that compile a Complete Information Contract into a canonical Enterprise Subject. Generic compiler phases, rule structure and state semantics are owned by SA-SCS.

## 2. Compiler Profile

EA‑T01 implements CP-001 through CP-006 without modification.

```text
EA-T01 Information Contract
        ↓ CP-001 / AR rules
Applicable Enterprise branch
        ↓ CP-002–003 / SC rules
Complete applicable knowledge
        ↓ CP-004 / TR rules
Established Enterprise Subject
        ↓ CP-006 / SG rules
Guaranteed Enterprise Subject
```

## 3. Preconditions

| ID | Requirement |
|---|---|
| TS-PRE-001 | The input conforms to EA‑T01-IC. |
| TS-PRE-002 | Knowledge references conform to EA‑T01-KA. |
| TS-PRE-003 | KU-LC-FORM-001 is established. |
| TS-PRE-004 | No unresolved conflict prevents applicability resolution. |

## 4. Applicability Rule Catalogue

### EA-T01-AR-001 — Resolve Legal Form Branch

| Property | Definition |
|---|---|
| Purpose | Select the applicable Enterprise structural branch. |
| Preconditions | TS-PRE-001–004 |
| Consumes | KU-LC-FORM-001 |
| Evaluation | Resolve the matching KA-AR-001–007 rule. |
| Produces | SS-APPLICABLE and the applicable Knowledge Unit set. |
| Failure | SS-INCOMPLETE where Legal Form is absent; SS-INVALID where contradictory. |
| Traceability | EA‑T01-KA §6 → EA‑T01-IC §6 |

### EA-T01-AR-002 — Resolve Conditional Identifiers

| Property | Definition |
|---|---|
| Purpose | Select identifiers applicable to the resolved form, subtype and jurisdiction. |
| Consumes | KU-LC-FORM-001; applicable subtype and jurisdiction; KF-EI-ID |
| Evaluation | Apply the identifier applicability statements in EA‑T01-KA §5.2. |
| Produces | Applicable identifier set. |
| Failure | SS-INCOMPLETE where an applicable identifier is unresolved. |

## 5. Completeness Rule Catalogue

### EA-T01-SC-001 — Evaluate Enterprise Identity

| Property | Definition |
|---|---|
| Consumes | KF-EI-NAME, KF-EI-ID and KF-EI-EXIST |
| Evaluation | Apply IC-SC-001. |
| Produces | Complete or Incomplete identity state. |

### EA-T01-SC-002 — Evaluate Legal Constitution

| Property | Definition |
|---|---|
| Consumes | KU-LC-FORM-001 |
| Evaluation | Apply IC-SC-002. |
| Produces | Complete or Incomplete constitution state. |

### EA-T01-SC-003 — Evaluate Applicable Legal Structure

| Property | Definition |
|---|---|
| Consumes | Applicable units from KF-LS-POWER, KU-LS-ROLE-001 and KU-LS-DECISION-001 |
| Evaluation | Apply the resolved KA-AR rule and IC-SC-003–005. |
| Produces | SS-COMPLETE or SS-INCOMPLETE. |

### EA-T01-SC-004 — Detect Semantic Conflict

| Property | Definition |
|---|---|
| Consumes | All participating governed assertions |
| Evaluation | Detect mutually inconsistent identity, form, status, authority or relationship assertions. |
| Produces | SS-INVALID when conflict prevents canonical construction. |

## 6. Transformation Rule Catalogue

### EA-T01-TR-001 — Preserve Enterprise Identity

| Property | Definition |
|---|---|
| Preconditions | EA-T01-SC-001 succeeds. |
| Consumes | Applicable Knowledge Units in KF-EI-NAME, KF-EI-ID and KF-EI-EXIST. |
| Evaluation | Preserve governed values, temporal states and lineage without reinterpretation. |
| Produces | Enterprise Identity canonical component. |
| Guarantee | SG-001. |

### EA-T01-TR-002 — Establish Legal Constitution

| Property | Definition |
|---|---|
| Preconditions | EA-T01-SC-002 succeeds. |
| Consumes | KU-LC-FORM-001. |
| Evaluation | Preserve the resolved Legal Form and authorised taxonomy code. |
| Produces | Legal Constitution canonical component. |
| Guarantee | SG-002. |

### EA-T01-TR-003 — Canonicalise Applicable Legal Structure

| Property | Definition |
|---|---|
| Preconditions | EA-T01-SC-003 succeeds. |
| Consumes | Applicable governing powers and relationship assertions. |
| Evaluation | Construct relationship-centric Legal Structure; exclude non-applicable knowledge; preserve constraints and lineage. |
| Produces | Applicable Legal Structure canonical component. |
| Guarantee | SG-003 and SG-004. |

### EA-T01-TR-004 — Construct Enterprise Subject

| Property | Definition |
|---|---|
| Preconditions | EA-T01-TR-001–003 succeed and no SS-INVALID state exists. |
| Consumes | Enterprise Identity, Legal Constitution and Applicable Legal Structure canonical components. |
| Evaluation | Compose in accordance with SS-CR-001–005. |
| Produces | SS-ESTABLISHED Enterprise Subject. |
| Failure | SS-INCOMPLETE or SS-INVALID. |
| Guarantee | SG-001–005. |

### EA-T01-TR-005 — Assert Semantic Guarantees

| Property | Definition |
|---|---|
| Preconditions | EA-T01-TR-004 succeeds. |
| Evaluation | Verify all output invariants and lineage requirements. |
| Produces | SS-GUARANTEED Enterprise Subject. |

## 7. Knowledge Unit Transformation Matrix

| Knowledge reference | Rule | Canonical destination |
|---|---|---|
| KF-EI-NAME | TR-001 | Enterprise Identity |
| KF-EI-ID | TR-001 | Enterprise Identity |
| KF-EI-EXIST | TR-001 | Enterprise Identity |
| KU-LC-FORM-001 | TR-002 | Legal Constitution |
| KF-LS-POWER | TR-003 | Applicable Legal Structure |
| KU-LS-ROLE-001 | TR-003 | Structural Role Relationships |
| KU-LS-DECISION-001 | TR-003 | Governing Responsibility Relationships |

## 8. State Transitions

| From | Rule/condition | To |
|---|---|---|
| SS-CANDIDATE | AR-001 resolves | SS-APPLICABLE |
| SS-APPLICABLE | SC-001–003 succeed | SS-COMPLETE |
| SS-APPLICABLE | Required knowledge missing | SS-INCOMPLETE |
| Any pre-established state | SC-004 detects conflict | SS-INVALID |
| SS-COMPLETE | TR-001–004 succeed | SS-ESTABLISHED |
| SS-ESTABLISHED | TR-005 succeeds | SS-GUARANTEED |

## 9. Semantic Guarantees

| ID | Guarantee |
|---|---|
| SG-001 | Enterprise identity and continuity are preserved. |
| SG-002 | Legal Constitution is resolved and represented exactly once. |
| SG-003 | Only knowledge applicable to the resolved branch contributes to Legal Structure. |
| SG-004 | Structural roles and governing responsibility are represented as canonical relationships. |
| SG-005 | The Enterprise Subject is internally consistent, traceable and suitable for downstream semantic reliance. |

## 10. Failure Taxonomy

| Failure state | Meaning |
|---|---|
| SS-INCOMPLETE | Required applicable knowledge is missing or unresolved. |
| SS-INVALID | Governed assertions conflict or violate an invariant. |

## 11. Traceability

| Source authority | Transformation use | Output authority |
|---|---|---|
| EA‑T01-KA Knowledge Unit IDs and KA-AR rules | AR, SC and TR rules in this specification | EA‑T01-CO canonical components |
| EA‑T01-IC participation and completeness rules | Preconditions and completeness evaluation | Output validity state |
| EA‑T01-SS composition and invariants | TR-004 and TR-005 | Enterprise Subject guarantees |

## 12. Boundary

This specification does not define Knowledge Unit meaning, generic compiler language, acquisition workflow, evidence sufficiency, UI, storage, API structure or downstream assessment.

## 13. Conformance

A conforming implementation SHALL execute the EA‑T01 rules using SA-SCS, consume only authoritative knowledge references, preserve deterministic output and assert SG-001–005 before exposing a Guaranteed Enterprise Subject.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
