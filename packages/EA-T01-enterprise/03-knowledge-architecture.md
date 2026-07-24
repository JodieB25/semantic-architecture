---
id: EA-T01-KA
package: EA-T01
name: Enterprise
document: Knowledge Architecture
version: 1.1.0
status: Publication Candidate
authority: Normative
---

# EA-T01 — Knowledge Architecture

## 1. Purpose and Authority

This specification is the sole authority for the governed knowledge that expresses EA‑T01 Enterprise. It defines Knowledge Families, Knowledge Units, semantic types, taxonomies, relationships, applicability and knowledge invariants. It does not redefine the meaning or boundary of Enterprise, which are owned by EA‑T01-SS.

## 2. Governing Principles

| ID | Principle | Requirement |
|---|---|---|
| KA-P-001 | Thin Slice | Recover only knowledge necessary to establish Enterprise. |
| KA-P-002 | Single Semantic Authority | Knowledge definitions SHALL exist only in this specification. |
| KA-P-003 | Relationship-Centric Modelling | Legal Structure SHALL model legally meaningful relationships rather than duplicate parties. |
| KA-P-004 | Assessment Separation | Facts and relationships belong here; assessment conclusions do not. |
| KA-P-005 | Constitution-Driven Applicability | Legal Form determines applicable structural knowledge. |

## 3. Knowledge Composition

| Semantic component | Knowledge Family | Family ID |
|---|---|---|
| Enterprise Identity | Enterprise Names | KF-EI-NAME |
| Enterprise Identity | Enterprise Identifiers | KF-EI-ID |
| Enterprise Identity | Enterprise Existence | KF-EI-EXIST |
| Legal Constitution | Legal Form | KF-LC-FORM |
| Legal Structure | Governing Powers | KF-LS-POWER |
| Legal Structure | Structural Roles and Relationships | KF-LS-ROLE |
| Legal Structure | Governing Decision-Makers | KF-LS-DECISION |

## 4. Semantic Type System

| Type | Meaning |
|---|---|
| Name | A designation by which the Enterprise is known. |
| Identifier | A governed value used to distinguish or register the Enterprise. |
| Temporal | A date or period relevant to existence or status. |
| Jurisdiction | A legal or administrative place of constitution or registration. |
| State | A governed condition effective at a point in time. |
| Classification | A governed categorisation of legal form or subtype. |
| Authority | A legally meaningful power, delegation or constraint. |
| Relationship | A legally meaningful connection between the Enterprise and another subject or role-holder. |
| Constraint | A limitation on authority or operation of a relationship. |

## 5. Knowledge Unit Register

### 5.1 Enterprise Names — KF-EI-NAME

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-EI-NAME-001 | Enterprise Legal Name | Name | The legally recognised name of the Enterprise. |
| KU-EI-NAME-002 | Enterprise Business Name | Name | A registered or otherwise governed business name used by the Enterprise. |
| KU-EI-NAME-003 | Enterprise Other Known Name | Name | A non-primary name by which the Enterprise is known. |
| KU-EI-NAME-004 | Enterprise Former Name | Name | A prior governed name of the same Enterprise. |

### 5.2 Enterprise Identifiers — KF-EI-ID

| ID | Knowledge Unit | Type | Applicability |
|---|---|---|---|
| KU-EI-ID-001 | Australian Business Number | Identifier | Conditional |
| KU-EI-ID-002 | Australian Company Number | Identifier | Australian Company |
| KU-EI-ID-003 | Australian Registered Body Number | Identifier | Registered Australian body where applicable |
| KU-EI-ID-004 | Australian Registered Scheme Number | Identifier | Registered scheme where applicable |
| KU-EI-ID-005 | Incorporated Association Identifier | Identifier | Incorporated association where applicable |
| KU-EI-ID-006 | Foreign Enterprise Identifier | Identifier | Foreign Enterprise where applicable |

A generic “Government Identifier” is not a governed Knowledge Unit in Version 1.1 because no sufficiently precise semantic definition has been established.

### 5.3 Enterprise Existence — KF-EI-EXIST

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-EI-EXIST-001 | Establishment Date | Temporal | The date on which the Enterprise was legally established. |
| KU-EI-EXIST-002 | Establishment Jurisdiction | Jurisdiction | The jurisdiction under which the Enterprise was established. |
| KU-EI-EXIST-003 | Existence Status | State | The governed status of the Enterprise’s legal existence. |
| KU-EI-EXIST-004 | Existence Status Effective Date | Temporal | The date from which the Existence Status applies. |

Evidence references are excluded; they belong to an Evidence Model rather than the Enterprise knowledge model.

### 5.4 Legal Form — KF-LC-FORM

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-LC-FORM-001 | Legal Form | Classification | The legally recognised form through which the Enterprise exists. |

#### Primary Legal Form Taxonomy

| Code | Legal Form |
|---|---|
| LF-01 | Individual Acting as Sole Trader |
| LF-02 | Body Corporate |
| LF-03 | Partnership |
| LF-04 | Trust or Foreign Equivalent |
| LF-05 | Unincorporated Association |
| LF-06 | Government Body |
| LF-07 | Other Legally Recognised Person or Arrangement |

#### Body Corporate Taxonomy

| Code | Body Corporate subtype |
|---|---|
| BC-01 | Australian Company |
| BC-02 | Foreign Body Corporate |
| BC-03 | Incorporated Association |
| BC-04 | Registered Co-operative |
| BC-05 | Incorporated Partnership |
| BC-06 | Other Body Corporate |

“Company” is a subtype, not the primary constitutional concept. “Registered Foreign Body” is a registration condition and is not a primary Legal Form.

### 5.5 Governing Powers — KF-LS-POWER

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-LS-POWER-001 | Governing Authority Basis | Authority | The legal or constitutional source from which governing authority arises. |
| KU-LS-POWER-002 | Binding Authority | Authority | Authority to bind the Enterprise. |
| KU-LS-POWER-003 | Governance Decision Authority | Authority | Authority to make governance decisions for the Enterprise. |
| KU-LS-POWER-004 | Delegation Model | Authority | The governed basis on which authority may be delegated. |
| KU-LS-POWER-005 | Authority Constraints | Constraint | Limits applying to a governing or delegated authority. |

### 5.6 Structural Roles and Relationships — KF-LS-ROLE

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-LS-ROLE-001 | Structural Role Relationship | Relationship | A legally meaningful relationship between the Enterprise and a subject occupying a structural role. |

#### Structural Role Taxonomy

| Code | Role specialisation |
|---|---|
| SR-01 | Director Relationship |
| SR-02 | Trustee Relationship |
| SR-03 | Partner Relationship |
| SR-04 | Committee Member Relationship |
| SR-05 | Office Holder Relationship |
| SR-06 | Government Office Relationship |
| SR-07 | Other Legally Recognised Structural Role Relationship |

Role-holders are not duplicated as Knowledge Units. The relationship links the Enterprise to a separately established subject.

### 5.7 Governing Decision-Makers — KF-LS-DECISION

| ID | Knowledge Unit | Type | Definition |
|---|---|---|---|
| KU-LS-DECISION-001 | Governing Responsibility Relationship | Relationship | A legally meaningful relationship identifying a subject or body that carries governing decision responsibility for the Enterprise. |

## 6. Applicability Rules

| ID | Condition | Applicable knowledge |
|---|---|---|
| KA-AR-001 | Legal Form = Body Corporate | Governing Powers; Structural Role Relationships appropriate to subtype; Governing Responsibility Relationship |
| KA-AR-002 | Legal Form = Trust or Foreign Equivalent | Governing Powers; Trustee Relationship; Governing Responsibility Relationship |
| KA-AR-003 | Legal Form = Partnership | Governing Powers; Partner Relationship; Governing Responsibility Relationship |
| KA-AR-004 | Legal Form = Individual Acting as Sole Trader | Governing Powers only where a legally distinct basis exists; no artificial self-relationship |
| KA-AR-005 | Legal Form = Unincorporated Association | Governing Powers; Committee Member or Office Holder Relationships; Governing Responsibility Relationship |
| KA-AR-006 | Legal Form = Government Body | Governing Powers; Government Office Relationships; Governing Responsibility Relationship |
| KA-AR-007 | Legal Form = Other | Applicable knowledge SHALL be established from the recognised legal characteristics without importing a known-form taxonomy by analogy. |

## 7. Applicability Matrix

| Knowledge Family | Sole Trader | Body Corporate | Partnership | Trust | Unincorporated Association | Government Body | Other |
|---|---|---|---|---|---|---|---|
| Enterprise Names | Required | Required | Required | Required | Required | Required | Required |
| Enterprise Identifiers | Conditional | Conditional | Conditional | Conditional | Conditional | Conditional | Conditional |
| Enterprise Existence | Required | Required | Required | Required | Required | Required | Required |
| Legal Form | Required | Required | Required | Required | Required | Required | Required |
| Governing Powers | Conditional | Required | Required | Required | Required | Required | Conditional |
| Structural Role Relationships | Not applicable by default | Required | Partner | Trustee | Committee/office holder | Government office | Conditional |
| Governing Responsibility Relationship | Individual responsibility | Required | Required | Required | Required | Required | Conditional |

## 8. Composition Rules

| ID | Rule |
|---|---|
| KA-CR-001 | A Knowledge Unit SHALL belong to one authoritative Knowledge Family. |
| KA-CR-002 | Legal Form SHALL resolve before constitution-specific Legal Structure is considered complete. |
| KA-CR-003 | A relationship SHALL reference separately established subjects and SHALL NOT duplicate their identity. |
| KA-CR-004 | Not Applicable SHALL be semantically distinct from Missing. |
| KA-CR-005 | Taxonomy specialisations SHALL NOT alter the meaning of their parent Knowledge Unit. |
| KA-CR-006 | Unsupported legal or business meaning SHALL NOT be inferred. |

## 9. Knowledge Invariants

| ID | Invariant |
|---|---|
| KA-INV-001 | Enterprise Identity, Legal Constitution and Legal Structure remain distinct. |
| KA-INV-002 | Legal Form is represented exactly once for an established semantic state. |
| KA-INV-003 | Structural roles are represented as relationships. |
| KA-INV-004 | Ownership, Control and Beneficial Ownership are excluded. |
| KA-INV-005 | Evidence provenance does not become Enterprise knowledge. |
| KA-INV-006 | Applicability is determined from governed semantic meaning. |

## 10. Boundaries and Deferred Concepts

| Concept | Disposition |
|---|---|
| Ownership Structure | Future Semantic Object |
| Beneficial Ownership | Assessment Architecture / future package |
| Control conclusion | Assessment Architecture |
| Business Operating Model | EA‑T02 |
| Corporation Sole | Deferred pending sufficient evidence and taxonomy decision |
| Government Identifier | Excluded pending precise semantic definition |

## 11. Downstream Use

| Consumer | Permitted use |
|---|---|
| EA‑T01 Information Contract | Select participation and completeness obligations by Knowledge Unit identifier. |
| EA‑T01 Transformation Specification | Execute rules over applicable Knowledge Units without redefining them. |
| EA‑T01 Canonical Output Specification | Reference Knowledge Units forming Enterprise Subject. |
| Information Acquisition Pattern | Define acquisition options for required Knowledge Units. |

## 12. Conformance

A conforming dependent artefact SHALL use the identifiers, definitions, semantic types, taxonomies and applicability rules in this specification without duplication or variation.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
