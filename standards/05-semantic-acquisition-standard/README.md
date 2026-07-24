---
id: SA-SAS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Semantic Acquisition Standard

## 1. Purpose

This standard defines the reusable model for progressively establishing the governed semantic information required by an Information Contract.

## 2. Authority

A package Information Acquisition Pattern owns acquisition stages, acquisition states, progressive acquisition rules, source classes, validation and completion. It does not redefine knowledge or prescribe implementation journeys.

## 3. Acquisition lifecycle

```text
Unknown
  ↓
Candidate
  ↓
Claimed or Observed
  ↓
Corroborated
  ↓
Established
  ↓
Contract-ready
```

## 4. Acquisition states

| ID | State | Meaning |
|---|---|---|
| AS-UNKNOWN | Unknown | No governed assertion is available. |
| AS-CANDIDATE | Candidate | A possible assertion has been identified. |
| AS-CLAIMED | Claimed | A subject or source has asserted the information. |
| AS-OBSERVED | Observed | Information has been directly observed from a source. |
| AS-CORROBORATED | Corroborated | Independent information supports the assertion. |
| AS-ESTABLISHED | Established | The information is semantically suitable for contract evaluation. |
| AS-CONTRACT-READY | Contract-ready | Required applicable information is available to the Information Contract. |

## 5. Rule schema

Every progressive acquisition rule SHALL define its identifier, purpose, preconditions, target knowledge reference, permitted source classes, validation, produced acquisition state, failure outcome and lineage.

## 6. Requirements

| ID | Requirement |
|---|---|
| SA-P-001 | Acquisition SHALL begin with the minimum knowledge required to resolve subsequent applicability. |
| SA-P-002 | Only applicable knowledge SHALL be acquired after applicability is resolved. |
| SA-P-003 | Applicability SHALL be re-evaluated when governing semantic information changes before compilation. |
| SA-P-004 | Acquisition SHALL stop when the Information Contract is satisfied; it SHALL NOT require all possible information. |
| SA-P-005 | The standard SHALL NOT prescribe forms, screens, APIs, workflow engines or persistence. |

## 7. Conformance

An acquisition pattern conforms when it can progressively establish a contract-ready information set while preserving knowledge authority and implementation independence.
