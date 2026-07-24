---
id: SA-SSS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Semantic Specification Standard

## 1. Purpose

This standard defines how the authoritative semantic meaning of a package is specified.

## 2. Authority

The Semantic Specification is the sole package authority for semantic meaning, grammar, composition, boundaries and semantic invariants. It does not own Knowledge Unit definitions or compiler execution.

## 3. Required sections

| Section | Responsibility |
|---|---|
| Canonical question | Restates the question owned by the Semantic Object. |
| Semantic responsibility | Defines what the package establishes. |
| Semantic grammar | Defines constituent semantic components. |
| Composition | Defines how components constitute the object. |
| Dependencies | Defines semantic dependencies between components. |
| Boundaries | Defines included and excluded meaning. |
| Invariants | Defines conditions that must always remain true. |
| Lineage | Links the specification to the Semantic Object and Knowledge Architecture. |

## 4. Normalisation rules

- Knowledge Units SHALL be referenced from the Knowledge Architecture.
- Input participation SHALL be referenced from the Information Contract.
- Acquisition behaviour SHALL be referenced from the Information Acquisition Pattern.
- Compiler behaviour SHALL be referenced from the Transformation Specification.
- Output validity SHALL be referenced from the Canonical Output Specification.

## 5. Conformance

A Semantic Specification conforms when it fully defines package meaning without importing implementation, assessment or downstream domain meaning.
