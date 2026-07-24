---
id: EA-T01-SO
package: EA-T01
name: Enterprise
document: Semantic Object
version: 2.1.0
status: Frozen
authority: Normative
---

# Semantic Object — Enterprise

## 1. Catalogue Entry

| Property | Value |
|---|---|
| Canonical question | **What Enterprise exists?** |
| Semantic output | Enterprise Subject |
| Architectural role | Root Semantic Object in the Enterprise domain |
| Upstream dependency | None |

## 2. Responsibility

Enterprise SHALL establish an Enterprise Subject. Its meaning, composition and invariants are defined exclusively by **EA‑T01 Semantic Specification**.

## 3. High-level Boundary

| Included responsibility | Excluded responsibility |
|---|---|
| Establish Enterprise Subject | Ownership and Control |
| Preserve Enterprise identity | Business Operating Model |
| Establish legal constitution and structure | Reporting Entity status |
| Provide a downstream semantic subject | Assessment conclusions, Governance and AML/CTF Program |

## 4. Semantic Grammar Reference

The authoritative grammar is **EA‑T01-SS §7**. The Semantic Object records only its high-level components:

```text
Enterprise
├── Enterprise Identity
├── Legal Constitution
└── Legal Structure
```

## 5. Downstream Relationships

| Consumer | Relationship |
|---|---|
| EA‑T02 Business Operating Model | Consumes Enterprise Subject |
| Ownership package (future) | Consumes Enterprise Subject |

## 6. Conformance

A catalogue representation conforms when it preserves the canonical question, architectural responsibility, high-level boundary and output without redefining semantic composition or governed knowledge.


## Repository cross-references

- [Package index](README.md)
- [Applicable reusable standards](../../standards/README.md)
- [Authority and normalisation rules](../../governance/single-semantic-authority.md)
