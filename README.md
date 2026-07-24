---
title: Semantic Architecture Repository
version: 1.0.0
status: Publication Candidate
---

# Semantic Architecture

Semantic Architecture defines a governed method for recovering semantic objects, expressing their knowledge architecture, acquiring required information, compiling governed knowledge, and producing canonical semantic outputs.

## Repository hierarchy

```text
semantic-architecture-v1.0/
├── README.md
├── standards/
│   ├── README.md
│   ├── 01-semantic-object-standard/
│   ├── 02-semantic-specification-standard/
│   ├── 03-knowledge-architecture-standard/
│   ├── 04-information-contract-standard/
│   ├── 05-semantic-acquisition-standard/
│   ├── 06-semantic-compilation-standard/
│   └── 07-canonical-output-standard/
├── packages/
│   ├── README.md
│   └── EA-T01-enterprise/
├── governance/
├── glossary/
└── examples/
```

## Normative hierarchy

1. Repository governance establishes publication and authority rules.
2. Reusable standards define the required structure and behaviour of specification types.
3. Package specifications instantiate those standards for a semantic object.
4. Informative examples and prototypes demonstrate possible realisations without changing normative meaning.

## Single Semantic Authority Principle

> Every semantic concept has one authoritative definition. Dependent artefacts reference that authority and do not reproduce or vary its meaning.

## Standards

| Order | Standard | Responsibility |
|---:|---|---|
| 1 | [Semantic Object Standard](standards/01-semantic-object-standard/README.md) | Defines the architectural responsibility and canonical question of a semantic object. |
| 2 | [Semantic Specification Standard](standards/02-semantic-specification-standard/README.md) | Defines semantic meaning, grammar, composition, boundaries and invariants. |
| 3 | [Knowledge Architecture Standard](standards/03-knowledge-architecture-standard/README.md) | Defines governed knowledge, types, taxonomies, relationships and applicability. |
| 4 | [Information Contract Standard](standards/04-information-contract-standard/README.md) | Defines participation, conditionality and completeness of transformation inputs. |
| 5 | [Semantic Acquisition Standard](standards/05-semantic-acquisition-standard/README.md) | Defines progressive establishment of information required by a contract. |
| 6 | [Semantic Compilation Standard](standards/06-semantic-compilation-standard/README.md) | Defines compiler phases, rules, states and guarantees. |
| 7 | [Canonical Output Standard](standards/07-canonical-output-standard/README.md) | Defines canonical output validity and downstream reliance. |

## Reference package

[EA-T01 Enterprise](packages/EA-T01-enterprise/README.md) is the first complete package implementation.

## Status labels

- **Normative**: requirements governing conformance.
- **Informative**: explanatory or illustrative material.
- **Publication Candidate**: suitable for review before formal release.
