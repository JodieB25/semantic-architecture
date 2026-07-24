---
id: SA-COS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Canonical Output Standard

## 1. Purpose

This standard defines how a package specifies the canonical semantic object produced by successful semantic compilation.

## 2. Authority

The Canonical Output Specification owns output composition, output validity, output invariants, exposed lineage, semantic state and the downstream reliance contract. It does not redefine package meaning, knowledge or transformation rules.

## 3. Required sections

| Section | Responsibility |
|---|---|
| Output identity | Names and identifies the canonical output. |
| Composition | References authoritative semantic and knowledge components. |
| Validity | Defines conditions under which the output is canonical. |
| Invariants | Defines conditions preserved by every valid output. |
| Lineage | Exposes source-to-output lineage. |
| Reliance contract | States what downstream consumers may and may not infer. |
| Boundary | Excludes storage, API, serialization and implementation concerns. |

## 4. Requirements

| ID | Requirement |
|---|---|
| CO-P-001 | Canonical composition SHALL use authoritative package references. |
| CO-P-002 | A canonical output SHALL expose its semantic state and lineage. |
| CO-P-003 | Only applicable governed knowledge SHALL be represented. |
| CO-P-004 | The reliance contract SHALL not imply downstream or assessment meaning. |

## 5. Conformance

A Canonical Output Specification conforms when output validity, invariants and downstream reliance can be evaluated without redefining upstream semantic concepts.
