# EA-T01 Prototype Interaction Specification

  Property          Value
  ----------------- -------------------------------------
  Semantic Object   EA-T01 Enterprise
  Artefact          Prototype Interaction Specification
  Version           1.0.0-rc1
  Status            Draft
  Authority         Informative
  Audience          Product, UX, Engineering
  Derived From      EA-T01 Experience Model (Frozen)

------------------------------------------------------------------------

## Purpose

Define the interaction capabilities required to realise the EA-T01
Enterprise Experience while remaining implementation independent.

This specification describes **what the interaction must achieve**, not
how it is presented.

------------------------------------------------------------------------

## Transformation Boundary

  Property          Value
  ----------------- ---------------------------------------------------
  **Start State**   Enterprise identity has not yet been established.
  **End State**     Canonical Enterprise Subject is ready for EA-T02.

------------------------------------------------------------------------

## Interaction Principles

  -----------------------------------------------------------------------
  Principle                           Intent
  ----------------------------------- -----------------------------------
  Enterprise Recognition              The enterprise recognises concepts
                                      rather than classifying them.

  Progressive Disclosure              Only the information required for
                                      the current transformation is
                                      introduced.

  Compiler Ownership                  Semantic conclusions remain
                                      compiler-owned.

  Enterprise Confirmation             The enterprise confirms
                                      understanding rather than semantic
                                      structures.

  Deterministic Recomposition         Review always reflects the current
                                      semantic state.

  Implementation Independence         UX determines presentation while
                                      preserving semantic behaviour.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Interaction Capability

### Interaction 1 --- Enterprise Identification

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Interaction Intent                  Identify the Enterprise.

  Enterprise Needs To                 Recognise the legal enterprise
                                      being established.

  Information Required                Minimum governed identity
                                      information sufficient to
                                      distinguish a candidate Enterprise.

  Compiler Needs To                   Establish a Candidate Enterprise.

  Enterprise Understands              Which enterprise is currently being
                                      established.

  Completion Signal                   One Candidate Enterprise exists.

  UX Latitude                         Any interaction pattern that
                                      preserves semantic intent.
  -----------------------------------------------------------------------

### Interaction 2 --- Enterprise Identity Confirmation

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Interaction Intent                  Confirm the recognised Enterprise
                                      identity.

  Enterprise Needs To                 Confirm or correct the current
                                      understanding.

  Information Required                Applicable identity and existence
                                      information.

  Compiler Needs To                   Validate identity coherence and
                                      preserve lineage.

  Enterprise Understands              The current enterprise identity.

  Completion Signal                   Identity confirmed.

  UX Latitude                         Grouping, layout and confirmation
                                      pattern are implementation choices.
  -----------------------------------------------------------------------

### Interaction 3 --- Legal Constitution Recognition

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Interaction Intent                  Establish the governed Legal Form.

  Enterprise Needs To                 Recognise the applicable legal
                                      constitution.

  Information Required                Governed Legal Form and, where
                                      applicable, subtype.

  Compiler Needs To                   Resolve applicability and the
                                      semantic branch.

  Enterprise Understands              The legal form through which the
                                      Enterprise exists.

  Completion Signal                   Applicable branch resolved.

  UX Latitude                         Any presentation preserving
                                      governed values.
  -----------------------------------------------------------------------

### Interaction 4 --- Enterprise Understanding

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Interaction Intent                  Present the compiler's
                                      understanding for review.

  Enterprise Needs To                 Review the recomposed
                                      understanding.

  Information Required                Established Enterprise state.

  Compiler Needs To                   Evaluate contract readiness.

  Enterprise Understands              The system's current understanding
                                      of the Enterprise.

  Completion Signal                   Enterprise confirms or requests
                                      correction.

  UX Latitude                         Any review or summary pattern.
  -----------------------------------------------------------------------

### Interaction 5 --- Completion and Handover

  Property                 Value
  ------------------------ -----------------------------------------
  Interaction Intent       Complete the transformation.
  Enterprise Needs To      Continue to the next semantic stage.
  Information Required     Confirmed Canonical Enterprise Subject.
  Compiler Needs To        Publish the canonical output.
  Enterprise Understands   Enterprise establishment is complete.
  Completion Signal        EA-T02 is ready to commence.
  UX Latitude              Any completion or transition treatment.

------------------------------------------------------------------------

## Interaction Invariants

  -----------------------------------------------------------------------
  The Prototype Shall                 The Prototype Shall Not
  ----------------------------------- -----------------------------------
  Support enterprise recognition      Require semantic expertise

  Present enterprise-readable         Expose compiler structures as the
  understanding                       primary experience

  Preserve deterministic              Allow direct editing of
  recompilation                       compiler-owned conclusions

  Preserve semantic completion        Merge semantic transformations for
  boundaries                          convenience

  Preserve governed values            Invent or alter semantic meaning
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Handover

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Downstream Consumer                 EA-T02 Business Operating Model

  Enterprise Message                  We now understand who your business
                                      is. Next, we will understand the
                                      services your business performs.

  Compiler Guarantee                  One Canonical Enterprise Subject is
                                      available for downstream
                                      consumption.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Completion Boundary

This specification is complete when every interaction required to
establish the EA-T01 Canonical Enterprise Subject has been defined in
terms of interaction intent, enterprise understanding, compiler
responsibility and completion signal, while leaving implementation
decisions to Product and UX.
