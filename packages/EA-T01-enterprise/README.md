---
id: EA-T01
name: Enterprise
version: 1.0.0
status: Publication Candidate
---

# EA-T01 — Enterprise

## Canonical question

> What Enterprise exists?

## Hierarchical specification order

| Order | Artefact | Authority |
|---:|---|---|
| 1 | [Semantic Object](01-semantic-object.md) | Architectural responsibility and canonical question |
| 2 | [Semantic Specification](02-semantic-specification.md) | Enterprise meaning, grammar, composition, boundaries and invariants |
| 3 | [Knowledge Architecture](03-knowledge-architecture.md) | Knowledge Families, Knowledge Units, types, taxonomies, relationships and applicability |
| 4 | [Information Contract](04-information-contract.md) | Participation, conditionality, completeness and input lineage |
| 5 | [Information Acquisition Pattern](05-information-acquisition-pattern.md) | Progressive establishment of contract-ready information |
| 6 | [Transformation Specification](06-transformation-specification.md) | EA-T01-specific semantic compilation rules and guarantees |
| 7 | [Canonical Output Specification](07-canonical-output-specification.md) | Canonical Enterprise Subject and downstream reliance |
| 8 | [Reference Prototype](08-reference-prototype.md) | Informative implementation-neutral illustration |

## Derivation

```text
Semantic Object
      ↓
Semantic Specification
      ↓
Knowledge Architecture
      ↓
Information Contract
      ↓
Information Acquisition Pattern
      ↓
Transformation Specification
      ↓
Canonical Output Specification
      ↓
Reference Prototype (informative)
```

## Normalisation

The package follows the [Single Semantic Authority Principle](../../governance/single-semantic-authority.md). Semantic definitions are not repeated in downstream specifications.
