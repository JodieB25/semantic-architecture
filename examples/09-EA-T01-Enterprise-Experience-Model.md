# EA-T01 Enterprise Experience Model

  Property          Value
  ----------------- -----------------------------------
  Semantic Object   EA-T01 Enterprise
  Artefact          Enterprise Experience Model
  Version           1.0.0-rc1
  Status            Draft
  Authority         Informative
  Audience          Product, UX, Engineering
  Derived From      EA-T01 Canonical Enterprise Model

------------------------------------------------------------------------

## Purpose

Describe the enterprise experience required to establish a canonical
Enterprise Subject without prescribing interface implementation. This
specification defines **what the enterprise experiences and
recognises**, not how the experience is rendered.

------------------------------------------------------------------------

## Transformation Boundary

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  **Start State**                     Enterprise identity has not yet
                                      been established.

  **End State**                       Canonical Enterprise Subject
                                      confirmed and available to EA-T02.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Prototype Objective

  -----------------------------------------------------------------------
  Perspective                         Required Outcome
  ----------------------------------- -----------------------------------
  Enterprise                          Recognise and confirm the
                                      Enterprise identity.

  Product                             Provide one coherent semantic
                                      journey from unknown Enterprise to
                                      confirmed Enterprise.

  UX                                  Support progressive recognition,
                                      review and confirmation without
                                      exposing semantic complexity.

  Engineering                         Produce a deterministic Canonical
                                      Enterprise Subject for downstream
                                      consumption.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Prototype Boundary

  -----------------------------------------------------------------------
  Included                            Deferred
  ----------------------------------- -----------------------------------
  Enterprise identification           Full legal structure branching

  Enterprise identity confirmation    Complete identifier catalogue

  Legal constitution recognition      Advanced governing powers

  Enterprise review and confirmation  Full production exception handling

  Canonical handover to EA-T02        Complete structural relationship
                                      modelling
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Enterprise Journey

  ------------------------------------------------------------------------
                  Stage Enterprise Goal  Enterprise       Completion
                                         Experience       Signal
  --------------------- ---------------- ---------------- ----------------
                      1 Understand the   Recognise why    Enterprise is
                        purpose          the Enterprise   ready to begin.
                                         must be          
                                         established      
                                         before any later 
                                         assessment.      

                      2 Identify the     Recognise and    Candidate
                        Enterprise       distinguish the  Enterprise
                                         correct legal    established.
                                         enterprise.      

                      3 Confirm          Confirm the      Identity
                        Enterprise       enterprise's     recognised as
                        identity         identity and     correct or
                                         current          corrected.
                                         existence.       

                      4 Recognise legal  Confirm the      Legal
                        constitution     applicable legal constitution
                                         form.            established.

                      5 Review           Review a         Enterprise
                        understanding    plain-language   understanding
                                         recomposition of confirmed.
                                         the Enterprise.  

                      6 Complete         Confirm          Canonical
                        transformation   completion and   Enterprise
                                         prepare for      Subject
                                         service          published.
                                         understanding.   
  ------------------------------------------------------------------------

------------------------------------------------------------------------

## Enterprise Recognition

  -----------------------------------------------------------------------
  Transformation Stage    Enterprise Recognises   Semantic Purpose
  ----------------------- ----------------------- -----------------------
  Enterprise              The legal enterprise    Distinguish one
  Identification          being established.      governed Enterprise.

  Identity Recognition    The enterprise identity Confirm governed
                          currently understood.   identity.

  Legal Constitution      The legal form through  Resolve applicability.
  Recognition             which the Enterprise    
                          exists.                 

  Enterprise              The compiler's          Confirm semantic
  Understanding           recomposed              understanding.
                          understanding.          

  Enterprise Completion   The Enterprise has been Enable EA-T02.
                          established.            
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Enterprise Review

  -----------------------------------------------------------------------
  Enterprise Reviews                  Enterprise Understands
  ----------------------------------- -----------------------------------
  Enterprise identity                 Who the system believes the
                                      Enterprise is.

  Legal constitution                  The recognised legal form.

  Enterprise summary                  A coherent business-readable
                                      description rather than semantic
                                      fields.
  -----------------------------------------------------------------------

Illustrative review statement:

> We have identified your enterprise as **ABC Conveyancing Pty Ltd**, an
> active Australian company operating under the business name **ABC
> Conveyancing**.

------------------------------------------------------------------------

## Enterprise Confirmation

  -----------------------------------------------------------------------
  Enterprise Decision                 Semantic Result
  ----------------------------------- -----------------------------------
  Confirm                             Canonical Enterprise Subject
                                      constructed.

  Correct                             Return to the affected semantic
                                      interaction and recompose
                                      understanding.

  Defer                               Enterprise remains unresolved and
                                      handover is prevented.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Transition

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Downstream Consumer                 EA-T02 Business Operating Model

  Enterprise Message                  We now understand who your business
                                      is. Next, we will understand the
                                      services your business performs.

  Semantic Guarantee                  One confirmed Canonical Enterprise
                                      Subject is available to EA-T02.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## UX Latitude

  -----------------------------------------------------------------------
  UX May                              UX Must Not
  ----------------------------------- -----------------------------------
  Choose layouts, navigation,         Change semantic meaning or governed
  controls and interaction patterns.  values.

  Refine wording while preserving     Merge semantic completion
  meaning.                            boundaries.

  Decide visual hierarchy and         Make compiler-owned conclusions
  responsiveness.                     directly editable.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Acceptance Criteria

  ID       Criterion
  -------- ------------------------------------------------------------
  EM-001   The enterprise can recognise and confirm its identity.
  EM-002   The experience remains implementation independent.
  EM-003   The review presents enterprise-readable understanding.
  EM-004   Confirmation produces one Canonical Enterprise Subject.
  EM-005   The transformation concludes with a valid EA-T02 handover.

------------------------------------------------------------------------

## Completion Boundary

The prototype is complete when an enterprise can progress from an
unidentified legal subject to a confirmed Canonical Enterprise Subject
through recognition, confirmation and review, without requiring semantic
expertise or exposing implementation detail. The Experience Model
defines the semantic experience only; interaction design and
implementation remain downstream concerns.
