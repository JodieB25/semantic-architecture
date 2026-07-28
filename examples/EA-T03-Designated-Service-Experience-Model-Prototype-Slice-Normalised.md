---
id: EA-T03-EM-PS
package: EA-T03
name: Designated Service Experience Model — Prototype Slice
document: Experience Model
version: 0.1.0
status: Informative Prototype Slice
authority: Informative Projection
governing_standard: SA-EMS v1.1.0-rc1
---

# EA-T03 — Designated Service Experience Model — Prototype Slice

## 1. Prototype Objective

Demonstrate that the confirmed EA-T02 service profile can be evaluated against recovered legislative knowledge without repeated acquisition and compiled into a Canonical Enterprise Designated Service Model for EA-T04.

| Perspective | Prototype outcome |
|---|---|
| Enterprise | The enterprise can understand which regulated services apply and why. |
| Product | The EA-T02 profile is reused without a repeated questionnaire. |
| UX | Conclusions are clear, explainable and correctable through upstream facts. |
| Engineering | Identical source models and legislative versions produce identical determinations. |

## 2. Transformation Boundary

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | Confirmed EA-T02 Canonical Enterprise Service Model plus applicable EA-T03 legislative knowledge |
| **End State** | Canonical Enterprise Designated Service Model available to EA-T04 |

## 3. Prototype Boundary

| Included | Deferred |
|---|---|
| Reuse of EA-T01 and EA-T02 canonical state | Reacquisition of enterprise or service facts |
| Evaluation of bounded Designated Service definitions | Exhaustive service catalogue |
| Applicable, Not Applicable and Unresolved results | Production assurance workflows |
| Explainability and lineage | Full regulatory reporting interface |
| EA-T04 handover | Reporting Entity determination |

## 4. Starting Context

| Input | Source | Enterprise action required |
|---|---|---|
| Enterprise identity | EA-T01 | None |
| Enterprise Service Model | EA-T02 | Review only |
| Designated Service definitions and exclusions | EA-T03 regulatory knowledge | None |

No new enterprise facts are acquired in this prototype slice.

## 5. End-to-End Journey

| Stage | Enterprise Experience | System Behaviour | Compiler Behaviour | Exit Condition |
|---:|---|---|---|---|
| 1 | Review the existing service profile | Show the relevant service summary | Load the EA-T02 canonical model | Profile loaded |
| 2 | Observe regulated-service evaluation | Show progress without repeated questions | Evaluate candidate definitions, qualifications and exclusions | Evaluation complete |
| 3 | Review results | Present Applicable, Not Applicable and Unresolved conclusions | Publish determinations | Results available |
| 4 | Inspect reasoning | Show linked service, conditions, exclusions and source | Expose lineage | Explanation understood |
| 5 | Continue | Explain that Reporting Entity status is next | Publish the canonical model to EA-T04 | EA-T04 can commence |

## 6. Experience Principles

| Principle | Requirement |
|---|---|
| No repeated acquisition | Reuse established upstream facts. |
| Regulatory knowledge remains external | The enterprise does not select legal conclusions. |
| Explainability | Every result links to service facts and legislative knowledge. |
| Correct correction path | Service corrections return to EA-T02. |
| Compiler ownership | Designated Service determinations remain compiler-owned. |

## 7. Enterprise Interaction

| Result or question | Enterprise-facing treatment | Correction path |
|---|---|---|
| Applicable | This regulated service applies to the established service profile. | Inspect reasoning or correct EA-T02 facts |
| Not Applicable | The definition was evaluated and does not apply. | Inspect failed condition or exclusion |
| Unresolved | A required upstream detail is unresolved. | Return to the exact EA-T02 requirement |

## 8. Compiler Behaviour

| Trigger | Compiler behaviour | Visible consequence |
|---|---|---|
| EA-T02 model loaded | Select candidate definitions | Evaluation scope displayed |
| Evaluation started | Evaluate elements, qualifications and exclusions | Progress visible |
| Evaluation completed | Persist determinations and lineage | Results displayed |
| Source service changed | Invalidate and re-evaluate dependencies | Results update deterministically |
| Explanation opened | Return source-service and legislative trace | Detailed reasoning shown |
| Continue selected | Publish canonical model to EA-T04 | Handover enabled |

## 9. Canonical Output

| Canonical element | Minimum guarantee |
|---|---|
| Applicable Designated Services | Established and linked to source services |
| Non-applicable determinations | Failed condition or exclusion retained |
| Unresolved determinations | Exact missing upstream requirement retained |
| Legislative references | Authoritative definition and source reference preserved |
| Canonical lineage | Service, rule, evaluation and determination trace preserved |

## 10. State Model

| Enterprise-facing state | System state |
|---|---|
| Ready to evaluate | EA-T02 model and legislative version loaded |
| Evaluating | Determinations in progress |
| Needs attention | One or more determinations unresolved |
| Results available | Determinations published |
| Explained | Selected result lineage exposed |
| Compiled | Canonical model available to EA-T04 |

## 11. Product/UX Latitude

| May vary | Must remain invariant |
|---|---|
| Cards, tables or progressive disclosure | Result meanings and correction paths |
| Visual progress treatment | No repeated acquisition |
| Explanation depth and reveal pattern | Complete lineage remains available |
| Wording refinements | Legal conclusions remain compiler-owned |

## 12. Acceptance Criteria

| ID | Criterion |
|---|---|
| P-AC-001 | The enterprise is not asked to re-enter EA-T02 facts. |
| P-AC-002 | Identical source models and legislative versions produce identical results. |
| P-AC-003 | A non-specialist can understand each determination. |
| P-AC-004 | Detailed lineage is available without dominating the primary experience. |
| P-AC-005 | Corrections occur in EA-T02 rather than by editing legal conclusions. |
| P-AC-006 | The canonical model is available to EA-T04. |

## 13. Source Alignment

| Prototype concern | EA-T03 source authority |
|---|---|
| Service facts | EA-T02 Canonical Enterprise Service Model |
| Legislative definitions and exclusions | EA-T03 Knowledge Architecture |
| Required conclusions | EA-T03 Semantic Assertion Contract |
| Evaluation behaviour | EA-T03 Semantic Evaluation Specification |
| Canonical construction | EA-T03 Semantic Compilation Specification |
| Handover output | EA-T03 Canonical Semantic Model |

## 14. Downstream Handover

| Property | Value |
|---|---|
| Consumer | EA-T04 Reporting Entity |
| Guarantee | Canonical Enterprise Designated Service Model with determinations and lineage |
| Transition | We now understand which regulated services apply. Next, we will determine Reporting Entity status. |

## 15. Completion Boundary

The slice is complete when the enterprise can understand applicable, non-applicable and unresolved Designated Service determinations, inspect their reasoning, and continue to EA-T04.
