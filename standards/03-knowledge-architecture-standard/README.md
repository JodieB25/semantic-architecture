---
id: SA-KAS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Knowledge Architecture Standard

## 1. Purpose

This standard defines how governed knowledge for a Semantic Object is modelled and published.

## 2. Authority

The Knowledge Architecture is the sole package authority for Knowledge Families, Knowledge Units, semantic types, taxonomies, relationships, applicability and knowledge invariants.

## 3. Required structures

| Structure | Requirement |
|---|---|
| Knowledge Family register | Groups knowledge by coherent semantic responsibility. |
| Knowledge Unit register | Provides stable identifiers, names, definitions and semantic types. |
| Semantic type system | Defines the permitted types used by Knowledge Units. |
| Taxonomies | Defines governed specialisations without duplicating Knowledge Units. |
| Relationship model | Represents legally or semantically meaningful relationships. |
| Applicability rules | Determines which knowledge applies under governed conditions. |
| Composition rules | Defines permitted knowledge composition. |
| Invariants | Defines conditions that must remain true. |
| Deferred concepts | Records unresolved or excluded candidate concepts. |

## 4. Principles

| ID | Requirement |
|---|---|
| KA-P-001 | Knowledge definitions SHALL have stable identifiers. |
| KA-P-002 | Applicability SHALL be semantic and implementation independent. |
| KA-P-003 | Relationships SHALL be modelled as relationships where the meaning is relational. |
| KA-P-004 | Assessment conclusions SHALL NOT be represented as factual Knowledge Units. |
| KA-P-005 | Taxonomies SHALL specialise governed concepts without introducing ungoverned meaning. |

## 5. Conformance

A Knowledge Architecture conforms when all package knowledge used by contracts, acquisition rules, transformations and canonical outputs resolves to an authoritative governed definition.
