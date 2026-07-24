# Single Semantic Authority Principle

> Every semantic concept SHALL have exactly one authoritative definition. All dependent artefacts SHALL reference that definition and SHALL NOT reproduce, vary or extend its meaning.

## Authority allocation

| Artefact type | Owns | Does not own |
|---|---|---|
| Semantic Object | Architectural responsibility and canonical question | Detailed grammar or knowledge |
| Semantic Specification | Meaning, grammar, composition, boundaries and invariants | Knowledge Unit definitions or rule execution |
| Knowledge Architecture | Knowledge, types, taxonomies, relationships and applicability | Package meaning or implementation |
| Information Contract | Participation, conditionality and completeness | Knowledge definitions |
| Information Acquisition Pattern | Progressive establishment of information | Knowledge definitions or transformation |
| Transformation Specification | Package-specific compilation rules and guarantees | Generic compiler language or knowledge definitions |
| Canonical Output Specification | Output validity and reliance | Upstream definitions or transformation mechanics |
