---
id: EA-T05-SAC
name: EA-T05 Enterprise Operating Context Semantic Assertion Contract
document: Semantic Assertion Contract
version: 1.0.0
status: Production Candidate
authority: Normative
semantic_object: EA-T05 Enterprise Operating Context
governing_standard: SA-SACS v2.0.0-rc1
reference_implementation: EA-T04 Semantic Assertion Contract v1.0.0-rc1
depends_on:
  - EA-T05 Semantic Specification v1.0.0
  - EA-T05 Knowledge Architecture v0.5.1-remediated
---

# EA-T05 Enterprise Operating Context Semantic Assertion Contract

## Document Identity

| Property | Value |
|---|---|
| Identifier | EA-T05-SAC |
| Semantic Object | EA-T05 Enterprise Operating Context |
| Artefact | Semantic Assertion Contract |
| Authority | Normative |
| Status | Production Candidate |
| Version | 1.0.0 |
| Governing Standard | Semantic Assertion Contract Standard v2.0.0-rc1 |
| Reference Implementation | EA-T04 Semantic Assertion Contract v1.0.0-rc1 |

## 1. Purpose

This contract defines the governed Semantic Assertions and proof obligations that must be semantically sufficient before deterministic compilation of the Canonical Enterprise Operating Context may proceed.

It owns assertion participation, conditionality, dependencies, resolution, sufficiency, lineage and transformation eligibility. It does not redefine semantic meaning, Knowledge Units, acquisition behaviour or transformation rules.

## 2. Contract Object

| Property | Value |
|---|---|
| Contract Object ID | CO-EA-T05-01 |
| Canonical Name | Enterprise Operating Context Determination |
| Definition | The governed contract object containing the assertions and proof obligations that must be semantically sufficient before deterministic compilation of the Canonical Enterprise Operating Context may proceed. |

## 3. Governed States

### 3.1 Participation States

- Required
- Conditional
- Optional
- Not Applicable

### 3.2 Resolution States

- Established
- Explicitly Absent
- Deferred
- Unresolved
- Unsupported by Facts

Not Applicable is a participation state and SHALL NOT be treated as missing. Completeness is evaluated only for Required assertions and applicable Conditional or Optional assertions.

## 4. Semantic Assertions

The assertion inventory is derived from the eleven retained Knowledge Units, the Conditional Enrichment Overlay Pattern, and the package-level applicability, attachment and lineage controls.

### SA-01.01 — Delivery Means Applicability Assertion

**Proposition:** The applicability of Delivery Means Characteristic is resolved for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-01` |
| Knowledge Family | `EA-T05-EOC-KF-01` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-01 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0101` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-01.02 — Delivery Means Characteristic Assertion

**Proposition:** Every applicable Delivery Means Characteristic is established for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-01` |
| Knowledge Family | `EA-T05-EOC-KF-01` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-01.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-01 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0102` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-02.01 — Customer Kind Assertion

**Proposition:** At least one governed Customer Kind qualifies the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-02` |
| Knowledge Family | `EA-T05-EOC-KF-02` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-02 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0201` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-02.02 — Customer Participation Assertion

**Proposition:** At least one Customer participates in the exact Applicable Designated Service Operating Configuration through the governed Customer Relationship.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-03` |
| Knowledge Family | `EA-T05-EOC-KF-02` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-02.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-03 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0202` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-02.03 — Joint Customer Preservation Assertion

**Proposition:** Every joint Customer is independently represented where joint customer participation exists.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-03` |
| Knowledge Family | `EA-T05-EOC-KF-02` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-02.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-03 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0203` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-02.04 — Customer-Side Topology Assertion

**Proposition:** Acting-for-another, representation and other customer-side relationships are preserved as additional topology and do not replace the mandatory Customer Relationship.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-03` |
| Knowledge Family | `EA-T05-EOC-KF-02` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-02.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-03 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0204` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-02.05 — Customer Context Completeness Assertion

**Proposition:** Customer Kind and Customer Relationship are complete for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-03` |
| Knowledge Family | `EA-T05-EOC-KF-02` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-02.01`, `SA-02.02`, `SA-02.03`, `SA-02.04` |
| Attachment scope | Inherited from EA-T05-EOC-KU-03 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0205` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-03.01 — Delivery Channel Applicability Assertion

**Proposition:** The applicability of a Service–Channel Relationship is resolved for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-05` |
| Knowledge Family | `EA-T05-EOC-KF-03` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-05 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0301` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-03.02 — Service–Channel Relationship Assertion

**Proposition:** Every applicable Delivery Channel is connected to the exact Applicable Designated Service Operating Configuration through the governed Service–Channel Relationship.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-05` |
| Knowledge Family | `EA-T05-EOC-KF-03` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-03.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-05 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0302` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-03.03 — Delivery Channel Authority Preservation Assertion

**Proposition:** Delivery Channel identity remains referenced from its upstream authority and is not redefined by EA-T05.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-05` |
| Knowledge Family | `EA-T05-EOC-KF-03` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-03.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-05 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0303` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-04.01 — Geographic Connection Applicability Assertion

**Proposition:** The applicability of each Geographic Connection Qualification is resolved for an exact qualified target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-06` |
| Knowledge Family | `EA-T05-EOC-KF-04` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-06 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0401` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-04.02 — Geographic Role Assertion

**Proposition:** Each applicable Geographic Connection preserves one explicit geographic relationship role.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-06` |
| Knowledge Family | `EA-T05-EOC-KF-04` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-04.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-06 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0402` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-04.03 — Geographic Endpoint Assertion

**Proposition:** Each applicable Geographic Connection identifies one governed Country, Territory, Place or Jurisdiction reference for the exact qualified target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-06` |
| Knowledge Family | `EA-T05-EOC-KF-04` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-04.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-06 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0403` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.01 — Transaction Qualification Applicability Assertion

**Proposition:** The applicability of Transaction Qualification is resolved for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-07` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-07 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0501` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.02 — Transaction Configuration Assertion

**Proposition:** Every applicable Transaction Qualification preserves the governed transaction circumstance and exact service attachment.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-07` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-07 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0502` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.03 — Transaction Predicate and Relationship Assertion

**Proposition:** Every applicable Transaction Qualification preserves its material predicates, participants, relationships and direction.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-07` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-07 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0503` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.04 — Transaction Logical Branch Assertion

**Proposition:** Conjunctive, alternative, conditional, linked, recurring, reversal, refund, instruction and settlement branches remain distinguishable where applicable.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-07` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.03` |
| Attachment scope | Inherited from EA-T05-EOC-KU-07 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0504` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.05 — Value Qualification Applicability Assertion

**Proposition:** Value Qualification participation is resolved for every selected transaction or service branch containing value, amount, quantity, currency, unit, frequency, volume or aggregation semantics.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-08` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-08 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0505` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.06 — Value Measure Assertion

**Proposition:** Every applicable Value Qualification preserves value, unit or currency, measurement basis, period, aggregation scope and exact qualified target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-08` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.05` |
| Attachment scope | Inherited from EA-T05-EOC-KU-08 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0506` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-05.07 — Transaction and Value Distinction Assertion

**Proposition:** Transaction Qualification and Value Qualification remain distinct and are attached to their exact governed targets.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-08` |
| Knowledge Family | `EA-T05-EOC-KF-05` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-05.02`, `SA-05.06` |
| Attachment scope | Inherited from EA-T05-EOC-KU-08 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0507` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-06.01 — Operating Arrangement Applicability Assertion

**Proposition:** The applicability of a Service–Arrangement Relationship is resolved for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-10` |
| Knowledge Family | `EA-T05-EOC-KF-06` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-10 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0601` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-06.02 — Service–Arrangement Relationship Assertion

**Proposition:** Every applicable Operating Arrangement is connected to the exact Applicable Designated Service Operating Configuration through the governed Service–Arrangement Relationship.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-10` |
| Knowledge Family | `EA-T05-EOC-KF-06` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-06.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-10 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0602` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-06.03 — Arrangement Topology Assertion

**Proposition:** The applicable arrangement topology is preserved, including direct performance, agency, outsourcing, reporting group, reliance, obligation discharge, information sharing or establishment attachment where applicable.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-10` |
| Knowledge Family | `EA-T05-EOC-KF-06` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-06.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-10 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0603` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-06.04 — Arrangement Participant and Responsibility Assertion

**Proposition:** Material arrangement participants, roles, service scope, authority and retained responsibility distinctions are preserved.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-10` |
| Knowledge Family | `EA-T05-EOC-KF-06` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-06.03` |
| Attachment scope | Inherited from EA-T05-EOC-KU-10 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0604` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-06.05 — Operating Arrangement Authority Preservation Assertion

**Proposition:** Operating Arrangement identity remains referenced from its upstream authority and is not redefined by EA-T05.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-10` |
| Knowledge Family | `EA-T05-EOC-KF-06` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-06.02` |
| Attachment scope | Inherited from EA-T05-EOC-KU-10 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0605` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.01 — Operating State Assertion

**Proposition:** A governed Operating State is established for the exact service-operating target and effective period.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-11` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-11 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0701` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.02 — Operating State Target-Specificity Assertion

**Proposition:** Operating State remains target-specific and registration suspension is not generalised to service provision.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-11` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-07.01` |
| Attachment scope | Inherited from EA-T05-EOC-KU-11 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0702` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.03 — Operating Scale Applicability Assertion

**Proposition:** The applicability of Operating Scale Qualification is resolved for the exact service-operating target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-12` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-12 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0703` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.04 — Operating Scale Measure Assertion

**Proposition:** Every applicable Operating Scale Qualification preserves a source-supported measure or authorised band, basis, period and exact target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-12` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-07.03` |
| Attachment scope | Inherited from EA-T05-EOC-KU-12 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0704` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.05 — Operating Change Applicability Assertion

**Proposition:** The applicability of Operating Change Qualification is resolved for the exact service-operating target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-13` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KU-13 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0705` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.06 — Operating Change Circumstance Assertion

**Proposition:** Every applicable Operating Change Qualification preserves the planned or actual change predicates, affected target, temporal scope and underlying facts.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-13` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-07.05` |
| Attachment scope | Inherited from EA-T05-EOC-KU-13 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0706` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-07.07 — State Scale and Change Distinction Assertion

**Proposition:** Operating State, Operating Scale and Operating Change remain separate semantic authorities and are not collapsed into one operating characteristic.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KU-13` |
| Knowledge Family | `EA-T05-EOC-KF-07` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-07.01`, `SA-07.04`, `SA-07.06` |
| Attachment scope | Inherited from EA-T05-EOC-KU-13 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0707` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-08.01 — Conditional Enrichment Activation Assertion

**Proposition:** Conditional Operating Enrichment is activated only where a selected core branch cannot be represented completely using core Knowledge Units alone.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CP-006` |
| Knowledge Family | `EA-T05-EOC-KF-08` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-CP-006 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0801` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-08.02 — Enrichment Authority Assertion

**Proposition:** Every activated enrichment identifies the authoritative upstream semantic object or register containing the referenced assertion.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CP-006` |
| Knowledge Family | `EA-T05-EOC-KF-08` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-08.01` |
| Attachment scope | Inherited from EA-T05-EOC-CP-006 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0802` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-08.03 — Enrichment Purpose Assertion

**Proposition:** Every activated enrichment identifies the exact unresolved precision requirement and semantic purpose for participation.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CP-006` |
| Knowledge Family | `EA-T05-EOC-KF-08` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-08.01` |
| Attachment scope | Inherited from EA-T05-EOC-CP-006 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0803` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-08.04 — Enrichment Attachment Assertion

**Proposition:** Every activated enrichment identifies the triggering core branch, referenced assertion and exact attachment target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CP-006` |
| Knowledge Family | `EA-T05-EOC-KF-08` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-08.02`, `SA-08.03` |
| Attachment scope | Inherited from EA-T05-EOC-CP-006 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0804` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-08.05 — Enrichment Ownership Preservation Assertion

**Proposition:** Conditional enrichment references upstream assertions without copying, replacing or transferring their semantic authority.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CP-006` |
| Knowledge Family | `EA-T05-EOC-KF-08` |
| Participation | Conditional |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | `SA-08.04` |
| Attachment scope | Inherited from EA-T05-EOC-CP-006 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0805` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-09.01 — Applicability Resolution Assertion

**Proposition:** Every retained Knowledge Unit and composition branch has an explicit participation state for the exact Applicable Designated Service Operating Configuration.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-AR-001` |
| Knowledge Family | `EA-T05-EOC` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-AR-001 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0901` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-09.02 — Exact Attachment Assertion

**Proposition:** Every assertion and relationship attaches to one exact Applicable Designated Service Operating Configuration or exact lower-level qualified target.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CR-001` |
| Knowledge Family | `EA-T05-EOC` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-CR-001 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0902` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-09.03 — Unresolved State Preservation Assertion

**Proposition:** Missing, disputed, contradicted or insufficient facts remain unresolved and do not become affirmative assertions or silent Not Applicable states.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-AR-007` |
| Knowledge Family | `EA-T05-EOC` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-AR-007 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0903` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-09.04 — Source Logic Preservation Assertion

**Proposition:** Source conjunctions, alternatives, conditions, exclusions, branch identity and material uncertainty remain preserved.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-CR-003` |
| Knowledge Family | `EA-T05-EOC` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-CR-003 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0904` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

### SA-09.05 — Canonical Lineage Assertion

**Proposition:** Every applicable assertion retains complete Knowledge Unit, Knowledge Family, semantic authority and source lineage.

| Contract Property | Value |
|---|---|
| Knowledge authority | `EA-T05-EOC-KI-014` |
| Knowledge Family | `EA-T05-EOC` |
| Participation | Required |
| Resolution states | Established, Explicitly Absent, Deferred, Unresolved, Unsupported by Facts |
| Dependencies | None |
| Attachment scope | Inherited from EA-T05-EOC-KI-014 |
| Temporal scope | Operating-context effective period unless the Knowledge Unit defines a narrower effective period. |
| Lineage identifier | `EA-T05-SAC-TR-0905` |
| Transformation eligibility | Eligible only when applicable and resolved as Established or Explicitly Absent, or when governed as Not Applicable by participation. |

## 5. Pattern Instantiations

### PI-01 — Designated Service Operating Characteristics Pattern Instantiation

**Assertions**

- `SA-01.01`
- `SA-01.02`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-02 — Customer Kind and Relationship Pattern Instantiation

**Assertions**

- `SA-02.01`
- `SA-02.02`
- `SA-02.03`
- `SA-02.04`
- `SA-02.05`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-03 — Delivery Channel Pattern Instantiation

**Assertions**

- `SA-03.01`
- `SA-03.02`
- `SA-03.03`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-04 — Geographic Connection Pattern Instantiation

**Assertions**

- `SA-04.01`
- `SA-04.02`
- `SA-04.03`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-05 — Transaction and Value Pattern Instantiation

**Assertions**

- `SA-05.01`
- `SA-05.02`
- `SA-05.03`
- `SA-05.04`
- `SA-05.05`
- `SA-05.06`
- `SA-05.07`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-06 — Operating Arrangement Pattern Instantiation

**Assertions**

- `SA-06.01`
- `SA-06.02`
- `SA-06.03`
- `SA-06.04`
- `SA-06.05`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-07 — Operating State Scale and Change Pattern Instantiation

**Assertions**

- `SA-07.01`
- `SA-07.02`
- `SA-07.03`
- `SA-07.04`
- `SA-07.05`
- `SA-07.06`
- `SA-07.07`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-08 — Conditional Operating Enrichment Pattern Instantiation

**Assertions**

- `SA-08.01`
- `SA-08.02`
- `SA-08.03`
- `SA-08.04`
- `SA-08.05`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

### PI-09 — Applicability Attachment and Lineage Pattern Instantiation

**Assertions**

- `SA-09.01`
- `SA-09.02`
- `SA-09.03`
- `SA-09.04`
- `SA-09.05`

**Completeness rule**

Every Required assertion and every applicable Conditional assertion in the pattern is resolved without Unresolved or Unsupported by Facts. Assertions governed as Not Applicable are excluded from completeness calculations.

**Result states:** Complete; Incomplete; Not Applicable.

## 6. Compositions

### CP-01 — Core Service Operating Context Composition

- Pattern instantiations: `PI-01`, `PI-02`, `PI-03`, `PI-04`
- Required for: `AG-01`

### CP-02 — Transaction and Value Composition

- Pattern instantiations: `PI-05`
- Required for: `AG-02`

### CP-03 — Operating Arrangement Composition

- Pattern instantiations: `PI-06`
- Required for: `AG-03`

### CP-04 — Operating State Scale and Change Composition

- Pattern instantiations: `PI-07`
- Required for: `AG-04`

### CP-05 — Conditional Enrichment Composition

- Pattern instantiations: `PI-08`
- Required for: `AG-05`

### CP-06 — Applicability Attachment and Lineage Composition

- Pattern instantiations: `PI-09`
- Required for: `AG-06`

## 7. Aggregates

### AG-01 — Core Operating Context Aggregate

- Dependencies: `CP-01`
- Sufficiency rule: Customer Kind and Customer Relationship are complete; every applicable delivery-means, channel and geographic branch is complete; exact attachment and upstream authority are preserved.

### AG-02 — Transaction and Value Aggregate

- Dependencies: `CP-02`
- Sufficiency rule: Every applicable transaction branch preserves its circumstance, predicates, participants, relationships and logic; every applicable value branch preserves its measure, basis, period and target.

### AG-03 — Operating Arrangement Aggregate

- Dependencies: `CP-03`
- Sufficiency rule: Every applicable arrangement branch preserves its authoritative arrangement reference, topology, participants, roles, service scope and responsibility distinctions.

### AG-04 — Operating State Scale and Change Aggregate

- Dependencies: `CP-04`
- Sufficiency rule: Operating State is established; every applicable scale and change branch is complete; state, scale and change remain semantically distinct.

### AG-05 — Conditional Enrichment Aggregate

- Dependencies: `CP-05`
- Sufficiency rule: Every activated enrichment has an exact trigger, purpose, authoritative reference and attachment target, and no semantic ownership is transferred.

### AG-06 — Semantic Integrity Aggregate

- Dependencies: `CP-06`
- Sufficiency rule: Participation, exact attachment, unresolved states, source logic and canonical lineage are complete for the exact Applicable Designated Service Operating Configuration.

### AG-07 — Canonical Enterprise Operating Context Aggregate

- Dependencies: `AG-01`, `AG-02`, `AG-03`, `AG-04`, `AG-05`, `AG-06`
- Sufficiency rule: Every Required assertion and every applicable Conditional assertion is resolved as Established or Explicitly Absent; no applicable assertion is Unresolved or Unsupported by Facts; all exact attachments, semantic distinctions and lineage are complete.

## 8. Transformation Eligibility

### 8.1 Eligible When

- `AG-07` is semantically sufficient.
- No applicable Required or Conditional assertion is Deferred, Unresolved or Unsupported by Facts.
- Every assertion used for transformation has complete Knowledge Unit, Knowledge Family, semantic authority and source lineage.
- Every assertion and relationship has one exact attachment target.
- Not Applicable assertions are excluded from completeness calculations.
- No composition collapses distinct Delivery Means, Delivery Channel, Customer Kind, Customer Relationship, Transaction, Value, Operating Arrangement, Operating State, Operating Scale or Operating Change semantics.

### 8.2 Not Eligible When

- Any applicable Required assertion is Deferred, Unresolved or Unsupported by Facts.
- Any required Pattern Instantiation is incomplete.
- Any applicable Conditional branch is only partially resolved.
- Exact attachment, source logic or semantic lineage is incomplete.
- The assertion set contains conflicting attachment or temporal scopes.
- Conditional enrichment lacks an exact trigger, purpose, authoritative reference or attachment target.
- Any assertion introduces assessment, risk, judgement, response, control or AML/CTF Program semantics.

## 9. Authority and Traceability

This contract references the EA-T05 Knowledge Architecture for Knowledge Unit definitions, relationship meanings, composition patterns, applicability rules, composition rules, invariants and source mappings. It does not duplicate or redefine those authorities.

Every assertion retains:

- its stable assertion identifier;
- its governing Knowledge Unit or package control;
- its governing Knowledge Family;
- its exact attachment scope;
- its temporal scope where material;
- its dependencies; and
- its source and authority lineage.

## 10. Standards and Reference-Implementation QA

| Validation | Result |
|---|:---:|
| Every assertion has a stable identifier and authoritative Knowledge reference | PASS (42 assertions) |
| Only standard participation states are used | PASS |
| Only standard resolution states are used | PASS |
| Not Applicable is excluded from missing-assertion calculations | PASS |
| Completeness hierarchy is explicit: Assertion → Pattern Instantiation → Composition → Aggregate → Canonical Model | PASS (9 patterns; 6 compositions; 7 aggregates) |
| Assertion participation, conditionality, dependencies and sufficiency are owned by the contract | PASS |
| Semantic meaning and Knowledge Unit definitions are not redefined | PASS |
| Acquisition behaviour and transformation rules are not defined | PASS |
| Exact attachment and temporal scope are preserved | PASS |
| Conditional branches become mandatory in full once applicable | PASS |
| Single Semantic Authority is preserved | PASS |
| EA-T04 structural hierarchy is preserved | PASS |

## 11. Validation Metrics

- Assertion count: **42**
- Pattern Instantiation count: **9**
- Composition count: **6**
- Aggregate count: **7**
- Canonical transformation-eligibility aggregate: **AG-07**

## 12. Document Status

| Property | Value |
|---|---|
| Status | Production Candidate |
| Semantic completeness | Complete for contract compilation |
| Standards conformance | PASS |
| Reference implementation conformance | PASS |
| Knowledge authority | Referenced through EA-T05 Knowledge Architecture |
| Open issues | Independent regulatory-corpus falsification and cross-artefact validation remain inherited production controls |
| Promotion condition | Approval of assertion participation, dependencies, aggregate sufficiency and inherited production controls |

## 13. Publication Determination

**PRODUCTION-QUALITY SEMANTIC ASSERTION CONTRACT — PRODUCTION CANDIDATE**

The contract is structurally complete and suitable to govern downstream Semantic Input, Evaluation and Compilation specifications. Its publication status remains Production Candidate because the governing Knowledge Architecture is itself a Production Candidate awaiting independent regulatory-corpus falsification and cross-artefact validation.
