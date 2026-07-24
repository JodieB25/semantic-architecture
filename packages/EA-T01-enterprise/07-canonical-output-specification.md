---
id: EA-T01-CO
package: EA-T01
name: Enterprise
document: Canonical Output Specification
version: 1.1.0
status: Publication Candidate
authority: Normative
---

# EA-T01 — Canonical Output Specification

## 1. Purpose

This specification defines the canonical output contract for Enterprise Subject. It does not redefine Enterprise meaning, governed knowledge or transformation mechanics.

## 2. Canonical Output

| Property | Value |
|---|---|
| Output | Enterprise Subject |
| Required state | SS-GUARANTEED |
| Semantic authority | EA‑T01-SS |
| Knowledge authority | EA‑T01-KA |
| Construction authority | EA‑T01-TS |

## 3. Composition

| Canonical component | Authoritative source | Required |
|---|---|---|
| Enterprise Identity | EA‑T01-KA: KF-EI-NAME, KF-EI-ID, KF-EI-EXIST | Yes |
| Legal Constitution | EA‑T01-KA: KU-LC-FORM-001 | Yes |
| Applicable Legal Structure | EA‑T01-KA: applicable KF-LS-POWER, KU-LS-ROLE-001, KU-LS-DECISION-001 | Yes, according to applicability |
| Semantic lineage | EA‑T01-IC and EA‑T01-TS | Yes |
| Output state and guarantees | EA‑T01-TS | Yes |

## 4. Output Validity

An Enterprise Subject is canonical only when:

- EA‑T01-TR-004 constructed it from Complete applicable knowledge;
- EA‑T01-TR-005 asserted SG-001–005;
- all EA‑T01-SS invariants are preserved;
- no non-applicable or downstream meaning has been introduced.

## 5. Output Invariants

| ID | Invariant |
|---|---|
| CO-INV-001 | One Legal Constitution is represented. |
| CO-INV-002 | Enterprise Identity lineage is preserved. |
| CO-INV-003 | Legal Structure contains only applicable knowledge. |
| CO-INV-004 | Structural roles are represented as relationships. |
| CO-INV-005 | Ownership, assessment and operational meaning are absent. |

## 6. Downstream Reliance Contract

Downstream consumers may rely on the Guaranteed Enterprise Subject for:

- Enterprise identity and existence;
- resolved Legal Form;
- applicable governing powers and structural relationships;
- semantic lineage and guarantee state.

They may not infer ownership, control, regulatory classification, risk, operational activity or organisational decisions from the Enterprise Subject.

## 7. Boundary

This specification does not prescribe a database schema, API payload, serialisation format, programming class, UI presentation or storage model.

## 8. Conformance

A conforming representation SHALL contain the canonical components, preserve CO-INV-001–005 and expose its semantic state and lineage without varying authoritative definitions.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
