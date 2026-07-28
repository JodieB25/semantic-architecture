---
id: EA-T02-ESEM-PROTOTYPE
package: EA-T02
name: Enterprise Service Experience Model — Prototype Slice
document: Experience Model
version: 0.1.0
status: Informative Prototype Slice
authority: Informative Projection
governing_standard: SA-EMS v1.1.0-rc1
source_repository: Semantic Architecture Reference Repository v1.0.0-RC1
source_package: EA-T02 Enterprise Service Model
audience:
  - Product
  - UX Design
  - Engineering
prototype_pathways:
  - Conveyancing Practice
  - Real Estate Agency
---

# EA-T02 — Enterprise Service Experience Model

## First Working End-to-End Prototype Slice

> This document defines the minimum enterprise journey required to demonstrate EA-T02 end to end for two representative business types: a conveyancing practice and a real estate agency. It does not prescribe a particular interface, page structure, component library or implementation technology, and it introduces no new semantic authority.

## 1. Prototype Objective

Demonstrate that a confirmed EA-T01 Enterprise can select one of two recognisable business pathways, identify the services it performs through controlled choices, provide the minimum contextual facts needed for deterministic semantic evaluation, review the system's plain-language understanding, and produce a canonical Enterprise Service Model suitable for handover to EA-T03.

| Perspective | Prototype outcome |
|---|---|
| Enterprise | “The system has accurately understood the services our business performs.” |
| Product | One reusable journey supports two materially different business types without redesigning the semantic process. |
| UX | The enterprise recognises its business, receives only relevant choices and confirms a coherent service description. |
| Engineering | Controlled selections compile deterministically into facts, assertions, compositions and a canonical Enterprise Service Model. |

## 2. Transformation Boundary

| Transformation Boundary | Canonical State |
|---|---|
| **Start State** | Confirmed EA-T01 canonical Enterprise Subject |
| **End State** | Confirmed Canonical Enterprise Service Model available to EA-T03 |

## 3. Prototype Boundary

| Included in the first prototype | Deferred |
|---|---|
| Confirmed EA-T01 Enterprise as the starting context | Enterprise identity creation or correction |
| Two business pathways: conveyancing and real estate agency | All other service families |
| Controlled, multi-select service discovery | Free-text service discovery |
| Contextual service-detail selections | Full production fact catalogue |
| Relevant exclusion and qualification checks | Exhaustive legislative exclusions |
| One or more candidate service arrangements | Complex cross-enterprise arrangements |
| One or more Service Conduct Compositions | Full portfolio-scale composition management |
| Plain-language review and confirmation | Full assurance and governance workflow |
| Technical detail available for inspection | Production-grade trace visualisation |
| Canonical EA-T02 output and EA-T03 handover | Designated Service conclusions |

## 5. End-to-End Journey

| Stage | Enterprise Experience | System Behaviour | Compiler Behaviour | Exit Condition |
|---:|---|---|---|---|
| 1 | Recognise the confirmed business | Present EA-T01 identity and explain the purpose of this stage | Load the canonical Enterprise Subject | Enterprise starts |
| 2 | Choose the business pathway that best reflects the enterprise | Offer the two prototype pathways without implying a legal classification | Activate the relevant acquisition scope | At least one pathway selected |
| 3 | Identify the services the business performs | Present controlled, business-recognisable service descriptions | Activate candidate fact requirements and composition branches | At least one service selected |
| 4 | Describe how each selected service operates | Present only the contextual selections required for the chosen service | Establish Enterprise Facts and evaluate applicability | Required prototype facts resolved |
| 5 | Check relevant exclusions or limiting conditions | Present only exclusions associated with the active branch | Exclude, narrow or retain candidate semantic branches | Applicable exclusions resolved |
| 6 | Review the system's understanding | Recompose the emerging service model into coherent business language | Evaluate assertions and assemble Service Conduct Compositions | Enterprise accepts or edits |
| 7 | Confirm the service profile | Confirm the enterprise-readable description, not raw classifications | Compile the Canonical Enterprise Service Model | Model confirmed |
| 8 | Continue | Explain that the next stage tests whether any compiled services are Designated Services | Hand the canonical model to EA-T03 | EA-T03 can commence |

## 6. Experience Principles

| Principle | Prototype requirement |
|---|---|
| Recognition before detail | Begin with familiar business and service descriptions before asking contextual questions. |
| Controlled selection | Use governed lists, checkboxes, single-select or multi-select controls; do not require free-text classification. |
| Context before facts | Ask detailed questions only after the enterprise has selected a recognisable service context. |
| Progressive disclosure | Reveal only the choices and exclusions required by the active service branch. |
| Multiple selections where valid | Permit more than one service, activity, participant, subject or capacity where the semantic structure allows it. |
| Enterprise confirms meaning | Present a coherent description of what the system understands, rather than a list of canonical values. |
| Compiler retains semantic authority | The enterprise selects business facts; the system determines canonical Conduct, Capacity, Context, Role and Composition. |
| Correction through facts | A canonical conclusion is changed by correcting its supporting selections, not by editing the conclusion directly. |
| Technical detail is secondary | Canonical assertions, patterns and lineage may be inspected but must not dominate the enterprise journey. |

## 4. Starting Context from EA-T01

EA-T02 does not begin with an unidentified business or an “empty enterprise”. It begins with the confirmed EA-T01 output.

| Starting element | Prototype treatment |
|---|---|
| Canonical Enterprise Subject | Required input |
| Legal name | Display for orientation |
| Business name | Display where available |
| Primary identifier | Available for confirmation and traceability |
| Legal form | Retained as enterprise context |
| Enterprise confirmation | Must already be complete |

Suggested transition:

> We now understand who your business is. Next, we will understand the services your business performs.

## 6. Pathway selection

The first EA-T02 choice is an application-navigation decision. It does not itself establish a canonical semantic classification.

| Prototype pathway | Enterprise-recognisable description | Semantic consequence |
|---|---|---|
| Conveyancing Practice | We perform conveyancing, property transfer or settlement work for clients. | Activate the conveyancing service-discovery branch. |
| Real Estate Agency | We market, negotiate, sell, buy, lease or manage real estate for clients. | Activate the real-estate-agency service-discovery branch. |

| Selection behaviour | Requirement |
|---|---|
| Single pathway | Permitted |
| Both pathways | Permitted where the enterprise performs both types of work |
| Neither pathway | The prototype records the slice as not applicable and does not invent another pathway |

# Part A — Conveyancing Practice Prototype Slice

## 7. Conveyancing service discovery

The prototype presents a bounded set of recognisable conveyancing activities. Multiple selections are permitted.

| Service description | Prototype status | Effect of selection |
|---|:---:|---|
| Residential property conveyancing | Included | Activate residential property-transfer facts |
| Commercial property conveyancing | Included | Activate commercial property-transfer facts |
| Property settlement services | Included | Activate settlement execution and funds-handling facts |
| Transfer documentation preparation | Included | Activate document-preparation facts |
| Mortgage discharge or refinance settlement work | Included | Activate lender, borrower and secured-interest facts |
| Off-the-plan purchase or sale work | Included | Activate future-transfer and staged-transaction facts |
| Other legal services | Deferred | Do not compile within this slice |

## 8. Conveyancing contextual selections

The system presents only the groups relevant to the services selected. The interaction mechanism is not prescribed.

### 8.1 Parties represented

| Enterprise selection | Cardinality |
|---|---|
| Buyers or purchasers | Multi-select allowed |
| Sellers or vendors | Multi-select allowed |
| Borrowers | Multi-select allowed |
| Lenders or mortgagees | Multi-select allowed |
| Developers | Multi-select allowed |
| Other parties to the property transaction | Multi-select allowed within a controlled list |

### 8.2 Work performed

| Enterprise selection | Cardinality |
|---|---|
| Prepare or review transfer documents | Multi-select allowed |
| Arrange or coordinate settlement | Multi-select allowed |
| Lodge or arrange registration of documents | Multi-select allowed |
| Receive, hold or disburse settlement funds | Multi-select allowed |
| Calculate or adjust settlement amounts | Multi-select allowed |
| Communicate or negotiate on behalf of a client | Multi-select allowed |
| Arrange discharge, refinance or registration of a mortgage | Multi-select allowed |

### 8.3 Property and transaction context

| Enterprise selection | Cardinality |
|---|---|
| Residential real estate | Multi-select allowed |
| Commercial real estate | Multi-select allowed |
| Vacant land | Multi-select allowed |
| Off-the-plan property | Multi-select allowed |
| Transfer of an existing property interest | Multi-select allowed |
| Creation or restructuring of a property interest | Multi-select allowed where applicable |

### 8.4 Authority and capacity context

| Enterprise selection | Cardinality |
|---|---|
| We act under a client engagement or appointment | Select where true |
| We act for more than one party in different matters | Select where true |
| We are authorised to receive or disburse client money | Select where true |
| We act only as an administrative messenger or lodgement channel | Select where true |

## 9. Conveyancing exclusions and limiting conditions

Only exclusions relevant to the selected services should be shown.

| Exclusion or qualification check | Consequence |
|---|---|
| The business only provides general legal advice and does not undertake property-transfer or settlement work | Exclude the conveyancing branch from this prototype slice |
| The business only introduces clients to another provider and performs no substantive conveyancing activity | Exclude or narrow the candidate composition |
| The business only performs internal administrative work for another legal practice | Prevent compilation as a standalone enterprise service unless the enterprise itself performs the service |
| The business does not act for a client or other external party | Re-evaluate Provider Capacity and recipient-role requirements |
| The business does not receive, hold or disburse funds | Exclude funds-handling facts without excluding the broader conveyancing service |

## 10. Conveyancing recomposed understanding

The enterprise reviews a coherent description assembled from its selections.

| Recomposition element | Example presentation content |
|---|---|
| Service | Residential conveyancing and property settlement |
| Parties | Buyers and sellers |
| Activities | Preparing transfer documents, coordinating settlement and disbursing settlement funds |
| Subject | Residential real estate |
| Authority | Acting under client engagement |

Illustrative statement:

> We understand that your business provides residential conveyancing and property-settlement services for buyers and sellers. Your work includes preparing transfer documentation, coordinating settlement and receiving or disbursing settlement funds under client engagements.

| Enterprise response | Required consequence |
|---|---|
| This accurately describes our work | Permit confirmation and compilation |
| Some details are wrong | Return to the affected controlled selections |
| A service is missing | Return to conveyancing service discovery |
| We are not sure | Preserve unresolved state and prevent final compilation |

# Part B — Real Estate Agency Prototype Slice

## 11. Real estate service discovery

The prototype presents a bounded set of recognisable real-estate-agency activities. Multiple selections are permitted.

| Service description | Prototype status | Effect of selection |
|---|:---:|---|
| Residential property sales | Included | Activate seller, buyer, marketing and negotiation facts |
| Commercial property sales | Included | Activate commercial-sale facts |
| Property auctions | Included | Activate auction and bidding-related facts |
| Buyer advocacy or acquisition services | Included | Activate buyer-representation facts |
| Residential leasing | Included | Activate leasing facts |
| Commercial leasing | Included | Activate commercial-leasing facts |
| Property management | Included as a distinct branch | Activate management and rent-handling facts |
| Referral-only services | Included for exclusion testing | Activate referral-only qualification checks |

## 12. Real estate contextual selections

### 12.1 Parties represented or served

| Enterprise selection | Cardinality |
|---|---|
| Property sellers or vendors | Multi-select allowed |
| Property buyers or purchasers | Multi-select allowed |
| Landlords or lessors | Multi-select allowed |
| Tenants or lessees | Multi-select allowed |
| Developers | Multi-select allowed |
| Bidders or auction participants | Multi-select allowed |

### 12.2 Work performed

| Enterprise selection | Cardinality |
|---|---|
| Market or advertise property | Multi-select allowed |
| Arrange inspections or viewings | Multi-select allowed |
| Negotiate price or transaction terms | Multi-select allowed |
| Conduct or facilitate auctions | Multi-select allowed |
| Receive expressions of interest or offers | Multi-select allowed |
| Receive or arrange deposits | Multi-select allowed |
| Introduce buyers and sellers | Multi-select allowed |
| Manage leases, rent or property operations | Multi-select allowed |
| Act as a buyer's agent or advocate | Multi-select allowed |

### 12.3 Property and transaction context

| Enterprise selection | Cardinality |
|---|---|
| Residential real estate | Multi-select allowed |
| Commercial real estate | Multi-select allowed |
| Industrial property | Multi-select allowed |
| Rural property or land | Multi-select allowed |
| Existing property sale | Multi-select allowed |
| New development or off-the-plan sale | Multi-select allowed |
| Lease or tenancy arrangement | Multi-select allowed |

### 12.4 Commercial and authority context

| Enterprise selection | Cardinality |
|---|---|
| We act under an agency appointment | Select where true |
| We are paid commission or another transaction-based fee | Select where true |
| We are authorised to negotiate on behalf of a client | Select where true |
| We receive or control deposits, rent or other client money | Select where true |
| We only advertise or refer prospective clients to another provider | Select where true |

## 13. Real estate exclusions and limiting conditions

| Exclusion or qualification check | Consequence |
|---|---|
| The enterprise only owns and sells its own property and does not act for another party | Exclude agency-capacity branches; retain only facts relevant to the enterprise's own activity if required |
| The enterprise only provides advertising space and does not introduce, negotiate or act for transaction parties | Exclude or narrow Broker/Agent candidate branches |
| The enterprise only provides referral services and performs no transaction-related activity | Compile a referral-only branch or exclude substantive agency compositions |
| Property management is performed without sales, acquisition or leasing activity | Keep property-management work separate from sales-related compositions |
| Deposits or client money are never received or controlled | Exclude money-handling facts without excluding the broader agency service |
| Auction facilities are supplied but the enterprise does not conduct or facilitate the auction | Exclude auction-conduct facts |

## 14. Real estate recomposed understanding

| Recomposition element | Example presentation content |
|---|---|
| Service | Residential property sales and auctions |
| Parties | Property sellers and prospective buyers |
| Activities | Marketing property, arranging inspections, negotiating offers and conducting auctions |
| Subject | Residential real estate |
| Authority | Acting under seller agency appointments |

Illustrative statement:

> We understand that your business acts for property sellers in residential real estate transactions. Your agency markets properties, arranges inspections, negotiates offers and may conduct auctions under seller agency appointments.

| Enterprise response | Required consequence |
|---|---|
| This accurately describes our work | Permit confirmation and compilation |
| Some details are wrong | Return to the affected controlled selections |
| A service is missing | Return to real estate service discovery |
| We are not sure | Preserve unresolved state and prevent final compilation |

## 8. Compiler Behaviour

The user experience remains business-facing, while the compiler performs the canonical transformation.

| Enterprise action or state | Compiler behaviour |
|---|---|
| Selects a business pathway | Activates the associated prototype acquisition scope |
| Selects one or more services | Creates candidate Service Arrangement and composition branches |
| Selects contextual details | Establishes or updates Enterprise Facts |
| Resolves an exclusion | Removes, narrows or retains affected semantic branches |
| Changes a prior selection | Invalidates dependent assertions and recompiles affected branches |
| Reaches sufficient fact completeness | Evaluates canonical assertions |
| Accepts the recomposed understanding | Compiles confirmed Service Conduct Compositions |
| Confirms all included services | Produces the Canonical Enterprise Service Model |

## 9. Canonical Output

The prototype must produce enough canonical state to demonstrate the EA-T02 transformation without attempting the full production model.

| Canonical element | Minimum prototype requirement |
|---|---|
| Enterprise Service Model | One model linked to the confirmed EA-T01 Enterprise |
| Enterprise Service Arrangement | At least one per materially distinct selected service grouping |
| Service Conduct Composition | At least one complete composition for each demonstrated pathway |
| Pattern Instantiation | Applicable prototype Pattern obligations resolved |
| Established Semantic Assertions | Required Conduct, Capacity, Context, Subject, Role and other applicable values established |
| Semantic relationships | Arrangement, composition, participant and subject relationships preserved |
| Lineage | Each canonical conclusion traces to controlled enterprise selections and the governing semantic authority |
| Completeness state | Confirmed as complete for the bounded prototype slice |

## 17. Enterprise-facing result

The primary result is a concise service profile. Technical detail remains available but secondary.

| Result layer | Audience | Required content |
|---|---|---|
| Business service profile | Enterprise | Coherent descriptions of each confirmed service arrangement |
| Service details | Product or compliance user | Activities, parties, property types and limiting conditions |
| Technical detail | Semantic architect or engineer | Compositions, Pattern Instantiations, assertions, lineage and states |

The result must not state that a service is a Designated Service or that the enterprise is a Reporting Entity.

## 10. State Model

| Enterprise-facing state | System meaning |
|---|---|
| Not started | No EA-T02 pathway selected |
| Selecting services | One or more pathway or service selections exist |
| Describing service | Required contextual facts are incomplete |
| Needs attention | A required choice, exclusion or contradiction remains unresolved |
| Ready to review | The bounded fact set is sufficient to recompose an enterprise-readable understanding |
| Confirmed | The enterprise has accepted the recomposed service description |
| Compiled | The Canonical Enterprise Service Model has been produced for the prototype slice |

## 11. Product/UX Latitude

This model defines the journey and semantic behaviour, not the interface implementation.

| May be designed by product, UX or engineering | Must remain invariant |
|---|---|
| Page, panel, wizard, conversational or dashboard structure | Controlled pathway and service selections |
| Visual hierarchy and component choice | Contextual progressive disclosure |
| Navigation pattern | Enterprise Facts remain the acquired authority |
| Wording refinements that preserve meaning | Canonical conclusions remain compiler-owned |
| Desktop or responsive behaviour | Exclusion logic and dependency behaviour |
| How technical detail is revealed | Enterprise-readable recomposition before confirmation |
| Animation, transitions and progress treatment | Deterministic recompilation after corrections |

## 12. Acceptance Criteria

| ID | Criterion |
|---|---|
| P-AC-001 | The journey begins with the confirmed EA-T01 Enterprise. |
| P-AC-002 | A user can recognise and select either the Conveyancing Practice or Real Estate Agency pathway without semantic or legislative expertise. |
| P-AC-003 | Multiple services and contextual values can be selected where allowed. |
| P-AC-004 | No free-text service classification is required. |
| P-AC-005 | Only facts and exclusions relevant to selected services are presented. |
| P-AC-006 | The enterprise is never asked to select canonical Conduct, Capacity, Context, Pattern or Designated Service values. |
| P-AC-007 | Each pathway recompiles selections into a coherent enterprise-readable service description. |
| P-AC-008 | Editing a selection deterministically updates the affected description and canonical branch. |
| P-AC-009 | At least one Service Conduct Composition can be compiled for each pathway. |
| P-AC-010 | The prototype produces one Canonical Enterprise Service Model linked to the EA-T01 Enterprise. |
| P-AC-011 | Every canonical conclusion remains traceable to controlled selections and semantic authority. |
| P-AC-012 | No Designated Service, Reporting Entity, risk or AML/CTF obligation conclusion is produced. |
| P-AC-013 | The compiled model is suitable for direct handover to EA-T03. |

## 13. Source Alignment

| Prototype concern | EA-T02 source authority |
|---|---|
| Enterprise Service Model boundary and purpose | Semantic Object and Semantic Specification |
| Service grammar, canonical vocabularies and composition structures | Knowledge Architecture |
| Required semantic conclusions and completeness | Semantic Assertion Contract |
| Controlled fact requirements and acquisition dependencies | Enterprise Fact Acquisition Pattern |
| Fact-to-assertion reasoning and exclusions | Semantic Evaluation Specification |
| Assertion-to-model transformation | Semantic Compilation Specification |
| Canonical handover model | Canonical Enterprise Service Model |

## 14. Downstream Handover

| Handover element | Minimum guarantee |
|---|---|
| Enterprise | The model is linked to the confirmed EA-T01 Enterprise Subject |
| Service arrangements | Demonstrated conveyancing and/or real-estate arrangements are identifiable |
| Compositions | Required prototype Service Conduct Compositions are complete |
| Assertions | Canonical assertions are established and traceable |
| Exclusions | Relevant prototype exclusions are resolved |
| Confirmation | The enterprise has accepted the business-readable service profile |
| Output | A Canonical Enterprise Service Model is available to EA-T03 |

Suggested transition:

> We now understand the services your business performs. Next, we will determine whether any of those services are Designated Services under the AML/CTF framework.

## 15. Completion Boundary

The first working prototype is complete when both pathways can be demonstrated end to end from the confirmed EA-T01 Enterprise through controlled service discovery, contextual fact selection, relevant exclusion testing, plain-language review, confirmation and compilation of the Canonical Enterprise Service Model.

It does not need to demonstrate every service family, canonical value, composition pattern, exclusion, arrangement relationship or production exception supported by EA-T02.
