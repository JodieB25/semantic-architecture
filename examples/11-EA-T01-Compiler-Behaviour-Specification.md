# EA-T01 Compiler Behaviour Specification

  Property          Value
  ----------------- -----------------------------------
  Semantic Object   EA-T01 Enterprise
  Artefact          Compiler Behaviour Specification
  Version           1.0.0-rc1
  Status            Draft
  Authority         Informative
  Audience          Engineering
  Derived From      EA-T01 Canonical Enterprise Model

------------------------------------------------------------------------

## Purpose

Describe the deterministic runtime behaviour required to compile the
EA-T01 Canonical Enterprise Subject. This specification defines **what
the compiler does**, not how the user interacts with it.

------------------------------------------------------------------------

## Transformation Boundary

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  **Start State**                     Enterprise facts sufficient to
                                      identify a candidate Enterprise.

  **End State**                       Canonical Enterprise Subject
                                      published and available to EA-T02.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Runtime Context

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Current Transformation              EA-T01 Enterprise

  Upstream Dependency                 None (Root Transformation)

  Downstream Consumer                 EA-T02 Business Operating Model

  Runtime Trigger                     Enterprise information becomes
                                      available for semantic compilation.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Compiler Runtime

  ------------------------------------------------------------------------
                  Stage Consumes         Compiler         Produces
                                         Behaviour        
  --------------------- ---------------- ---------------- ----------------
                      1 Enterprise facts Initialise the   Runtime context
                                         root semantic    
                                         transformation   
                                         and runtime      
                                         context.         

                      2 Candidate        Resolve          Established
                        Enterprise       Enterprise       Enterprise
                        information      identity and     identity
                                         validate         
                                         identity         
                                         coherence.       

                      3 Legal Form and   Resolve          Applicable
                        applicable       applicability    Knowledge Unit
                        subtype          and determine    set
                                         the applicable   
                                         knowledge        
                                         branch.          

                      4 Applicable       Evaluate         Contract-ready
                        established      Information      state
                        knowledge        Contract         
                                         completeness and 
                                         semantic         
                                         readiness.       

                      5 Contract-ready   Construct the    Canonical
                        state            Canonical        Enterprise
                                         Enterprise       Subject
                                         Subject,         
                                         preserving       
                                         identity and     
                                         lineage.         

                      6 Canonical        Publish the      EA-T02-ready
                        Enterprise       canonical output handover
                        Subject          and downstream   
                                         guarantee.       
  ------------------------------------------------------------------------

------------------------------------------------------------------------

## Compiler Guarantees

  -----------------------------------------------------------------------
  Compiler SHALL                      Compiler SHALL NOT
  ----------------------------------- -----------------------------------
  Preserve canonical identity         Redefine legislative meaning

  Preserve canonical lineage          Invent enterprise facts

  Produce deterministic outputs       Perform organisational judgement

  Preserve canonical identifiers      Alter semantic meaning

  Publish one canonical Enterprise    Merge semantic transformations
  Subject                             
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Recompilation Behaviour

  Change Detected                     Recompile From
  ----------------------------------- ----------------
  Enterprise identity                 Stage 2
  Legal Form or subtype               Stage 3
  Applicable governed knowledge       Stage 4
  Information Contract completeness   Stage 4

Unchanged canonical state SHALL be preserved.

------------------------------------------------------------------------

## Explainability

  Compiler Explains          Primary Source
  -------------------------- ------------------------------
  Enterprise identity        Enterprise facts
  Applicability resolution   Legal Form
  Information completeness   Information Contract
  Canonical construction     Semantic Compilation
  Downstream readiness       Canonical Enterprise Subject

------------------------------------------------------------------------

## Handover

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Output                              Canonical Enterprise Subject

  Consumer                            EA-T02 Business Operating Model

  Guarantee                           One downstream-ready canonical
                                      Enterprise state with preserved
                                      identity and lineage.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Completion Boundary

Compilation is complete when one Canonical Enterprise Subject has been
deterministically constructed, identity and lineage have been preserved,
the downstream guarantee has been published, and EA-T02 may commence
without requiring re-acquisition of Enterprise identity.
