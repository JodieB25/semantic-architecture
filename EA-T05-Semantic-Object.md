---
id: EA-T05
name: Enterprise Operating Context
document: Semantic Object
version: 1.0.0
status: Production Candidate
authority: Normative
package: Enterprise Architecture
governing_standard: Semantic Object Standard
---

# EA-T05 Semantic Object

# Document Identity

| Property | Value |
|---|---|
| Semantic Object | Enterprise Operating Context |
| Identifier | EA-T05 |
| Package | Enterprise Architecture |
| Authority | Normative |
| Status | Production Candidate |

# Purpose

The purpose of this Semantic Object is to establish the canonical Enterprise Operating Context for each exact Applicable Designated Service Operating Configuration performed by a Reporting Entity.

It establishes the complete operating-context semantic state required by downstream Semantic Objects while preserving semantic authority owned by EA‑T01 through EA‑T04.

# Canonical Question

> **What is the complete Enterprise Operating Context for this Applicable Designated Service Operating Configuration?**

# Semantic Subject

Enterprise Operating Context.

# Semantic Outcome

A canonical Enterprise Operating Context semantic state comprising:

- Applicable Designated Service Operating Configuration
- Delivery Means Characteristic
- Customer Kind
- Customer Relationship
- Service–Channel Relationship
- Geographic Connection Qualification
- Transaction Qualification
- Value Qualification
- Service–Arrangement Relationship
- Operating State Qualification
- Operating Scale Qualification
- Operating Change Qualification
- Conditional Operating Enrichment
- Applicability
- Canonical Semantic Lineage

# Scope

This Semantic Object includes:

- operating context qualification;
- operating characteristics;
- customer operating context;
- delivery channel participation;
- geographic operating context;
- transaction and value context;
- operating arrangements;
- operating state, scale and change;
- conditional enrichment; and
- canonical semantic lineage.

# Out of Scope

This Semantic Object excludes:

- Enterprise identity (EA‑T01);
- Business Operating Model (EA‑T02);
- Designated Service determination (EA‑T03);
- Reporting Entity determination (EA‑T04);
- Enterprise ML/TF Assessment (EA‑T06);
- Enterprise Understanding (EA‑T07);
- Enterprise Judgement (EA‑T08);
- Enterprise Response (EA‑T09);
- AML/CTF Program compilation (EA‑T10); and
- implementation schemas, workflows, interfaces and presentation formats.

# Upstream Dependencies

- EA‑T01 Enterprise
- EA‑T02 Business Operating Model
- EA‑T03 Designated Services
- EA‑T04 Reporting Entity

# Downstream Dependencies

- EA‑T06 Enterprise ML/TF Assessment
- EA‑T07 Enterprise Understanding
- EA‑T08 Enterprise Judgement
- EA‑T09 Enterprise Response
- EA‑T10 AML/CTF Program

# Semantic Authority

EA‑T05 is the sole semantic authority for Enterprise Operating Context.

No downstream Semantic Object may redefine:

- Enterprise Operating Context;
- operating-context composition;
- applicability;
- operating-context semantic relationships;
- operating-context semantic lineage.

# Canonical Output

The canonical output of this Semantic Object is the EA‑T05 Canonical Semantic Model, providing the authoritative Enterprise Operating Context consumed by downstream Semantic Objects.

# Standards Conformance

| Requirement | Result |
|---|:---:|
| Single Semantic Subject | PASS |
| Canonical Question | PASS |
| Explicit Scope | PASS |
| Explicit Boundaries | PASS |
| Upstream Dependencies | PASS |
| Downstream Dependencies | PASS |
| Single Semantic Authority | PASS |
| Canonical Semantic Output | PASS |
| Implementation Independence | PASS |

# Document Status

| Property | Value |
|---|---|
| Status | Production Candidate |
| Semantic Object Standard | Compliant |
| EA‑T04 Reference Implementation | Structurally Aligned |
| Ready for Semantic Specification | Yes |
| Ready for Publication Freeze | Yes |
