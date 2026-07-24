---
id: EA-T01-RP
package: EA-T01
document: Reference Prototype
version: 1.0.0
status: Informative
---

# EA-T01 — Reference Prototype

> This document is informative. It demonstrates one implementation-neutral expression of the normative specifications and creates no new semantic authority.

## 1. Prototype pipeline

```text
Input assertions and observations
        ↓
EA-T01 Information Acquisition Pattern
        ↓
Contract-ready governed information
        ↓
EA-T01 Information Contract
        ↓
EA-T01 Transformation Specification
        ↓
Canonical Enterprise Subject
```

## 2. Illustrative branch selection

| Established Legal Form | Applicable acquisition branch |
|---|---|
| Body Corporate | Acquire applicable body-corporate identifiers and structural relationships. |
| Trust | Acquire Trustee Relationships and applicable governing knowledge. |
| Partnership | Acquire Partner Relationships and applicable governing knowledge. |
| Sole Trader | Preserve individual–Enterprise identity continuity and avoid artificial self-relationships. |

## 3. Illustrative pseudo-contract

```yaml
enterprise_identity:
  names: established
  identifiers: resolved_by_applicability
  existence: established
legal_constitution:
  legal_form: established
legal_structure:
  applicable_branch: resolved
  governing_powers: established
  structural_relationships: established
  governing_responsibility: established
contract_state: complete
```

## 4. Non-normative implementation options

The normative package may be realised using guided forms, APIs, registry integrations, document extraction, human review or mixed acquisition channels. These options do not alter package semantics.

## 5. Cross-references

- [Package index](README.md)
- [Information Acquisition Pattern](05-information-acquisition-pattern.md)
- [Transformation Specification](06-transformation-specification.md)
- [Canonical Output Specification](07-canonical-output-specification.md)
