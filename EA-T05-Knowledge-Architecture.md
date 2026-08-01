---
id: EA-T05-EOC-KA-001
package: EA-T05
name: Enterprise Operating Context Stage 5 Source-Reconciled Knowledge Architecture
version: 0.5.1-remediated
status: Remediated Production Candidate — Awaiting Cross-Artefact Validation
governing_standard: SA-KAS v2.0.0-draft
source_family_derivations:
  - EA-T05-EOC-S3-KF01-P2-KA-001 v0.3.0-working
  - EA-T05-EOC-S3-KF02-P2-KA-001 v0.3.2-working
  - EA-T05-EOC KF-03 Phase 2 v0.2.0-working
  - EA-T05-EOC-S3-KF04-P2-KA-001 v0.1.0-working
  - EA-T05-EOC KF-05 Phase 2 v0.1.0-working
  - EA-T05-EOC-S3-KF06-P2-KA-001 v0.1.0-working
  - EA-T05-EOC-S3-KF07-P2-KA-001 v0.1.0-working
  - EA-T05-EOC-S3-KF08-P2-KA-001 v0.1.0-working
---

# EA-T05 Enterprise Operating Context

# Stage 5 — Source-Reconciled Knowledge Architecture

## 1. Purpose

This artefact consolidates and normalises the eight Stage 3 Knowledge Family derivations into one package-level Knowledge Architecture for Enterprise Operating Context.

It preserves the approved Knowledge Family responsibilities while reconciling duplicated semantic authorities, provisional Knowledge Unit allocations, Semantic Forms, Composition Roles, Attachment Scopes, relationship types, composition patterns, applicability rules, composition rules, invariants, rejected concepts, deferred concepts and downstream-use constraints.

This artefact is a source-reconciled working architecture. It does not constitute a frozen or normative publication.

## 2. Authority Boundary

The Knowledge Architecture governs:

- Knowledge Families;
- Knowledge Units and their definitions;
- Semantic Forms;
- Composition Roles;
- Attachment Scopes;
- governed taxonomy subsets;
- relationship types;
- composition patterns;
- applicability rules;
- composition rules;
- package knowledge invariants;
- source and authority lineage for knowledge structures;
- rejected and deferred concepts; and
- permitted downstream use.

It does not govern:

- Enterprise, Enterprise Service, Designated Service or Reporting Entity identity or definition;
- endpoint meanings owned by the Enterprise Operating Knowledge registers or upstream packages;
- acquisition interaction design;
- transformation execution logic;
- canonical output presentation;
- exploitation, exposure, risk, judgement, response or control conclusions; or
- implementation-specific schemas, interfaces or storage structures.

## 3. Governing Semantic Container and Anchor

### 3.1 Semantic container

```text
Applicable Designated Service Operating Configuration
```

The container preserves the operating-context assertions that belong to one exact applicable Designated Service configuration.

### 3.2 Semantic anchor

```text
Applicable Designated Service Operating Configuration
```

The anchor organises the package composition but does not own the meanings of participating Knowledge Units or referenced endpoints.

### 3.3 Package composition

```text
Applicable Designated Service Operating Configuration
+
Delivery Means Characteristic, where applicable
+
Customer Kind
+
Customer Relationship
+
Service–Channel Relationship, where applicable
+
Geographic Connection Qualification, where applicable
+
Transaction Qualification, where applicable
+
Value Qualification, where applicable
+
Service–Arrangement Relationship, where applicable
+
Operating State Qualification
+
Operating Scale Qualification, where applicable
+
Operating Change Qualification, where applicable
+
Conditional Enrichment Overlay, where activated
+
Applicability
+
Source and Authority Lineage
```

Customer Kind and Customer Relationship participation are mandatory for every valid Applicable Designated Service Operating Configuration. All other branches participate only when selected by their governing applicability conditions. Once selected, each branch is mandatory in full.

## 4. Knowledge Family Register

| Family ID | Name | Normalised responsibility | Stage 4 status |
|---|---|---|---|
| `EA-T05-EOC-KF-01` | Designated Service Operating Characteristics | Governs Delivery Means Characteristic qualification of an exact service-operating configuration. | Retained |
| `EA-T05-EOC-KF-02` | Customer Kind and Relationship Characteristics | Governs Customer Kind qualification and operative Customer Relationship participation. | Retained |
| `EA-T05-EOC-KF-03` | Delivery Channel Characteristics | Governs the operative Service–Channel Relationship. Delivery Channel identity remains upstream-owned. | Retained with duplicate allocation removed |
| `EA-T05-EOC-KF-04` | Country Connection Characteristics | Governs role-specific Geographic Connection Qualification. | Retained |
| `EA-T05-EOC-KF-05` | Transaction and Value Characteristics | Governs Transaction Qualification and Value Qualification. | Retained |
| `EA-T05-EOC-KF-06` | Operating Arrangement Characteristics | Governs the operative Service–Arrangement Relationship. Arrangement identity remains upstream-owned. | Retained with duplicate allocation removed |
| `EA-T05-EOC-KF-07` | Operating Scale and Change Characteristics | Governs Operating State, Operating Scale and Operating Change qualifications. | Retained |
| `EA-T05-EOC-KF-08` | Conditional Operating Enrichment | Governs conditional overlay activation and participation rules; it owns no endpoint Knowledge Unit. | Retained as architectural control family |

## 5. Normalisation Decisions

### 5.1 KF-03 duplicate authority

`EA-T05-EOC-KU-04 — Delivery Channel Qualification` and `EA-T05-EOC-KU-05 — Service–Channel Relationship` expressed the same operative topology between the service-operating configuration and a Delivery Channel.

A qualification label does not constitute a second semantic authority where the meaning is fully relational. In accordance with SA-KAS relationship preservation requirements:

- `EA-T05-EOC-KU-04` is rejected as duplicative;
- `EA-T05-EOC-KU-05 — Service–Channel Relationship` is retained; and
- Delivery Channel identity remains an upstream reference-bearing participant, not a local Knowledge Unit.

### 5.2 KF-06 duplicate authority

`EA-T05-EOC-KU-09 — Operating Arrangement Qualification` and `EA-T05-EOC-KU-10 — Service–Arrangement Relationship` expressed the same operative topology between the service-operating configuration and an Operating Arrangement.

Accordingly:

- `EA-T05-EOC-KU-09` is rejected as duplicative;
- `EA-T05-EOC-KU-10 — Service–Arrangement Relationship` is retained; and
- Operating Arrangement identity remains upstream-owned.

### 5.3 KF-08 participation authority

`EA-T05-EOC-KU-14 — Conditional Operating Enrichment Participation` governed whether referenced knowledge participates rather than an independently defined unit of knowledge.

SA-KAS assigns branch selection to applicability rules and non-authoritative topology to composition patterns. Accordingly:

- `EA-T05-EOC-KU-14` is rejected as a Knowledge Unit;
- its valid meaning is retained as package-level Conditional Enrichment Overlay Pattern and Applicability Rule; and
- Product, Business Activity, Party, Resource, Information, Authority and detailed Temporal meanings remain with their originating authorities.

### 5.4 Customer Kind Attachment Scope

Customer Kind was classified as a Composition-Level Fact in KF-02. Its definition and relationship model establish that it qualifies one exact service-operating configuration. Its normalised Attachment Scope is therefore **Qualified-Target Scope**.

### 5.5 Identifier preservation

Rejected provisional identifiers are not reused or renumbered. The consolidated register preserves gaps for `KU-04`, `KU-09` and `KU-14` and records their disposition explicitly.

## 6. Consolidated Knowledge Unit Register

| KU ID | Knowledge Unit | Family | Semantic Form | Composition Role | Attachment Scope | Status |
|---|---|---|---|---|---|---|
| `EA-T05-EOC-KU-01` | Delivery Means Characteristic | KF-01 | Atomic Governed Value | Qualifier | Qualified-Target Scope | Allocated |
| `EA-T05-EOC-KU-02` | Customer Kind | KF-02 | Atomic Governed Value | Qualifier | Qualified-Target Scope | Allocated; mandatory for every valid service-operating configuration |
| `EA-T05-EOC-KU-03` | Customer Relationship | KF-02 | Relationship | Relationship | Cross-Scope Relationship | Allocated; minimum one customer participation relationship mandatory |
| `EA-T05-EOC-KU-04` | Delivery Channel Qualification | KF-03 | — | — | — | Rejected as duplicate of KU-05 |
| `EA-T05-EOC-KU-05` | Service–Channel Relationship | KF-03 | Relationship | Relationship | Cross-Scope Relationship | Allocated |
| `EA-T05-EOC-KU-06` | Geographic Connection Qualification | KF-04 | Relationship | Qualifier | Qualified-Target Scope | Allocated |
| `EA-T05-EOC-KU-07` | Transaction Qualification | KF-05 | Circumstance | Composed Qualification | Qualified-Target Scope | Allocated; role normalised |
| `EA-T05-EOC-KU-08` | Value Qualification | KF-05 | Quantitative Measure | Measured Qualification | Qualified-Target Scope | Allocated |
| `EA-T05-EOC-KU-09` | Operating Arrangement Qualification | KF-06 | — | — | — | Rejected as duplicate of KU-10 |
| `EA-T05-EOC-KU-10` | Service–Arrangement Relationship | KF-06 | Relationship | Relationship | Cross-Scope Relationship | Allocated |
| `EA-T05-EOC-KU-11` | Operating State Qualification | KF-07 | Attribute | Attribute | Qualified-Target Scope | Allocated |
| `EA-T05-EOC-KU-12` | Operating Scale Qualification | KF-07 | Quantitative Measure | Measured Qualification | Qualified-Target Scope | Allocated |
| `EA-T05-EOC-KU-13` | Operating Change Qualification | KF-07 | Circumstance | Composed Qualification | Qualified-Target Scope | Allocated; role normalised |
| `EA-T05-EOC-KU-14` | Conditional Operating Enrichment Participation | KF-08 | — | — | — | Rejected as applicability/composition control, not KU |

### 6.1 Retained Knowledge Unit count

- Initial allocations before normalisation: 14.
- Retained Knowledge Units after normalisation: 11.
- Rejected duplicate or misclassified allocations: 3.

## 7. Normalised Knowledge Unit Definitions

### 7.1 `EA-T05-EOC-KU-01` — Delivery Means Characteristic

A governed Delivery Means value that qualifies the means by which an applicable Designated Service is provided within one exact service-operating configuration.

Canonical question:

> Which Delivery Means Characteristic applies to this Applicable Designated Service Operating Configuration?

### 7.2 `EA-T05-EOC-KU-02` — Customer Kind

A governed Customer Kind value that qualifies one exact Applicable Designated Service Operating Configuration. At least one Customer Kind SHALL be present for every valid configuration. The value SHALL reference the upstream Customer Configuration authority and SHALL preserve Act, Rules and guidance lineage without representing the upstream list as an exhaustive taxonomy enacted by the Act.

Canonical question:

> Which Customer Kind qualifies this Applicable Designated Service Operating Configuration?

### 7.3 `EA-T05-EOC-KU-03` — Customer Relationship

The mandatory operative relationship connecting the exact Applicable Designated Service Operating Configuration or its exact service-operating branch to at least one customer. The relationship SHALL preserve every customer, including each joint customer, and SHALL preserve the relationship type established by the governing proposition. Acting-for-another, representation and other customer-side relationships are additional topology and SHALL NOT substitute for the mandatory customer participation relationship.

Canonical question:

> Which Customer Relationship participates in this Applicable Designated Service Operating Configuration?

### 7.4 `EA-T05-EOC-KU-05` — Service–Channel Relationship

The operative relationship connecting one exact Applicable Designated Service Operating Configuration with one Delivery Channel.

Canonical question:

> Through which Delivery Channel is this Applicable Designated Service Operating Configuration delivered?

### 7.5 `EA-T05-EOC-KU-06` — Geographic Connection Qualification

A role-specific relationship connecting one exact qualified target in the service-operating composition to one Country, Territory, Place or Jurisdiction reference.

Canonical question:

> Which role-specific Geographic Connection qualifies this target within the Applicable Designated Service Operating Configuration?

### 7.6 `EA-T05-EOC-KU-07` — Transaction Qualification

A governed circumstance preserving the transaction predicates, participants, relationships and logical structure that qualify one exact Applicable Designated Service Operating Configuration.

Canonical question:

> Which Transaction Configuration qualifies this Applicable Designated Service Operating Configuration?

### 7.7 `EA-T05-EOC-KU-08` — Value Qualification

A quantitative qualification preserving value, unit or currency, measurement basis, period, aggregation scope and exact qualified target where applicable.

Canonical question:

> Which Value characteristics qualify this Applicable Designated Service Operating Configuration or its transaction branch?

### 7.8 `EA-T05-EOC-KU-10` — Service–Arrangement Relationship

The operative relationship connecting one exact Applicable Designated Service Operating Configuration with one Operating Arrangement, preserving the arrangement type, participants, topology and responsibility distinctions required by the governing proposition.

Canonical question:

> Through which Operating Arrangement is this Applicable Designated Service Operating Configuration performed or supported?

### 7.9 `EA-T05-EOC-KU-11` — Operating State Qualification

A governed operating-state attribute attached to one exact service-operating target for an effective period.

Canonical question:

> Which Operating State applies to this Applicable Designated Service Operating Configuration?

### 7.10 `EA-T05-EOC-KU-12` — Operating Scale Qualification

A quantitative qualification preserving the scale, prevalence, concentration, distribution or capacity measure, its basis, period and exact target.

Canonical question:

> Which Operating Scale measure qualifies this Applicable Designated Service Operating Configuration?

### 7.11 `EA-T05-EOC-KU-13` — Operating Change Qualification

A governed circumstance preserving the planned or actual change predicates, affected target, temporal scope and underlying facts that qualify one exact service-operating configuration.

Canonical question:

> Which Operating Change applies to this Applicable Designated Service Operating Configuration?

## 8. Semantic Form System

| Semantic Form | Package use | Structural completeness |
|---|---|---|
| Atomic Governed Value | KU-01, KU-02 | One governed value, exact target, qualification relationship, branch, applicability and lineage. |
| Relationship | KU-03, KU-05, KU-06, KU-10 | Source, target, relationship type, branch, basis where material, effective period where material and lineage. |
| Circumstance | KU-07, KU-13 | Circumstance type, underlying predicates and relationships, exact target, branch, source logic and lineage. |
| Quantitative Measure | KU-08, KU-12 | Value, unit or scale, currency where applicable, basis, period, aggregation scope, exact target and derivation lineage. |
| Attribute | KU-11 | Governed attribute value, semantic role, exact target, effective period or basis and lineage. |

No package-specific Semantic Form is introduced.

## 9. Composition Role System

| Composition Role | Package use | Responsibility |
|---|---|---|
| Qualifier | KU-01, KU-02, KU-06 | Qualifies an explicit target without replacing it. |
| Relationship | KU-03, KU-05, KU-10 | Connects governed participants through an operative relationship. |
| Composed Qualification | KU-07, KU-13 | Applies a governed circumstance preserving underlying predicates and relationships. |
| Measured Qualification | KU-08, KU-12 | Applies a quantitative measure to an explicit target. |
| Attribute | KU-11 | Describes an operating state attached to an explicit target. |
| Overlay | Package pattern only | Adds referenced knowledge conditionally without creating a Knowledge Unit or transferring authority. |

## 10. Attachment Scope System

| Attachment Scope | Package use | Rule |
|---|---|---|
| Qualified-Target Scope | KU-01, KU-02, KU-06, KU-07, KU-08, KU-11, KU-12, KU-13 | Assertion attaches to the exact target identified by the governing proposition. |
| Cross-Scope Relationship | KU-03, KU-05, KU-10 | Relationship connects participants or assertions across their native scopes. |
| Profile-Level Shared Fact | Referenced only | A shared fact is established once upstream and linked to applicable branches. |
| Container-Level Fact | Package container metadata only | Belongs to the exact Applicable Designated Service Operating Configuration. |
| Composition-Level Fact | Source-branch metadata only | Belongs to an exact internal branch and is not used as a substitute for Qualified-Target Scope. |

## 11. Consolidated Relationship Register

| Relationship ID | Canonical name | Source type | Target type | Cardinality | Attachment Scope | Owning family |
|---|---|---|---|---|---|---|
| `EA-T05-EOC-REL-001` | `has-delivery-means-characteristic` | Applicable Designated Service Operating Configuration | Delivery Means Characteristic | 1:1 per assertion; 1:n across branch | Qualified-Target Scope | KF-01 |
| `EA-T05-EOC-REL-002` | `has-customer-kind` | Applicable Designated Service Operating Configuration | Customer Kind | 1:n mandatory | Qualified-Target Scope | KF-02 |
| `EA-T05-EOC-REL-003` | `has-customer` | Applicable Designated Service Operating Configuration or exact service-operating branch | Customer | 1:n mandatory; preserve each joint customer | Cross-Scope Relationship | KF-02 |
| `EA-T05-EOC-REL-004` | `delivered-through` | Applicable Designated Service Operating Configuration | Delivery Channel | 1:n where applicable | Cross-Scope Relationship | KF-03 |
| `EA-T05-EOC-REL-005` | `has-geographic-connection` | Exact qualified target | Country, Territory, Place or Jurisdiction | 1:n by role | Qualified-Target Scope | KF-04 |
| `EA-T05-EOC-REL-006` | `has-transaction-configuration` | Applicable Designated Service Operating Configuration | Transaction circumstance | 1:n where applicable | Qualified-Target Scope | KF-05 |
| `EA-T05-EOC-REL-007` | `has-value-qualification` | Applicable service or transaction target | Value measure | 1:n where applicable | Qualified-Target Scope | KF-05 |
| `EA-T05-EOC-REL-008` | `performed-or-supported-through` | Applicable Designated Service Operating Configuration | Operating Arrangement | 1:n where applicable | Cross-Scope Relationship | KF-06 |
| `EA-T05-EOC-REL-009` | `has-operating-state` | Exact service-operating target | Operating State | 1:n over non-overlapping periods | Qualified-Target Scope | KF-07 |
| `EA-T05-EOC-REL-010` | `has-operating-scale` | Exact service-operating target | Operating Scale measure | 1:n by measure and period | Qualified-Target Scope | KF-07 |
| `EA-T05-EOC-REL-011` | `has-operating-change` | Exact service-operating target | Operating Change circumstance | 1:n where applicable | Qualified-Target Scope | KF-07 |
| `EA-T05-EOC-REL-012` | `participates-as-enrichment` | Applicable service-operating branch | Referenced upstream assertion | 0:n | Cross-Scope Relationship | KF-08 pattern authority |

### 11.1 Relationship prohibitions

- A role label does not substitute for an operative relationship.
- Endpoint identity does not substitute for a relationship.
- Relationship meaning is not reduced to a boolean where source, target, role or basis is material.
- Duplicate relationship types are not created solely to express “qualification”.

## 12. Canonical Taxonomy and Subset Register

| Taxonomy or subset | Owning authority | Package treatment | Stage 4 status |
|---|---|---|---|
| Delivery Means Characteristic subset | RR-001 / KF-01 subset authority | Retains admitted RR-001 values and identifiers; no local renaming. | Partial; value reconciliation open |
| Customer Kind values | Upstream Customer Configuration authority | Reference the applicable legal form or legal arrangement. `Foreign Equivalent` SHALL NOT be used as an independent peer Customer Kind; foreign-equivalent status qualifies the applicable form or arrangement under Rules r 6-3. The list remains open beyond expressly identified examples. | Reconciled through higher-authority qualification |
| Customer Relationship types | Upstream Customer/Party relationship authorities | Referenced operative types; no role-label substitution. | Deferred pending complete relationship reconciliation |
| Delivery Channel identities/types | RR-005 | Referenced through Service–Channel Relationship. | No local taxonomy |
| Geographic role and endpoint values | RR-012 and endpoint authorities | Role-specific relationship; endpoint values referenced. | Subset reconciliation open |
| Transaction configuration values | RR-011 | Preserved within Transaction Qualification circumstance. | Taxonomy reconciliation open |
| Value kinds, units and currencies | RR-011 and relevant upstream authorities | Preserved within Value Qualification. | Compatibility rules open |
| Operating Arrangement types | RR-006 | Referenced through Service–Arrangement Relationship. | Subset reconciliation open |
| Operating State values | RR-001/RR-013 and contributing authorities | KU-11 admits target-specific designated-service provision states `Provided/Current`, `Proposed`, `Not Commenced` and `Ceased`. `Suspended` is not a generic service-operating state; `Suspended Registration` may be referenced only when the exact registration target participates. | Reconciled subject to exact-target validation |
| Operating Scale measures | Contributing registers | Direct measures or authorised bands only; no local risk-like scale. | Ownership issue remains open |
| Operating Change types | Contributing registers / RR-013 | Referenced by KU-13. | Harmonisation open |

## 13. Consolidated Composition Pattern Register

### 13.1 `EA-T05-EOC-CP-001` — Atomic Qualification Pattern

**Purpose**

Bind one or more governed atomic values to one exact service-operating target.

**Participating Knowledge Units**

- KU-01 Delivery Means Characteristic;
- KU-02 Customer Kind.

**Completeness**

Each selected branch preserves the complete governed value set, exact target, logical operator, applicability, effective period where required and proposition-level Act, Rules and guidance lineage. KU-02 Customer Kind is selected for every valid Applicable Designated Service Operating Configuration and SHALL contain one or more values.

### 13.2 `EA-T05-EOC-CP-002` — Operative Relationship Pattern

**Purpose**

Preserve source, target, relationship type, basis, role, branch and effective scope for relationships crossing native semantic scopes.

**Participating Knowledge Units**

- KU-03 Customer Relationship;
- KU-05 Service–Channel Relationship;
- KU-10 Service–Arrangement Relationship.

**Completeness**

Every selected relationship branch includes all required endpoints, operative type, basis where material, exact service-operating branch, applicability and proposition-level Act, Rules and guidance lineage. KU-03 Customer Relationship SHALL be instantiated at least once for every valid Applicable Designated Service Operating Configuration. Additional acting-capacity, representation, agency, reliance or other relationship topology SHALL remain distinct and SHALL NOT substitute for the mandatory customer relationship.

### 13.3 `EA-T05-EOC-CP-003` — Role-Specific Geographic Connection Pattern

**Purpose**

Preserve a role-specific connection between an exact qualified target and a geographic endpoint.

**Participating Knowledge Unit**

- KU-06 Geographic Connection Qualification.

### 13.4 `EA-T05-EOC-CP-004` — Transaction and Value Composition Pattern

**Purpose**

Preserve transaction predicates, participants, relationships and logical branches together with value measures attached to their exact transaction or service targets.

**Participating Knowledge Units**

- KU-07 Transaction Qualification;
- KU-08 Value Qualification, where applicable.

Value Qualification is conditionally mandatory where the selected transaction branch includes value, amount, quantity, currency, unit, frequency, volume or aggregation semantics.

### 13.5 `EA-T05-EOC-CP-005` — State, Scale and Change Pattern

**Purpose**

Preserve distinct but composable operating-state, scale and change assertions for one exact target.

**Participating Knowledge Units**

- KU-11 Operating State Qualification;
- KU-12 Operating Scale Qualification, where applicable;
- KU-13 Operating Change Qualification, where applicable.

State, scale and change remain separate authorities and are not merged into one generic operating characteristic.

### 13.6 `EA-T05-EOC-CP-006` — Conditional Enrichment Overlay Pattern

**Purpose**

Attach referenced Product, Business Activity, Party, Resource, Information, Authority or detailed Temporal assertions where a selected core branch cannot be completed without them.

**Authority consequence**

This pattern owns participation topology only. It does not create a Knowledge Unit and does not own referenced endpoint meaning.

## 14. Consolidated Applicability Rule Register

### 14.1 `EA-T05-EOC-AR-001` — Exact Target Selection

A Knowledge Unit branch participates only where an authoritative proposition identifies the exact service-operating configuration or lower-level qualified target to which it applies. KU-02 Customer Kind and KU-03 Customer Relationship are mandatory for every valid Applicable Designated Service Operating Configuration and are not conditional branches.

### 14.2 `EA-T05-EOC-AR-002` — Conditional Mandatory Branch

```text
Condition not satisfied
    → branch absent or governed not-applicable state

Condition satisfied
    → complete branch mandatory
```

No applicable branch is described as optional. This rule does not make KU-02 or KU-03 conditional: those Knowledge Units participate in every valid Applicable Designated Service Operating Configuration.

### 14.3 `EA-T05-EOC-AR-003` — Relationship Completion

Where a source proposition establishes a relationship, all semantically material endpoints, operative type, role, basis, branch and effective scope are mandatory. For `EA-T05-EOC-REL-003`, at least one Customer endpoint is mandatory for every valid Applicable Designated Service Operating Configuration, and each joint customer SHALL remain independently represented.

### 14.4 `EA-T05-EOC-AR-004` — Quantitative Completion

Where a quantitative branch applies, value, unit or scale, currency where applicable, basis, period, aggregation scope, exact target and lineage are mandatory.

### 14.5 `EA-T05-EOC-AR-005` — Conditional Enrichment Activation

An enrichment overlay participates only where:

1. a core branch is selected;
2. that branch cannot be represented completely using the core Knowledge Units alone;
3. the required referenced authority and exact semantic purpose are identified;
4. the complete referenced assertion is linked without copying its meaning; and
5. AUSTRAC-communicated risk information, Rules-specified assessment matters and downstream assessment evidence remain referenced inputs and are not re-owned as EOC endpoint knowledge.

### 14.6 `EA-T05-EOC-AR-006` — No Adjacent-Fact Inference

No Knowledge Unit may be selected solely from an adjacent label or indicator, including:

- Delivery Means from Delivery Channel label;
- Customer Kind from Party identity;
- Geographic Connection from nationality, language or currency;
- Operating Arrangement from organisational structure alone;
- Transaction Qualification from value alone;
- state, scale or change from downstream risk classification.

### 14.7 `EA-T05-EOC-AR-007` — Unresolved State Preservation

Missing, disputed, contradicted or insufficient facts remain unresolved and do not become affirmative assertions or silent not-applicable states.

## 15. Consolidated Composition Rule Register

| Rule ID | Rule |
|---|---|
| `EA-T05-EOC-CR-001` | Every assertion or relationship SHALL attach to one exact service-operating configuration or exact lower-level target. |
| `EA-T05-EOC-CR-002` | Assertions from unrelated service-operating configurations SHALL NOT be combined. |
| `EA-T05-EOC-CR-003` | Source `AND`, `OR`, alternative, conjunctive, conditional, nested and exclusion branches SHALL remain distinguishable. |
| `EA-T05-EOC-CR-004` | Shared endpoint identities and shared facts SHALL be established once at native authority and linked through governed participation. |
| `EA-T05-EOC-CR-005` | Atomic values SHALL NOT absorb relationships, participants, locations, arrangements or quantitative conclusions. |
| `EA-T05-EOC-CR-006` | Relationship assertions SHALL preserve source, target, operative statutory or source-supported predicate, role, basis, cardinality and effective scope where material. `EA-T05-EOC-REL-003` SHALL preserve one or more Customer endpoints for every valid Applicable Designated Service Operating Configuration. |
| `EA-T05-EOC-CR-007` | Quantitative measures SHALL remain attached to the exact target and branch they measure. |
| `EA-T05-EOC-CR-008` | Circumstances SHALL preserve their underlying predicates and relationships and SHALL NOT replace them. |
| `EA-T05-EOC-CR-009` | `Provided/Current`, `Proposed`, `Not Commenced` and `Ceased` designated-service provision states SHALL remain distinguishable by exact target and effective period. `Suspended Registration` SHALL attach only to an exact registration target and SHALL NOT be compiled as a generic service-operating state. |
| `EA-T05-EOC-CR-010` | Conditional enrichment SHALL reference and SHALL NOT duplicate upstream assertions. |
| `EA-T05-EOC-CR-011` | Composition SHALL NOT create exploitation, exposure, risk, likelihood, consequence, response or control conclusions. |
| `EA-T05-EOC-CR-012` | A selected composition branch is valid only where its applicability intersection is non-empty. |

## 16. Package Knowledge Invariants

| Invariant ID | Invariant |
|---|---|
| `EA-T05-EOC-KI-001` | Every semantic meaning has one authoritative owner. |
| `EA-T05-EOC-KI-002` | The Applicable Designated Service Operating Configuration is the package container and anchor, not a replacement endpoint authority. |
| `EA-T05-EOC-KI-003` | Delivery Means and Delivery Channel remain distinct. |
| `EA-T05-EOC-KI-004` | Customer Kind and Customer Relationship remain distinct, and both participate in every valid Applicable Designated Service Operating Configuration with one or more Customer endpoints preserved. |
| `EA-T05-EOC-KI-005` | Geographic Connection remains role-specific and does not collapse to a bare country label. |
| `EA-T05-EOC-KI-006` | Transaction circumstances and Value measures remain distinct and correctly attached. |
| `EA-T05-EOC-KI-007` | Operating Arrangement relationship topology remains distinct from Party identity and legal validity. |
| `EA-T05-EOC-KI-008` | Operating State, Operating Scale and Operating Change remain separate semantic authorities. Operating State values remain target-specific; registration suspension SHALL NOT be generalised to service provision. |
| `EA-T05-EOC-KI-009` | Conditional enrichment is a governed overlay pattern and not a residual Knowledge Unit. |
| `EA-T05-EOC-KI-010` | Applicability selects complete branches; composition preserves what must remain bound. |
| `EA-T05-EOC-KI-011` | Source logic, branch identity, uncertainty and exclusions remain semantic content. |
| `EA-T05-EOC-KI-012` | Shared facts and identities are linked rather than duplicated. |
| `EA-T05-EOC-KI-013` | No unsupported taxonomy value, relationship type, measure, band or conclusion is introduced. |
| `EA-T05-EOC-KI-014` | Every retained Knowledge Unit supports reversible derivation lineage and proposition-level lineage to each applicable Act provision, Rules provision and guidance document segment. Recovery-register lineage SHALL NOT substitute for regulatory-source lineage. |
| `EA-T05-EOC-KI-015` | Downstream artefacts consume and do not redefine Knowledge Architecture meaning. |

## 17. Cross-Family Dependency Model

| Dependent family | Dependency | Purpose | Constraint |
|---|---|---|---|
| All families | EA-T02 / EA-T03 service anchors | Resolve exact service-operating target. | Identity remains upstream-owned. |
| KF-02 | RR-002 Customer Configuration and RR-007 Party references | Resolve the mandatory Customer, Customer Kind and additional customer-side relationship topology. | Preserve at least one Customer endpoint for every valid configuration; preserve each joint customer; do not duplicate Party identity; treat foreign-equivalent status as a qualification of the applicable legal form or arrangement. |
| KF-03 | Delivery Channel authority | Resolve channel endpoint. | No local channel taxonomy unless authorised. |
| KF-04 | Geographic endpoint authorities | Resolve Country, Territory, Place or Jurisdiction. | Role-specific connection mandatory. |
| KF-05 | Transaction Configuration | Preserve transaction grammar and values. | No threshold or reporting conclusion. |
| KF-06 | Party and Authority references | Preserve arrangement participants and authority distinctions. | No legal-validity conclusion. |
| KF-07 | Temporal and contributing measure authorities | Preserve state, period, scale and change. | No invented bands or risk scale. |
| KF-08 | Product, Activity, Party, Resource, Information, Authority and Temporal authorities | Complete selected branches. | Activation purpose required; no copied authority. |

## 17A. Proposition-Level Regulatory Source Traceability Register

| Architecture object | Act lineage | Rules lineage | Guidance lineage | Authority treatment |
|---|---|---|---|---|
| `EA-T05-EOC-KU-01`; `REL-001`; KF-01 subset | ss 16, 21(2)–(3) | rr 4-8, 4-12, 4-14 where the exact delivery proposition applies | *Identify and assess*, pp. 5–7; *Manage and mitigate*, pp. 5–7 | Operating manner and permanent-establishment treatment only; not a universal risk or channel taxonomy. |
| `EA-T05-EOC-KU-02`; `REL-002` | s 5; ss 6, 7, 14, 28, 237–239 | rr 6-1 to 6-4; r 6-3 foreign-equivalent qualification | *Identify and assess*, pp. 7–11 | RR-002 retains endpoint authority; lists are not represented as Act-enumerated or guidance-closed taxonomies. |
| `EA-T05-EOC-KU-03`; `REL-003` | s 5; ss 6(1)–(5B), 7, 28 | rr 6-6, 6-9, 6-19, 6-29 to 6-31 | *Identify and assess*, pp. 7–13 | At least one Customer is mandatory; joint customers remain distinct; representation and acting capacity are additional topology. |
| `EA-T05-EOC-KU-05`; `REL-004` | s 26C(3)(c) | rr 4-5, 4-12, 4-14, 6-25, 6-29 to 6-31, 7-1 | *Identify and assess*, pp. 11–13; *Manage and mitigate*, pp. 1–7 | RR-005 owns channel identity; guidance channel examples remain illustrative unless upstream-governed. |
| `EA-T05-EOC-KU-06`; `REL-005`; CP-003 | ss 6(6), 14, 21, 26C(3)(d), 28(4)(e), 45, 100, 236A | rr 3-2, 4-4, 4-8, 6-25, 6-29 to 6-31, 8-1 to 8-9, 9-3 to 9-8 as role-applicable | *Identify and assess*, pp. 14–18 | Residence, formation, establishment, origin, destination, route and other roles remain distinct. |
| `EA-T05-EOC-KU-07`; `REL-006`; CP-004A–H | s 5; s 6 tables; ss 30(5), 41, 43–46A, 63A–67A, 107–108, 142 | rr 1-4, 1-8, 4-12, 4-14, 5-17 to 5-20, 6-20 to 6-21, 6-32 to 6-35, 8-1 to 8-9, 9-3 to 9-8 where predicates apply | *Identify and assess*, pp. 5–7, 18–23; *Manage and mitigate*, pp. 5–7 | Each subpattern activates only where its exact source predicates apply; reporting and risk conclusions remain excluded. |
| `EA-T05-EOC-KU-08`; `REL-007` | s 5; ss 18–19, 43, 45, 53–54, 63A–67A | rr 4-12, 4-14, 6-20 to 6-21, 8-1 to 8-9, 9-3 to 9-8 where value predicates apply | *Identify and assess*, pp. 5–7, 18–23; *Manage and mitigate*, pp. 5–7 | Preserve value, unit or currency, basis, period, aggregation and translation without reporting or risk inference. |
| `EA-T05-EOC-KU-10`; `REL-008`; CP-002A–H | s 5; ss 12, 21(1), 37–38, 46(5)–(6), 49A, 63A, 236B | rr 4-8, 4-12, 5-17 to 5-20, 6-25, 6-29 to 6-33, 7-1 to 7-3, 8-1 to 8-9 | *Identify and assess*, pp. 11–13; *Manage and mitigate*, pp. 1–12 | Generic package participation does not erase agency, outsourcing, reliance, group, intermediary or obligation-discharge topology. |
| `EA-T05-EOC-KU-11`; `REL-009`; CR-009 | ss 26C(2)–(4), 26D, 26U; s 30(2) | rr 3-2, 3-7, 3-9, 4-17 to 4-24, 4-34 | *Identify and assess*, pp. 1–7; *Program overview*, pp. 1–4 | Service states are target-specific; registration suspension is not a generic service state. |
| `EA-T05-EOC-KU-12`; `REL-010` | ss 26C(2)–(4), 26U | rr 3-3, 3-4, 3-9, 4-4, 4-15, 6-25, 7-1 | *Identify and assess*, pp. 18–23; *Manage and mitigate*, pp. 1–4 | Only source-supported measures of nature, size or complexity; no local risk-like scale. |
| `EA-T05-EOC-KU-13`; `REL-011` | ss 26D, 30(2) | rr 4-30, 4-34, 5-1, 6-30, 7-4 | *Identify and assess*, pp. 1–7; *Manage and mitigate*, pp. 8–12; *Program overview*, pp. 1–4 | Change attaches to an exact changed matter and effective time; no inference from downstream risk. |
| `REL-012`; CP-006; AR-005 | ss 26C(3)(e)–(f), 26D(1)(a)(ii)–(iii), 28(2)(g), 28(4)(f), 236B(3)(c)–(d) | Rules-specified assessment matters and operating dependencies only where exact predicates apply | *Identify and assess*, pp. 14–18; *Manage and mitigate*, pp. 1–12; *Program overview*, pp. 1–4 | AUSTRAC-communicated risk information, assessment matters and guidance examples remain referenced inputs; EOC does not re-own them. |

Guidance entries identify interpretive expectations or illustrative examples and SHALL NOT override Act or Rules authority. Recovery-register lineage remains preserved but SHALL NOT substitute for the regulatory-source lineage above.


## 18. Rejected and Superseded Concepts

| Concept | Disposition | Reason |
|---|---|---|
| Material Service Operating Characteristic | Superseded and prohibited | Unsupported umbrella that crossed family authorities. |
| Service Operating Characteristic umbrella KU | Rejected | Too broad and non-atomic. |
| Relationship Assertion as Semantic Form | Rejected | Not a baseline SA-KAS form and unsupported by change record. Remediation SHALL NOT reintroduce it: mandatory customer participation and source-distinct arrangement topology remain governed relationships using existing Knowledge Units and relationship authorities. |
| Delivery Channel Qualification KU-04 | Rejected | Duplicates the operative Service–Channel Relationship. |
| Operating Arrangement Qualification KU-09 | Rejected | Duplicates the operative Service–Arrangement Relationship. |
| Conditional Operating Enrichment Participation KU-14 | Rejected as KU | Governs applicability/composition participation rather than independent knowledge meaning. |
| Country or Jurisdiction identity KUs | Rejected | Endpoint identity remains upstream-owned. |
| Transaction identity KU | Rejected | Endpoint identity remains upstream-owned. |
| Prevalence and Concentration KUs | Rejected | Quantitative measures within Operating Scale. |
| Technology Change KU | Rejected | Circumstance within Operating Change. |
| Risk, exposure, threshold, legal-validity and control KUs | Rejected | Outside EOC authority. |

## 19. Deferred Concepts and Open Normalisation Matters

| Issue ID | Matter | Required treatment | Blocking effect |
|---|---|---|---|
| `EA-T05-EOC-S4-ISS-001` | Identifier Allocation Register confirmation | Confirm all retained, rejected and reserved identifiers. | Blocks normative publication. |
| `EA-T05-EOC-S4-ISS-002` | Complete Delivery Means subset | Reconcile every RR-001 delivery-means value against family boundaries. | Blocks taxonomy freeze. |
| `EA-T05-EOC-S4-ISS-003` | Customer Kind and Relationship value authorities | Confirm canonical values and operative relationship identifiers. | Blocks taxonomy/relationship freeze. |
| `EA-T05-EOC-S4-ISS-004` | Delivery Channel endpoint taxonomy | Confirm whether a canonical taxonomy exists or open references remain required. | Blocks channel taxonomy freeze only. |
| `EA-T05-EOC-S4-ISS-005` | Geographic roles and endpoint subsets | Reconcile all RR-012 roles and externally maintained classifications. | Blocks geographic subset freeze. |
| `EA-T05-EOC-S4-ISS-006` | Transaction and Value branch completeness | Reconcile RR-011 predicates, linked structures, measures and values. | Blocks KF-05 round-trip validation. |
| `EA-T05-EOC-S4-ISS-007` | Arrangement topology completeness | Reconcile RR-006 participants, roles, responsibility and authority relationships. | Blocks KF-06 round-trip validation. |
| `EA-T05-EOC-S4-ISS-008` | Scale, prevalence and concentration authority | Preserve direct measures, controlled-open measures or authorised bands only. | Blocks unsupported scale values. |
| `EA-T05-EOC-S4-ISS-009` | Conditional enrichment activation mapping | Map every overlay activation to a core branch and exact semantic purpose. | Blocks KF-08 freeze. |
| `EA-T05-EOC-S4-ISS-010` | Representative branch falsification and semantic round-trip | Test materially different propositions from RR-001 to RR-013. | Blocks architecture freeze. |

## 20. Downstream-Use Register

| Downstream artefact | Permitted use | Prohibition |
|---|---|---|
| Information Contract | Define facts required to complete applicable package compositions. | Shall not redefine KUs, relationships, patterns, taxonomies, applicability or composition rules. |
| Information Acquisition Pattern | Acquire enterprise facts and evidence sufficient to establish applicable compositions. | Shall not ask the enterprise for downstream conclusions or duplicate facts across branches. |
| Transformation Specification | Compile established facts and assertions into the governed package composition. | Shall not create absent facts, resolve uncertainty without authority or change semantic ownership. |
| Canonical Output Specification | Publish the governed package state with identities, branches, applicability and lineage. | Shall not compress distinct branches or transfer Knowledge Architecture authority. |
| Prototypes and implementations | Render or operationalise the architecture. | Shall not become semantic authorities. |

## 21. Package Recomposition Requirement

```text
Applicable Designated Service Operating Configuration
        ↓
Select applicable core and overlay patterns
        ↓
Instantiate retained Knowledge Units
        ↓
Preserve exact targets, participants and operative relationships
        ↓
Preserve quantitative basis, state, period and logical branches
        ↓
Preserve applicability and source/authority lineage
        ↓
Reconstruct complete operating-context propositions
```

A reconstructed proposition SHALL preserve all factual predicates, participants, relationships, qualifiers, logical branches, scope limitations, attachment points and material uncertainty states.

It SHALL NOT:

- lose or merge distinct predicates;
- add unsupported predicates;
- collapse unresolved states;
- introduce downstream conclusions; or
- alter endpoint authority.

## 22. Architectural Recompilation Status

| Test | Result |
|---|---|
| Eight Knowledge Family responsibilities derive from the approved Stage 2 boundary | PASS |
| One common semantic container and anchor derive across all families | PASS |
| Provisional Knowledge Units normalise to eleven retained authorities | PASS WITH THREE REJECTIONS |
| Semantic Form, Composition Role and Attachment Scope systems are coherent | PASS |
| Duplicate relationship/qualification authorities removed | PASS |
| Conditional enrichment converted to non-authoritative pattern and applicability rule | PASS |
| Upstream endpoint authority preserved | PASS |
| Downstream dependency direction preserved | PASS |
| Complete taxonomy reconciliation | DEFERRED |
| Representative cross-corpus falsification | DEFERRED |
| Package semantic round-trip validation | DEFERRED |

## 23. Stage 4 Determination

**PASS FOR CONSOLIDATED WORKING ARCHITECTURE WITH BLOCKING FREEZE CONTROLS**

The eight family derivations have been consolidated into one coherent package architecture containing eleven allocated Knowledge Units, twelve relationship types, six composition patterns, seven applicability rules, twelve composition rules and fifteen package invariants.

The architecture is ready for Stage 4 validation and source-fidelity testing. It is not ready for freeze or normative publication until the blocking matters in Section 19 are resolved.


## 24. Stage 5 Source-Reconciliation Amendments

### 24.1 Delivery Channel branch confirmation

RR-005 establishes one independently identifiable Delivery Channel Configuration and an exact Service–Channel relationship. Delivery Means, Technology, Location, Participant and Arrangement remain distinct objects connected by relationships. The Stage 4 rejection of `EA-T05-EOC-KU-04 — Delivery Channel Qualification` is confirmed. `EA-T05-EOC-KU-05 — Service–Channel Relationship` remains the sole KF-03 Knowledge Unit.

The relationship SHALL resolve:

- one exact Applicable Designated Service Operating Configuration;
- one exact Delivery Channel reference governed by RR-005;
- lifecycle and temporal scope by reference where required;
- exact service-channel applicability; and
- evidence and lineage.

### 24.2 Transaction source-pattern expansion

RR-011 contains materially different composition topologies that cannot be represented by one undifferentiated generic transaction branch. No new Knowledge Unit is required. The following source-derived composition subpatterns are added under `EA-T05-EOC-CP-004 — Circumstance Qualification Pattern`:

| Pattern ID | Name | Required governed content |
|---|---|---|
| `EA-T05-EOC-CP-004A` | Transaction Core | Transaction kind, participants, subject, direction, state, exact service attachment and provenance. |
| `EA-T05-EOC-CP-004B` | Value Movement | Transaction subject, amount or quantity, unit or currency, origin, destination and direction. |
| `EA-T05-EOC-CP-004C` | Transaction Instruction | Instructing party, authorised actor, instruction target, instruction status and authority reference. |
| `EA-T05-EOC-CP-004D` | On-Behalf-Of Transaction | Acting party, represented party, authority reference and exact transaction branch. |
| `EA-T05-EOC-CP-004E` | Linked Transaction Set | Each component transaction, relationship form, relationship evidence and component identity. |
| `EA-T05-EOC-CP-004F` | Reversal or Refund | Original transaction, reversing or refunding transaction, affected subject, value and basis. |
| `EA-T05-EOC-CP-004G` | Recurring Transaction Pattern | Pattern reference, component transactions, recurrence rule reference and temporal scope. |
| `EA-T05-EOC-CP-004H` | Settlement | Settlement method, parties, subject and settlement state. |

`EA-T05-EOC-KU-07 — Transaction Qualification` remains a Circumstance and SHALL preserve every underlying predicate and relationship selected by the applicable subpattern. `EA-T05-EOC-KU-08 — Value Qualification` remains a Quantitative Measure attached to the exact transferred or affected subject or transaction component.

### 24.3 Operating Arrangement source-pattern expansion

RR-006 establishes materially distinct arrangement topologies. No new Knowledge Unit is required because the arrangement meaning remains governed by RR-006 and KF-06 owns only the EOC participation relationship. The following source-derived composition subpatterns are added under `EA-T05-EOC-CP-002 — Operative Relationship Pattern`:

| Pattern ID | Name | Required governed content |
|---|---|---|
| `EA-T05-EOC-CP-002A` | Direct Performance | Exact arrangement, service scope and performing enterprise or party. |
| `EA-T05-EOC-CP-002B` | Agency | Principal, agent, authorised purpose or procedure, service scope and retained accountable entity. |
| `EA-T05-EOC-CP-002C` | Outsourced Performance | Accountable entity, provider, outsourced activity, service scope, evidence and retained responsibility. |
| `EA-T05-EOC-CP-002D` | Reporting Group | Group, formation basis, lead entity, members, effective membership and service scope. |
| `EA-T05-EOC-CP-002E` | Reliance | First entity, relied-upon person, procedure, agreement, information access and verification-data access. |
| `EA-T05-EOC-CP-002F` | Obligation Discharge | Discharging member, beneficiary member, exact obligation and applicable conditions. |
| `EA-T05-EOC-CP-002G` | Information Sharing | Sender, recipient, information class, purpose, confidentiality and use constraint. |
| `EA-T05-EOC-CP-002H` | Establishment Attachment | Arrangement, establishment or place, service scope and effective period. |

`EA-T05-EOC-KU-10 — Service–Arrangement Relationship` SHALL preserve the applicable RR-006 arrangement reference and the exact subpattern identity. It SHALL not collapse agency, outsourcing, reliance, group operation or obligation discharge into one generic arrangement label.

### 24.4 Geographic relationship confirmation

RR-012 confirms that geography is role-specific. `EA-T05-EOC-KU-06 — Geographic Connection Qualification` remains valid only where it preserves:

- the exact qualified subject;
- one explicit geographic relationship role;
- one governed place or jurisdiction reference;
- effective scope and source lineage; and
- ordered route position where route sequence is material.

Residence, formation, registration, physical presence, service provision, hosting, origin, destination, route, execution and settlement SHALL remain distinct roles.

### 24.5 Temporal ownership correction

RR-013 owns temporal identity and relationships. `EA-T05-EOC-KU-11 — Operating State Qualification` and `EA-T05-EOC-KU-13 — Operating Change Qualification` SHALL reference RR-013 temporal assertions where period, event time, sequence, recurrence or effective-state boundaries are material. KU-11 admits the designated-service provision states `Provided/Current`, `Proposed`, `Not Commenced` and `Ceased` only at the exact service-provision target. `Suspended Registration` remains a registration-state qualification and SHALL NOT be generalised to the service-operating configuration. No other local temporal value is authorised.

### 24.6 Conditional enrichment activation mapping

The KF-08 overlay is activated only through an exact core-branch insufficiency and an identified semantic purpose.

| Activation ID | Core trigger | Referenced authority | Required purpose |
|---|---|---|---|
| `EA-T05-EOC-ENR-001` | Product materially distinguishes service composition or availability. | RR-003 Product Configuration | Resolve exact Product participation. |
| `EA-T05-EOC-ENR-002` | Business Activity materially distinguishes performance. | RR-004 Business Activity Configuration | Resolve exact Activity participation. |
| `EA-T05-EOC-ENR-003` | A participant, capacity or represented party must be identified. | RR-007 Party Configuration | Resolve exact Party identity and capacity. |
| `EA-T05-EOC-ENR-004` | A resource changes availability, reach, capacity or technology participation. | RR-008 Resource Configuration | Resolve exact Resource participation. |
| `EA-T05-EOC-ENR-005` | Information flow, custody, access or opacity distinguishes operation. | RR-009 Information Configuration | Resolve exact Information participation. |
| `EA-T05-EOC-ENR-006` | Permission, mandate, delegation, reliance or approval affects operation. | RR-010 Authority Configuration | Resolve exact Authority participation. |
| `EA-T05-EOC-ENR-007` | Generic effective state is insufficient to preserve time semantics. | RR-013 Temporal Configuration | Resolve exact temporal role, period, event, recurrence or sequence. |

Every activation SHALL identify the triggering core Knowledge Unit or composition branch, the unresolved precision requirement, the referenced assertion and the exact attachment target. Enrichment SHALL not be activated merely because an upstream register exists.

### 24.7 Identifier reconciliation determination

The available Identifier Allocation Register reserves only EA-T05 namespaces. It does not allocate or approve EA-T05 identifiers. Existing EA-T05 identifiers remain provisional, including rejected identifiers which remain reserved and SHALL NOT be reused. This is a production-control gap and blocks freeze, but does not require renumbering during the Architecture Freeze.

## 25. Stage 5 Package Composition Pattern Register

The normalised package contains the six Stage 4 patterns plus the transaction and arrangement source-derived subpatterns in Section 24. These subpatterns bind existing Knowledge Units and referenced authorities; they do not own semantic meaning.

## 26. Stage 5 Determination

**PASS FOR SOURCE-RECONCILED WORKING ARCHITECTURE — NOT READY FOR FREEZE**

Source reconciliation confirms the eleven retained Knowledge Units. No additional Knowledge Unit is authorised. Transaction and Operating Arrangement fidelity is achieved through source-derived composition subpatterns rather than further decomposition.

Freeze remains blocked by:

1. EA-T05 identifier allocation approval;
2. complete Delivery Means subset reconciliation;
3. Customer Kind and Customer Relationship value-authority reconciliation;
4. Operating Scale measure and band authority reconciliation;
5. complete representative testing for RR-001, RR-002, RR-003, RR-004, RR-007, RR-008, RR-009 and RR-010 branches; and
6. final package-wide semantic round-trip validation after those reconciliations.


## 24. Taxonomy and Value-Authority Reconciliation Amendment

This version incorporates `EA-T05-EOC-TVAR-001 v0.1.0-working`.

- KF-01 Delivery Means subset is closed to `SDC-M-001`, `SDC-M-002`, `SDC-M-004` and `SDC-M-005`.
- `SDC-M-003` is decomposed to geographic/establishment authority; `SDC-M-006` to party/arrangement relationship authority; `SDC-M-007` is a derived composition state.
- KU-02 Customer Kind references the applicable RR-002 legal-form or legal-arrangement value. `Foreign Equivalent` is not an independent peer value: foreign-equivalent status qualifies the applicable form or arrangement under Rules r 6-3, and expressly identified examples are illustrative rather than exhaustive.
- KU-03 preserves the mandatory Customer participation relationship for every valid Applicable Designated Service Operating Configuration. Relationship form references RR-002 `CAV-RL-001`; acting capacity references `CAV-AC-001`; operative representation relationships resolve through RR-002 and RR-007 and remain additional to, not substitutes for, the mandatory Customer relationship.
- KU-12 uses controlled-open, source-bound quantitative measures and expressly authorised bands only. No local Operating Scale taxonomy is authorised.

`EA-T05-EOC-S5-ISS-002`, `EA-T05-EOC-S5-ISS-003` and `EA-T05-EOC-S5-ISS-004` are closed at working level.


## 25. Identifier Allocation Determination

All EA-T05 EOC identifiers published in this package are allocated under `EA-T05-EOC-IDR-001`. No identifier has been renumbered or reused. `EA-T05-EOC-KU-04`, `EA-T05-EOC-KU-09` and `EA-T05-EOC-KU-14` remain permanently reserved with their rejected dispositions.

## 26. Semantic Round-Trip Determination

Package-level architectural recomposition was executed under `EA-T05-EOC-VAL-RT-001`. The test confirms that the normalised families can be decomposed into governed assertions and recomposed without loss of:

- Knowledge Unit identity;
- exact qualified target;
- relationship endpoints and direction;
- logical branch structure;
- applicability state;
- quantitative basis and period where applicable;
- upstream semantic authority; and
- source and authority lineage.

Result: **PASS at architectural round-trip level**.

This determination does not test whether the regulatory corpus contains all propositions required to justify the architecture. Independent regulatory-corpus falsification remains mandatory.

## 27. Publication Determination

**COMPLETE KNOWLEDGE ARCHITECTURE PRODUCTION CANDIDATE — READY FOR INDEPENDENT REGULATORY-CORPUS FALSIFICATION.**
