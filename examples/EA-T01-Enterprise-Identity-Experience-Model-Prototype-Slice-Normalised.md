---
id: EA-T01-EIEM-PROTOTYPE
package: EA-T01
name: Enterprise Identity Experience Model — Prototype Slice
document: Experience Model
version: 0.1.0
status: Informative Prototype Slice
authority: Informative Projection
governing_standard: SA-EMS v1.1.0-rc1
---

# EA-T01 — Enterprise Identity Experience Model — Prototype Slice

## 1. Prototype Objective

Demonstrate that a user can identify an enterprise, confirm its legal form, review the system's understanding, and produce a canonical Enterprise Subject suitable for EA-T02.

| Perspective | Prototype outcome |
|---|---|
| Enterprise | The system has correctly identified our business and legal form. |
| Product | One coherent journey from enterprise lookup to confirmation. |
| UX | A recognisable, low-friction identity flow with progressive disclosure. |
| Engineering | Deterministic construction of one confirmed canonical Enterprise Subject. |

## 2. Transformation Boundary

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | Governed enterprise identity facts, declarations and evidence; no upstream Semantic Object |
| **End State** | Confirmed canonical Enterprise Subject available to EA-T02 |

## 3. Prototype Boundary

| Included | Deferred |
|---|---|
| Enterprise search or manual identification | Full legal-structure branching |
| Legal name and primary identifier | All identifier types and jurisdictions |
| One governed legal-form selection | Complex governing powers and relationships |
| Basic existence/status confirmation | Unsupported-branch governance workflow |
| Enterprise-readable review | Full source corroboration and assurance states |
| Confirmation and EA-T02 handover | Production exception management |

## 4. Starting Context

| Starting element | Source | Enterprise action required |
|---|---|---|
| Enterprise identity facts | Enterprise authority | Search, select or enter |
| Legal-form options | EA-T01 semantic authority | Select one governed value |
| Existing source evidence | Authoritative source where available | Confirm or correct |

## 5. End-to-End Journey

| Stage | Enterprise Experience | System Behaviour | Compiler Behaviour | Exit Condition |
|---:|---|---|---|---|
| 1 | Understand why the business must be identified | Explain the purpose and downstream dependency | Initialise EA-T01 candidate state | User starts |
| 2 | Find or enter the business | Search by legal name or primary identifier; allow manual fallback | Create or update candidate Enterprise | Candidate created |
| 3 | Confirm core identity | Show legal name, identifier and status | Validate candidate identity | Identity confirmed |
| 4 | Confirm legal form | Present a controlled legal-form list | Establish one governed legal-form value | Legal form selected |
| 5 | Review understanding | Present a plain-language enterprise summary | Recompose current canonical meaning | User accepts or edits |
| 6 | Confirm and continue | Confirm establishment and explain next stage | Construct canonical Enterprise Subject and publish handover | EA-T02 can commence |

## 6. Experience Principles

| Principle | Requirement |
|---|---|
| Recognition before detail | Begin with recognisable enterprise information. |
| Controlled selection | Legal form is selected from a governed list. |
| Enterprise confirmation | Confirm a plain-language recomposition. |
| Correction through facts | Corrections occur in source identity facts. |
| Compiler ownership | Canonical Enterprise construction remains compiler-owned. |

## 7. Enterprise Interaction

| Interaction | Required behaviour |
|---|---|
| Search result selected | Create or update candidate Enterprise |
| Identity detail changed | Revalidate candidate identity |
| Legal form selected | Store one governed value |
| Required information complete | Enable review |
| Summary confirmed | Construct canonical Enterprise Subject |
| Information changed after confirmation | Invalidate confirmation and recompose |

## 8. Compiler Behaviour

| Trigger | Compiler behaviour | Visible consequence |
|---|---|---|
| Candidate selected | Resolve candidate Enterprise identity | Identity details displayed |
| Legal form established | Attach governed legal-form state | Review summary updated |
| Facts changed | Invalidate dependent state | Review returns to unresolved or ready state |
| Confirmation received | Compile canonical Enterprise Subject | Handover enabled |

## 9. Canonical Output

| Canonical element | Minimum guarantee |
|---|---|
| Enterprise identity | One enterprise uniquely identified or explicitly entered |
| Legal form | One governed legal form |
| Status | Existence/status recorded |
| Confirmation | Enterprise accepted the recomposed meaning |
| Lineage | Canonical state traces to source facts and confirmation |

## 10. State Model

| Enterprise-facing state | System state |
|---|---|
| Not started | No candidate Enterprise |
| In progress | Candidate exists; required information incomplete |
| Needs attention | Missing, contradictory or unresolved information |
| Ready to review | Required prototype information established |
| Confirmed | Canonical Enterprise Subject constructed |

## 11. Product/UX Latitude

| May vary | Must remain invariant |
|---|---|
| Page, wizard, conversation or panel layout | Controlled identity and legal-form acquisition |
| Visual hierarchy and wording | Plain-language review before confirmation |
| Search interaction | Canonical conclusion remains compiler-owned |
| Progress treatment | Deterministic invalidation after corrections |

## 12. Acceptance Criteria

| ID | Criterion |
|---|---|
| P-AC-001 | A user can complete the journey without semantic terminology. |
| P-AC-002 | The journey begins with enterprise identification. |
| P-AC-003 | Legal form is selected from a controlled list. |
| P-AC-004 | The review is a plain-language recomposition. |
| P-AC-005 | Editing identity information updates the review deterministically. |
| P-AC-006 | Confirmation produces one canonical Enterprise Subject. |
| P-AC-007 | No service, Reporting Entity, risk or AML/CTF conclusion is produced. |
| P-AC-008 | The output can be handed directly to EA-T02. |

## 13. Source Alignment

| Prototype concern | EA-T01 source authority |
|---|---|
| Enterprise identity and legal form | Semantic Object and Semantic Specification |
| Canonical values and applicability | Knowledge Architecture |
| Required information and completeness | Information Contract / Semantic Assertion Contract |
| Acquisition sequence | Information Acquisition Pattern / Semantic Input Pattern |
| Canonical construction | Transformation / Semantic Compilation Specification |
| Handover output | Canonical Output / Canonical Semantic Model |

## 14. Downstream Handover

| Property | Value |
|---|---|
| Consumer | EA-T02 Business Operating Model |
| Guarantee | Confirmed canonical Enterprise Subject |
| Transition | We now understand who your business is. Next, we will understand the services your business performs. |

## 15. Completion Boundary

The slice is complete when an unidentified enterprise becomes one confirmed canonical Enterprise Subject and can be handed to EA-T02.
