# EA-T01–EA-T04 Experience Model Consistency Review

## Overall Determination

**PARTIALLY CONSISTENT — NORMALISATION REQUIRED**

The four source Experience Models follow the same architectural direction and preserve the same core principles: upstream reuse, progressive disclosure, enterprise confirmation, compiler-owned canonical conclusions, explainability and downstream handover.

They were not structurally consistent before normalisation.

## Source Comparison

| Area | EA-T01 | EA-T02 | EA-T03 | EA-T04 | Finding |
|---|---|---|---|---|---|
| Prototype objective | Present | Present | Present as “What This Prototype Proves” | Present | Consistent in substance; headings differed |
| Explicit start/end state | Implicit | Implicit | Implicit | Implicit | Missing across all four |
| Scope boundary | Detailed | Detailed | Partial | Minimal | Inconsistent completeness |
| Starting context | Partial | Detailed | Detailed | Implicit | EA-T04 required expansion |
| Journey | Table | Detailed table | Table | Numbered list | EA-T04 structurally inconsistent |
| Compiler behaviour | Trigger table | Trigger table | Trigger table | Bullets | EA-T04 structurally inconsistent |
| Canonical output | Handover guarantees | Detailed table | Implied | Bullets | Inconsistent presentation |
| State model | Present | Present | Missing | Missing | EA-T03 and EA-T04 required bounded state models |
| UX latitude | Implicit | Explicit | Brief prose | Missing | Required normalisation |
| Acceptance criteria | Detailed | Detailed | Table | Missing | EA-T04 required explicit criteria |
| Source alignment | Present | Present | Missing | Missing | EA-T03 and EA-T04 required alignment tables |
| Handover | Detailed | Detailed | Present | One line | EA-T04 required expansion |

## Semantic Findings

| ID | Finding | Classification | Treatment |
|---|---|---|---|
| EM-F-001 | EA-T01 uses “Canonical Enterprise Subject”, while some compiler material uses “Canonical Enterprise Model”. | Terminology alignment | Preserved the Experience Model term and flagged for package-level canonical naming review. |
| EM-F-002 | EA-T03 intentionally acquires no new enterprise facts in the prototype slice. | Valid package-specific behaviour | Preserved and made explicit in Starting Context. |
| EM-F-003 | EA-T04 includes “Business Groups” in the journey, while its listed canonical outputs focus on Reporting Groups and related objects. | Presentation ambiguity | Treated Business Group as contextual review, not a separate canonical output. |
| EM-F-004 | EA-T04 source is a skeletal prototype slice and does not evidence all detailed interaction rules. | Completeness limitation | Expanded only from the supplied EA-T04 journey, compiler behaviour and canonical output; no new semantic authority introduced. |

## Normalisation Result

| Requirement | Result |
|---|:---:|
| Common section order | PASS |
| Table-led transformation boundary | PASS |
| Table-led journey | PASS |
| Table-led compiler behaviour | PASS |
| Table-led canonical output | PASS |
| Table-led state model | PASS |
| Table-led acceptance criteria | PASS |
| Explicit downstream handover | PASS |
| Prototype status preserved | PASS |
| No new semantic authority introduced | PASS |

## Release Note

The normalised documents are suitable as coherent prototype handover artefacts. They remain informative prototype slices. The terminology issue in EM-F-001 should be resolved against the canonical EA-T01 package before any normative production release.
