---
id: SA-ICS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Information Contract Standard

## 1. Purpose

This standard defines how a package specifies the governed information that must participate in semantic compilation.

## 2. Authority

The Information Contract owns participation, conditionality, dependencies, completeness and input lineage. It references, but does not redefine, package knowledge.

## 3. Participation states

| State | Meaning |
|---|---|
| Required | Must be established for the applicable branch. |
| Conditional | Becomes Required when its governed condition is met. |
| Optional | May participate but does not determine completeness. |
| Not Applicable | Excluded from the resolved semantic branch and from completeness. |

## 4. Required sections

- Contract principles.
- Core participation contract.
- Branch or applicability contract.
- Progressive resolution model.
- Completeness rules.
- Input dependencies and lineage.
- Conformance requirements.

## 5. Requirements

| ID | Requirement |
|---|---|
| IC-P-001 | Contracts SHALL reference governed Knowledge Unit or Knowledge Family identifiers. |
| IC-P-002 | Not Applicable SHALL NOT be treated as Missing. |
| IC-P-003 | Completeness SHALL evaluate only the applicable information set. |
| IC-P-004 | Contracts SHALL remain independent of acquisition channel and implementation. |

## 6. Conformance

A contract conforms when a deterministic applicable information set and completeness result can be established without redefining semantic knowledge.
