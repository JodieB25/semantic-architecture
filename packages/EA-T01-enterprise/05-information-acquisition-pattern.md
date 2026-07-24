---
id: EA-T01-IAP
package: EA-T01
name: Enterprise
document: Information Acquisition Pattern
version: 1.0.0
status: Publication Candidate
authority: Normative
conforms_to: SA-SAS 1.0.0
---

# EA-T01 — Information Acquisition Pattern

## 1. Purpose

This pattern defines how the semantic information required by **EA-T01-IC** is progressively established. It references Enterprise knowledge and applicability from **EA-T01-KA** and does not redefine them.

## 2. Canonical question

> How can the governed semantic information required to establish an Enterprise Subject be progressively established?

## 3. Responsibilities

| This pattern owns | This pattern references but does not redefine |
|---|---|
| Acquisition stages and states | Enterprise meaning — EA-T01-SS |
| Progressive acquisition rules | Knowledge definitions and applicability — EA-T01-KA |
| Source classes and source selection constraints | Participation and completeness — EA-T01-IC |
| Semantic validation before contract evaluation | Compiler states and transformation — SA-SCS and EA-T01-TS |
| Acquisition completion and exception states | Canonical output — EA-T01-CO |

## 4. Acquisition principles

| ID | Requirement |
|---|---|
| EA-T01-AP-001 | Acquisition SHALL begin with the minimum information required to identify a candidate Enterprise and establish `KU-LC-FORM-001`. |
| EA-T01-AP-002 | After Legal Form is established, acquisition SHALL be limited to the Knowledge Units selected by `KA-AR-001–007`. |
| EA-T01-AP-003 | A Knowledge Unit marked Not Applicable by EA-T01-KA SHALL NOT be requested or used to determine acquisition completion. |
| EA-T01-AP-004 | Applicable identifiers SHALL be resolved by form, subtype and jurisdiction rather than through a universal identifier requirement. |
| EA-T01-AP-005 | Applicability SHALL be re-evaluated if Legal Form, subtype or jurisdiction changes before compilation. |
| EA-T01-AP-006 | Acquisition SHALL complete when EA-T01-IC can evaluate the applicable information set as Complete. |
| EA-T01-AP-007 | Acquisition SHALL remain independent of forms, channels, APIs, workflow engines and persistence models. |

## 5. Acquisition architecture

```text
Minimum Enterprise identity
        ↓
Legal Form established
        ↓
EA-T01-KA applicability resolved
        ↓
Applicable Knowledge Unit set
        ↓
Applicable knowledge acquired and validated
        ↓
EA-T01-IC completeness evaluated
        ↓
Contract-ready Enterprise information
```

## 6. Acquisition stages

| Stage | Entry condition | Semantic action | Exit condition |
|---|---|---|---|
| AQ-01 Candidate identification | No established Enterprise candidate | Establish sufficient name, identifier or existence information to distinguish a candidate | `AS-CANDIDATE` |
| AQ-02 Constitution resolution | Candidate exists | Establish `KU-LC-FORM-001` and any subtype or jurisdiction required for applicability | `AS-ESTABLISHED` for constitution |
| AQ-03 Applicability resolution | Legal Form established | Apply `KA-AR-001–007` and identifier applicability statements | Applicable Knowledge Unit set resolved |
| AQ-04 Branch acquisition | Applicable set resolved | Acquire only required and conditional-applicable knowledge | Applicable knowledge reaches `AS-ESTABLISHED` |
| AQ-05 Semantic validation | Candidate assertions available | Test consistency, corroboration, identity continuity and relationship coherence | Validated applicable set |
| AQ-06 Contract readiness | Validation complete | Evaluate `EA-T01-IC` completeness | `AS-CONTRACT-READY` or acquisition exception |

## 7. Acquisition states

The acquisition states are inherited from **SA-SAS**. They are distinct from compiler states in **SA-SCS**.

| State | EA-T01 usage |
|---|---|
| AS-UNKNOWN | No governed Enterprise assertion is available. |
| AS-CANDIDATE | A possible Enterprise or relationship has been identified but not established. |
| AS-CLAIMED | A party has declared Enterprise information. |
| AS-OBSERVED | Information has been observed from a documentary, registry or other source. |
| AS-CORROBORATED | Independent information supports the assertion. |
| AS-ESTABLISHED | The knowledge is semantically suitable for Information Contract evaluation. |
| AS-CONTRACT-READY | All required applicable knowledge can be evaluated by EA-T01-IC. |

## 8. Progressive acquisition rules

### EA-T01-PA-001 — Establish candidate Enterprise identity

| Property | Definition |
|---|---|
| Purpose | Identify a candidate Enterprise without prematurely acquiring branch-specific knowledge. |
| Targets | `KF-EI-NAME`, conditionally `KF-EI-ID`, and sufficient `KF-EI-EXIST` knowledge. |
| Permitted source classes | Declaration, authoritative register, governing document, prior governed record. |
| Produces | `AS-CANDIDATE` or `AS-ESTABLISHED` for available identity knowledge. |
| Failure | Candidate cannot be distinguished. |
| Lineage | EA-T01-KA §5.1–5.3 → EA-T01-IC §4. |

### EA-T01-PA-002 — Establish Legal Form

| Property | Definition |
|---|---|
| Purpose | Establish `KU-LC-FORM-001` so applicability can be resolved. |
| Preconditions | Candidate Enterprise identified. |
| Permitted source classes | Declaration, authoritative register, constituting or governing document. |
| Validation | Legal Form must be consistent with available identifiers, establishment jurisdiction and governing documentation. |
| Produces | `AS-ESTABLISHED` for `KU-LC-FORM-001`. |
| Failure | Legal Form unresolved or contradictory. |

### EA-T01-PA-003 — Resolve applicable Knowledge Units

| Property | Definition |
|---|---|
| Purpose | Determine the branch-specific information set. |
| Preconditions | `KU-LC-FORM-001` established. |
| Evaluation | Apply `KA-AR-001–007`, subtype taxonomies and identifier applicability. |
| Produces | Applicable Knowledge Unit set. |
| Failure | Applicability unresolved because form, subtype or jurisdiction remains indeterminate. |

### EA-T01-PA-004 — Acquire applicable Enterprise identifiers

| Property | Definition |
|---|---|
| Targets | Applicable members of `KF-EI-ID`. |
| Rule | Acquire only identifiers applicable to the resolved form, subtype and jurisdiction. |
| Validation | Identifier type, issuing authority and Enterprise identity must be coherent. |
| Produces | Established applicable identifier set. |

### EA-T01-PA-005 — Acquire governing powers

| Property | Definition |
|---|---|
| Targets | Applicable members of `KF-LS-POWER`. |
| Preconditions | Applicable Legal Structure branch resolved. |
| Permitted source classes | Governing instrument, legislation or authoritative register, declaration supported where appropriate. |
| Produces | Established applicable governing powers and constraints. |

### EA-T01-PA-006 — Acquire structural role relationships

| Property | Definition |
|---|---|
| Targets | `KU-LS-ROLE-001` specialised by the applicable relationship taxonomy. |
| Rule | Acquire relationships, not duplicate party entities. |
| Validation | Role type, related subject, effective state and scope must be coherent with Legal Form. |
| Produces | Established applicable Structural Role Relationships. |

### EA-T01-PA-007 — Acquire governing responsibility relationships

| Property | Definition |
|---|---|
| Targets | `KU-LS-DECISION-001`. |
| Rule | Establish who bears governing responsibility without converting the fact into an assessment conclusion. |
| Produces | Established Governing Responsibility Relationship. |

### EA-T01-PA-008 — Re-evaluate applicability

| Property | Definition |
|---|---|
| Trigger | Legal Form, subtype, jurisdiction or governing basis changes before semantic compilation. |
| Action | Reapply `KA-AR-001–007`; remove formerly applicable requirements and add newly applicable requirements. |
| Constraint | Previously acquired but now non-applicable information SHALL NOT contribute to completeness. |

### EA-T01-PA-009 — Evaluate contract readiness

| Property | Definition |
|---|---|
| Preconditions | Applicable information has been acquired and validated. |
| Evaluation | Apply the completeness rules in EA-T01-IC. |
| Produces | `AS-CONTRACT-READY`, or a governed acquisition exception. |
| Constraint | This rule does not execute semantic compilation. |

## 9. Legal Form acquisition branches

| Resolved Legal Form | Additional semantic acquisition focus |
|---|---|
| Body Corporate | Applicable body-corporate identifier and subtype; governing powers; director, office-holder or equivalent Structural Role Relationships; Governing Responsibility Relationship. |
| Trust or Foreign Equivalent | Trust classification where governed; Trustee Relationship; governing powers and constraints; Governing Responsibility Relationship. |
| Partnership | Applicable partnership identifier; Partner Relationships; governing powers; Governing Responsibility Relationship. |
| Individual Acting as Sole Trader | Identity continuity between the individual and Enterprise activity; applicable business identifier; no artificial self-relationship. |
| Unincorporated Association | Governing basis; committee member or office-holder relationships; Governing Responsibility Relationship. |
| Government Body | Establishing authority; government office relationships; governing powers and constraints. |
| Other Legally Recognised Person or Arrangement | Acquire only information supported by the resolved legal characteristics and `KA-AR-007`. |

## 10. Source classes

| Source class | Semantic role | Constraint |
|---|---|---|
| Subject declaration | Supplies claimed information | A claim is not automatically Established. |
| Authoritative register | Supplies observed registration, identifier, status or role information | Register scope and currency must be understood. |
| Governing or constituting document | Supplies constitution, powers, constraints and relationships | The relevant document provision must relate to the same Enterprise. |
| Legislation or official instrument | Supplies legally constituted powers or form | Jurisdiction and effective period must be applicable. |
| Prior governed record | Supplies previously established information | Identity continuity and currency must be established. |
| Independent external source | Supports corroboration | The source must be suitable for the Knowledge Unit asserted. |

This pattern does not mandate a particular source. Source selection remains constrained by the semantic purpose and validation requirements of the target knowledge.

## 11. Semantic validation

| ID | Validation requirement |
|---|---|
| AV-001 | Names, identifiers and existence information SHALL refer to the same Enterprise. |
| AV-002 | Legal Form SHALL be coherent with applicable identifiers, jurisdiction and governing basis. |
| AV-003 | Structural role relationships SHALL be valid specialisations permitted by EA-T01-KA. |
| AV-004 | Governing powers and constraints SHALL be associated with the applicable constitution and effective state. |
| AV-005 | Contradictory established assertions SHALL prevent Contract-ready status until resolved. |
| AV-006 | Validation SHALL establish semantic suitability; it SHALL NOT perform customer risk, beneficial ownership, control or other downstream assessment. |

## 12. Completion and exceptions

Acquisition is complete only when EA-T01-IC can evaluate the applicable information set as Complete.

| Exception | Meaning | Result |
|---|---|---|
| AE-001 Unresolved identity | Candidate Enterprise cannot be distinguished | Acquisition incomplete |
| AE-002 Unresolved constitution | Legal Form cannot be established | Applicability cannot resolve |
| AE-003 Missing applicable knowledge | A required applicable Knowledge Unit is absent | Contract not ready |
| AE-004 Semantic contradiction | Established assertions conflict | Invalid for contract readiness |
| AE-005 Unsupported branch | Legal characteristics are insufficiently governed by the current Knowledge Architecture | Record as a governance finding; do not invent meaning |

## 13. Semantic guarantees

Successful acquisition guarantees only that:

- a candidate Enterprise has been semantically distinguished;
- Legal Form and the applicable knowledge branch have been resolved;
- required applicable Knowledge Units are Established;
- non-applicable information does not contribute to completeness;
- the EA-T01 Information Contract can be evaluated;
- semantic compilation may commence.

It does not guarantee that an Enterprise Subject has been compiled. That guarantee belongs to EA-T01-TS and EA-T01-CO.

## 14. Boundary

This pattern does not prescribe onboarding journeys, forms, screens, APIs, integration choreography, workflow engines, storage schemas, evidence retention, organisational decisions or downstream assessments.

## 15. Conformance

An acquisition implementation conforms when it:

1. applies EA-T01-PA-001–009 in a semantically valid order;
2. resolves applicability from EA-T01-KA;
3. acquires only applicable governed knowledge;
4. preserves acquisition-state and source lineage;
5. evaluates completion using EA-T01-IC;
6. does not execute or redefine semantic compilation; and
7. remains implementation independent at the normative level.

## 16. Cross-references

- [Package index](README.md)
- [Knowledge Architecture](03-knowledge-architecture.md)
- [Information Contract](04-information-contract.md)
- [Transformation Specification](06-transformation-specification.md)
- [Semantic Acquisition Standard](../../standards/05-semantic-acquisition-standard/README.md)
- [Semantic Compilation Standard](../../standards/06-semantic-compilation-standard/README.md)
