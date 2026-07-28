# EA-T01 Prototype Content Pack

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Semantic Object                     EA-T01 Enterprise

  Artefact                            Prototype Content Pack

  Version                             1.0.0-rc1

  Status                              Draft

  Authority                           Informative

  Audience                            Product, UX, Engineering

  Derived From                        EA-T01 Experience Model, Prototype
                                      Interaction Specification, Compiler
                                      Behaviour Specification
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Purpose

Provide the governed content required to demonstrate the bounded EA-T01
prototype using two supported business scenarios while preserving
traceability to the governing semantic artefacts.

------------------------------------------------------------------------

## Transformation Boundary

  Property          Value
  ----------------- --------------------------------------------------
  **Start State**   Enterprise identity not yet established
  **End State**     Canonical Enterprise Subject available to EA-T02

------------------------------------------------------------------------

# Supported Prototype Scenarios

  -----------------------------------------------------------------------------
  Scenario          Business Type     Purpose                 Downstream Path
  ----------------- ----------------- ----------------------- -----------------
  TS-001            Conveyancing      Demonstrate the         Conveyancing
                    Practice          professional-services   
                                      pathway.                

  TS-002            Real Estate       Demonstrate the         Real Estate
                    Agency            real-estate-services    
                                      pathway.                
  -----------------------------------------------------------------------------

------------------------------------------------------------------------

# Governed Selection Catalogues

## Primary Legal Forms

  Code    Value
  ------- ------------------------------------------------
  LF-01   Individual Acting as Sole Trader
  LF-02   Body Corporate
  LF-03   Partnership
  LF-04   Trust or Foreign Equivalent
  LF-05   Unincorporated Association
  LF-06   Government Body
  LF-07   Other Legally Recognised Person or Arrangement

## Body Corporate Subtypes

  Code    Value
  ------- --------------------------
  BC-01   Australian Company
  BC-02   Foreign Body Corporate
  BC-03   Incorporated Association
  BC-04   Registered Co-operative
  BC-05   Incorporated Partnership
  BC-06   Other Body Corporate

## Structural Role Specialisations

  Code    Value
  ------- -------------------------------------------------------
  SR-01   Director Relationship
  SR-02   Trustee Relationship
  SR-03   Partner Relationship
  SR-04   Committee Member Relationship
  SR-05   Office Holder Relationship
  SR-06   Government Office Relationship
  SR-07   Other Legally Recognised Structural Role Relationship

------------------------------------------------------------------------

# Prototype Scenario Values

  -----------------------------------------------------------------------
  Semantic Intent         TS-001 Conveyancing     TS-002 Real Estate
                                                  Agency
  ----------------------- ----------------------- -----------------------
  Enterprise Legal Name   ABC Conveyancing Pty    ABC Realty Pty Ltd
                          Ltd                     

  Business Name           ABC Conveyancing        ABC Realty

  ABN                     12 345 678 901          98 765 432 109

  ACN                     123 456 789             987 654 321

  Establishment           New South Wales         New South Wales
  Jurisdiction                                    

  Enterprise Status       Active                  Active

  Legal Form              LF-02 Body Corporate    LF-02 Body Corporate

  Body Corporate Subtype  BC-01 Australian        BC-01 Australian
                          Company                 Company

  Structural Role         SR-01 Director          SR-01 Director
                          Relationship            Relationship
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Interaction Outcomes

  -----------------------------------------------------------------------
  Interaction Intent      TS-001                  TS-002
  ----------------------- ----------------------- -----------------------
  Enterprise              Candidate Enterprise    Candidate Enterprise
  Identification          established             established

  Enterprise Confirmation Conveyancing enterprise Real estate enterprise
                          confirmed               confirmed

  Legal Constitution      Body Corporate          Body Corporate
                          recognised              recognised

  Enterprise              Review accepted         Review accepted
  Understanding                                   

  Completion              Canonical Enterprise    Canonical Enterprise
                          Subject published       Subject published
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Compiler States

  -----------------------------------------------------------------------
  Runtime Stage           TS-001                  TS-002
  ----------------------- ----------------------- -----------------------
  Initialise              Runtime context created Runtime context created

  Identity                Enterprise established  Enterprise established

  Applicability           Applicable branch       Applicable branch
                          resolved                resolved

  Completeness            Contract ready          Contract ready

  Compilation             Canonical Enterprise    Canonical Enterprise
                          Subject                 Subject

  Publication             EA-T02 handover ready   EA-T02 handover ready
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Enterprise Review Content

  -----------------------------------------------------------------------
  Review Element          TS-001 Conveyancing     TS-002 Real Estate
  ----------------------- ----------------------- -----------------------
  Enterprise              ABC Conveyancing Pty    ABC Realty Pty Ltd
                          Ltd                     

  Business Name           ABC Conveyancing        ABC Realty

  Status                  Active                  Active

  Legal Form              Australian Company      Australian Company

  Review Statement        We have identified your We have identified your
                          enterprise as **ABC     enterprise as **ABC
                          Conveyancing Pty Ltd**, Realty Pty Ltd**, an
                          an active Australian    active Australian
                          company operating under company operating under
                          the business name **ABC the business name **ABC
                          Conveyancing**.         Realty**.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Transition Content

  -----------------------------------------------------------------------
  Property                            Value
  ----------------------------------- -----------------------------------
  Enterprise Message                  We now understand who your business
                                      is. Next, we will understand the
                                      services your business performs.

  Compiler Message                    Canonical Enterprise Subject
                                      published.

  Downstream Consumer                 EA-T02 Business Operating Model
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Traceability

  Prototype Content       Governing Artefact
  ----------------------- -------------------------------------
  Governed values         EA-T01 Knowledge Architecture
  Enterprise experience   EA-T01 Experience Model
  Interaction outcomes    Prototype Interaction Specification
  Compiler states         Compiler Behaviour Specification
  Scenario values         Synthetic prototype scenarios

------------------------------------------------------------------------

# Completion Boundary

This content pack is complete when both supported prototype scenarios
can traverse the complete EA-T01 transformation using the same governed
value catalogues while producing distinct enterprise content and a
common canonical Enterprise handover to EA-T02.
