---
id: EA-T04-EM-PS
package: EA-T04
name: Reporting Entity Experience Model — Prototype Slice
document: Experience Model
version: 0.1.0
status: Informative Prototype Slice
authority: Informative Projection
governing_standard: SA-EMS v1.1.0-rc1
---

# EA-T04 — Reporting Entity Experience Model — Prototype Slice

## 1. Prototype Objective

Demonstrate the transition from a confirmed EA-T03 Designated Service Model to a confirmed Canonical Reporting Entity Model suitable for EA-T05.

| Perspective | Prototype outcome |
|---|---|
| Enterprise | The enterprise can understand and confirm its Reporting Entity state and related legislative structures. |
| Product | One coherent journey establishes the regulatory perimeter. |
| UX | Legislative conclusions are presented in enterprise-readable form with progressive explanation. |
| Engineering | EA-T03 state and minimum EA-T04 facts compile deterministically into the canonical model. |

## 2. Transformation Boundary

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | Confirmed EA-T03 Canonical Enterprise Designated Service Model plus required Legislative Person and group facts |
| **End State** | Confirmed Canonical Reporting Entity Model available to EA-T05 |

## 3. Prototype Boundary

| Included | Deferred |
|---|---|
| Review of EA-T03 output | Reassessment of Designated Services |
| Legislative Person confirmation | Exhaustive legislative-person branches |
| Reporting Entity establishment | Full production exception and assurance workflow |
| Reporting Group, membership and Lead Entity review where applicable | All complex group lifecycle events |
| Responsibility attribution and lineage | Downstream governance assessment |
| EA-T05 handover | AML/CTF Program design |

## 4. Starting Context

| Starting element | Source | Enterprise action required |
|---|---|---|
| Enterprise identity | EA-T01 | Review only |
| Enterprise Service Model | EA-T02 | None |
| Designated Service Model | EA-T03 | Review only |
| Legislative Person facts | Enterprise authority | Confirm or complete minimum facts |
| Group and Lead Entity facts | Enterprise authority where applicable | Confirm or complete minimum facts |

## 5. End-to-End Journey

| Stage | Enterprise Experience | System Behaviour | Compiler Behaviour | Exit Condition |
|---:|---|---|---|---|
| 1 | Review the EA-T03 result | Show applicable Designated Services and relevant lineage | Load the EA-T03 canonical model | Upstream state loaded |
| 2 | Confirm the Legislative Person | Present the minimum identity facts required | Resolve Legislative Person | Legislative Person established |
| 3 | Review Reporting Entity status | Present the determination and establishment pathway | Establish Reporting Entity | Status available |
| 4 | Review relevant group context | Present Business Group context where relevant | Compile applicable group context | Context resolved |
| 5 | Review Reporting Groups | Present established Reporting Groups and basis | Compile Reporting Groups | Groups established or not applicable |
| 6 | Review memberships | Present membership relationships and effective state | Compile Reporting Group Memberships | Memberships resolved |
| 7 | Confirm Lead Entity where applicable | Present effective Lead Entity and period | Compile Lead Entity | Lead Entity resolved or not applicable |
| 8 | Review responsibility attribution | Present attributed statutory responsibility | Compile Responsibility Attribution | Attribution established |
| 9 | Review system understanding | Recompose the complete Reporting Entity state | Compile continuity and canonical lineage | Ready to confirm |
| 10 | Confirm and continue | Confirm the enterprise-readable model | Publish Canonical Reporting Entity Model | EA-T05 can commence |

## 6. Experience Principles

| Principle | Requirement |
|---|---|
| Upstream reuse | Do not reacquire EA-T01–EA-T03 state. |
| Minimum fact acquisition | Ask only for EA-T04 facts required by the active branch. |
| Enterprise confirmation | Confirm the recomposed Reporting Entity state. |
| Compiler ownership | Legislative conclusions remain compiler-owned. |
| Explainability | Establishment pathways and lineage remain inspectable. |

## 7. Enterprise Interaction

| Interaction | Required consequence |
|---|---|
| EA-T03 result reviewed | Activate relevant EA-T04 branches |
| Legislative Person fact confirmed | Re-evaluate Reporting Entity establishment |
| Group fact changed | Invalidate affected group, membership and Lead Entity state |
| Responsibility fact changed | Recompile affected attribution state |
| Recomposition accepted | Permit canonical publication |
| Enterprise is unsure | Preserve unresolved state and prevent handover |

## 8. Compiler Behaviour

| Trigger | Compiler behaviour | Visible consequence |
|---|---|---|
| EA-T03 model loaded | Initialise Reporting Entity evaluation scope | Upstream summary displayed |
| Legislative Person resolved | Establish candidate Reporting Entity | Status and pathway displayed |
| Group context established | Compile Reporting Groups and memberships | Group structure displayed |
| Lead Entity facts sufficient | Compile effective Lead Entity | Lead Entity result displayed |
| Responsibility facts sufficient | Compile Responsibility Attribution | Responsibility summary displayed |
| Relevant fact changed | Invalidate dependent state and recompile | Summary updates deterministically |
| Confirmation received | Attach continuity and lineage; publish model | EA-T05 handover enabled |

## 9. Canonical Output

| Canonical element | Minimum guarantee |
|---|---|
| Legislative Person | One resolved legislative subject |
| Reporting Entity | Established status and pathway |
| Establishment Pathways | Every established pathway preserved |
| Reporting Groups | Applicable groups preserved |
| Reporting Group Membership | Effective memberships and displaced lineage preserved |
| Lead Entity | Effective Lead Entity and period where applicable |
| Responsibility Attribution | Effective statutory obligation attribution |
| Legislative Identity Continuity | Recognised continuity relationships preserved |
| Canonical Lineage | Assertion, traceability, temporal and upstream lineage preserved |

## 10. State Model

| Enterprise-facing state | System state |
|---|---|
| Ready to begin | EA-T03 model loaded |
| Confirming identity | Legislative Person facts incomplete |
| Evaluating | Reporting Entity and group branches active |
| Needs attention | Required fact or conclusion unresolved |
| Ready to review | Bounded canonical state complete |
| Confirmed | Enterprise accepted the recomposed state |
| Compiled | Canonical Reporting Entity Model published |

## 11. Product/UX Latitude

| May vary | Must remain invariant |
|---|---|
| Page, panel, graph or guided-review layout | Stage and dependency order |
| Group visualisation | Canonical identities and relationships |
| Explanation reveal pattern | Establishment pathways and lineage availability |
| Wording refinements | Legislative conclusions remain compiler-owned |

## 12. Acceptance Criteria

| ID | Criterion |
|---|---|
| P-AC-001 | The journey begins from the confirmed EA-T03 model. |
| P-AC-002 | The enterprise is not asked to redefine Designated Services. |
| P-AC-003 | Only minimum EA-T04 facts are acquired. |
| P-AC-004 | Reporting Entity and group conclusions remain compiler-owned. |
| P-AC-005 | Changes deterministically invalidate and recompile dependent state. |
| P-AC-006 | Establishment pathways and lineage are explainable. |
| P-AC-007 | Confirmation produces one Canonical Reporting Entity Model. |
| P-AC-008 | The model is suitable for direct handover to EA-T05. |

## 13. Source Alignment

| Prototype concern | EA-T04 source authority |
|---|---|
| Reporting Entity scope and boundaries | Semantic Object and Semantic Specification |
| Legislative Person, groups and canonical vocabulary | Knowledge Architecture |
| Required assertions and completeness | Semantic Assertion Contract |
| Required enterprise facts | Semantic Input Pattern |
| Establishment rules | Semantic Evaluation Specification |
| Canonical projection | Semantic Compilation Specification |
| Handover output | Canonical Semantic Model |

## 14. Downstream Handover

| Property | Value |
|---|---|
| Consumer | EA-T05 Enterprise Governance Assessment |
| Guarantee | Confirmed Canonical Reporting Entity Model with identity, group, responsibility and lineage state |
| Transition | We now understand the Reporting Entity and its regulatory perimeter. Next, we will assess its governance capability. |

## 15. Completion Boundary

The slice is complete when EA-T03 state and the minimum required EA-T04 facts have been transformed into one confirmed Canonical Reporting Entity Model suitable for EA-T05.
