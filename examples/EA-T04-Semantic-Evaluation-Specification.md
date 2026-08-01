---
id: EA-T04-SES
name: EA-T04 Reporting Entity Semantic Evaluation Specification
document: Semantic Evaluation Specification
version: 1.0.0-rc1
status: Candidate
authority: Normative
semantic_object: EA-T04 Reporting Entity
governing_standard: SA-SES v2.0.0-rc1
depends_on:
  - EA-T04-KA v1.0.0-rc1
  - EA-T04-SAC v1.0.0-rc1
  - EA-T04-SIP v1.0.0-rc1
---

# EA-T04 Reporting Entity Semantic Evaluation Specification

## Document Identity

| Property | Value |
|---|---|
| Artefact ID | EA-T04-SES |
| Canonical Name | EA-T04 Reporting Entity Semantic Evaluation Specification |
| Semantic Object | EA-T04 Reporting Entity |
| Governing Standard | SA-SES v2.0.0-rc1 |
| Authority | Normative |
| Version | 1.0.0-rc1 |
| Status | Candidate |
| Upstream Dependencies | EA-T04 Knowledge Architecture; EA-T04 Semantic Assertion Contract; EA-T04 Semantic Input Pattern |
| Downstream Consumer | EA-T04 Semantic Compilation Specification |

## 1. Purpose

This specification defines how the authoritative EA-T04 Knowledge Architecture is deterministically applied to governed canonical models and authoritative Enterprise Facts to establish the Semantic Assertions required by the EA-T04 Semantic Assertion Contract.

## 2. Evaluation Equation

```text
EA-T04 Authoritative Knowledge
+
Governed Semantic Inputs
→
Established EA-T04 Semantic Assertions
```

Evaluation establishes assertions. It does not acquire facts, redefine knowledge, compile the Canonical Enterprise Reporting Entity Model or introduce presentation behaviour.

## 3. Authority and Boundary

### 3.1 Evaluation owns

- deterministic fact-to-assertion reasoning;
- applicability resolution;
- explicit conflict and insufficiency handling;
- assertion resolution-state assignment;
- dependency-aware evaluation sequencing;
- attachment-scope and temporal-scope preservation;
- lineage from each result to the rules, inputs and Knowledge Units applied.

### 3.2 Evaluation does not own

- Enterprise Fact acquisition;
- upstream canonical model reconstruction or mutation;
- Knowledge Unit meaning;
- assertion participation or proof obligations;
- canonical model transformation;
- renderer, workflow or user-interface behaviour.

## 4. Governed Evaluation Inputs

| Input ID | Canonical Name | Input Class | Participation |
|---|---|---|---|
| IN-CSM-001 | Canonical Enterprise Model | Canonical Semantic Models | Required |
| IN-CSM-002 | Canonical Enterprise Designated Service Model | Canonical Semantic Models | Required |
| IN-EF-001 | Legislative Person Resolution Facts | Enterprise Facts | Conditional |
| IN-EF-002 | Business Group Structure Facts | Enterprise Facts | Conditional |
| IN-EF-003 | Reporting Group Formation and Membership Facts | Enterprise Facts | Conditional |
| IN-EF-004 | Lead Entity Qualification Facts | Enterprise Facts | Conditional |
| IN-EF-005 | Responsibility Attribution and Continuity Facts | Enterprise Facts | Conditional |
| IN-AK-001 | EA-T04 Reporting Entity Knowledge Architecture | Authoritative Knowledge | Required |
| IN-ERM-001 | Australian Legal and Registration Reference Data | External Reference Models | Optional |

All inputs SHALL retain the source identity, version, effective period and lineage obligations declared by the Semantic Input Pattern.

## 5. Evaluation Result Model

Every evaluation rule produces one governed assertion result containing:

| Field | Requirement |
|---|---|
| Assertion ID | Stable identifier from the Semantic Assertion Contract. |
| Resolution State | Established, Explicitly Absent, Deferred, Unresolved or Unsupported by Facts. |
| Participation | Required, Conditional, Optional or Not Applicable. |
| Semantic Subject | Qualified subject to which the assertion attaches. |
| Temporal Scope | Determination period or narrower effective period. |
| Rule ID | Stable evaluation-rule identifier. |
| Knowledge Unit ID | Authoritative Knowledge Unit applied. |
| Input Lineage | Canonical model elements and Enterprise Facts used. |
| Traceability ID | Legislative traceability identifier inherited from the Knowledge Architecture. |
| Conflict Record | Any conflicting inputs and their governed disposition. |

## 6. Common Resolution Rules

| Rule ID | Condition | Result |
|---|---|---|
| ER-COM-001 | The assertion is applicable, every mandatory dependency is eligible, and the authoritative facts satisfy the Knowledge Unit. | Established |
| ER-COM-002 | The assertion is applicable, every mandatory dependency is eligible, and authoritative facts establish that the proposition does not apply or is absent. | Explicitly Absent |
| ER-COM-003 | Evaluation is intentionally postponed by a governed package decision. | Deferred |
| ER-COM-004 | Inputs are present but materially inconsistent, incomplete or incapable of deterministic resolution. | Unresolved |
| ER-COM-005 | A mandatory factual proposition cannot be supported by an authoritative fact source. | Unsupported by Facts |
| ER-COM-006 | A Conditional assertion is not applicable to the qualified subject. | Not Applicable participation; no missing assertion is created. |

## 7. Determinism, Conflict and Sufficiency

### 7.1 Determinism

Identical Knowledge Architecture versions, input versions, fact sets, effective periods and evaluation-rule versions SHALL produce identical assertion results.

### 7.2 Conflict handling

When authoritative inputs conflict, evaluation SHALL NOT silently select one value. The affected assertion SHALL resolve as Unresolved unless an explicit source-precedence rule exists in the Knowledge Architecture or Semantic Input Pattern. The conflict record SHALL identify every competing source.

### 7.3 Insufficiency handling

Missing facts SHALL resolve as Unsupported by Facts where the required fact category has no authoritative support. Incomplete or indeterminate facts SHALL resolve as Unresolved. Missing upstream canonical state SHALL not be patched by a parallel acquisition path.

### 7.4 Temporal handling

Evaluation SHALL apply the source, Knowledge Unit and factual state effective for the determination period. Historical and current periods SHALL not be merged.

## 8. Evaluation Sequence

```text
1. Validate governed input identity, version and effective period
2. Resolve assertion applicability
3. Validate assertion dependencies
4. Apply the authoritative Knowledge Unit to authoritative inputs
5. Assign an explicit resolution state
6. Preserve subject, temporal and legislative lineage
7. Test pattern, composition and aggregate sufficiency
8. Declare transformation eligibility
```

## 9. Evaluation Rule Catalogue

### 9.1 KF-01 — Legislative Person Resolution

**Governed inputs:** IN-CSM-001, IN-EF-001, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-01.01 | SA-01.01 — Ordinary Person Treatment Assertion | KU-01.01 | None | IN-CSM-001, IN-EF-001, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-010 |
| ER-01.02 | SA-01.02 — Partnership Treatment Assertion | KU-01.02 | None | IN-CSM-001, IN-EF-001, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-011 |
| ER-01.03 | SA-01.03 — Unincorporated Association Treatment Assertion | KU-01.03 | None | IN-CSM-001, IN-EF-001, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-012 |
| ER-01.04 | SA-01.04 — Trust Treatment Assertion | KU-01.04 | None | IN-CSM-001, IN-EF-001, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-013 |
| ER-01.05 | SA-01.05 — Enterprise–Legislative Person Correspondence Assertion | KU-01.05 | SA-01.01, SA-01.02, SA-01.03, SA-01.04 | IN-CSM-001, IN-EF-001, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-014 |

### 9.2 KF-02 — Reporting Entity Establishment

**Governed inputs:** IN-CSM-001, IN-CSM-002, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-02.01 | SA-02.01 — Reporting Entity Definition Assertion | KU-02.01 | SA-01.05 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-020 |
| ER-02.02 | SA-02.02 — Designated Service Provider Pathway Assertion | KU-02.02 | SA-02.01 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-021 |
| ER-02.03 | SA-02.03 — Lead Entity Pathway Assertion | KU-02.03 | SA-02.01, SA-07.16 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-022 |
| ER-02.04 | SA-02.04 — Establishment Basis Assertion | KU-02.04 | SA-02.02, SA-02.03 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-023 |
| ER-02.05 | SA-02.05 — Status Commencement Assertion | KU-02.05 | SA-02.04 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-024 |
| ER-02.06 | SA-02.06 — Status Continuation Assertion | KU-02.06 | SA-02.04, SA-02.05 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-025 |
| ER-02.07 | SA-02.07 — Status Cessation Assertion | KU-02.07 | SA-02.04, SA-02.06 | IN-CSM-001, IN-CSM-002, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-026 |

### 9.3 KF-03 — Business Group

**Governed inputs:** IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-03.01 | SA-03.01 — Business Group Assertion | KU-03.01 | None | IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-030 |
| ER-03.02 | SA-03.02 — Business Group Member Assertion | KU-03.02 | SA-03.01 | IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-031 |
| ER-03.03 | SA-03.03 — Control Relationship Assertion | KU-03.03 | SA-03.01, SA-03.02 | IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-032 |
| ER-03.04 | SA-03.04 — Controlling Person Assertion | KU-03.04 | SA-03.03 | IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-033 |
| ER-03.05 | SA-03.05 — Business Group Identity Assertion | KU-03.05 | SA-03.01 | IN-CSM-001, IN-EF-002, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-034 |

### 9.4 KF-04 — Business Group Reporting Group

**Governed inputs:** IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-04.01 | SA-04.01 — Candidate Business Group Reporting Group Assertion | KU-04.01 | SA-03.01 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-040 |
| ER-04.02 | SA-04.02 — Designated Service Member Assertion | KU-04.02 | SA-04.01, SA-02.02 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-041 |
| ER-04.03 | SA-04.03 — Reporting Entity Decline Notice Assertion | KU-04.03 | SA-04.01 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-042 |
| ER-04.04 | SA-04.04 — Notice Delivery Sufficiency Assertion | KU-04.04 | SA-04.03 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-043 |
| ER-04.05 | SA-04.05 — Decline Withdrawal Assertion | KU-04.05 | SA-04.03 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-044 |
| ER-04.06 | SA-04.06 — Business Group Ineligibility Assertion | KU-04.06 | SA-04.03, SA-04.04, SA-04.05 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-045 |
| ER-04.07 | SA-04.07 — Business Group Reporting Group Operating Condition Assertion | KU-04.07 | SA-04.01, SA-04.02, SA-04.06, SA-07.15, SA-08.07 | IN-CSM-002, IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-046 |

### 9.5 KF-05 — Elected Reporting Group

**Governed inputs:** IN-EF-002, IN-EF-003, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-05.01 | SA-05.01 — Candidate Elected Reporting Group Assertion | KU-05.01 | None | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-050 |
| ER-05.02 | SA-05.02 — Candidate Member Assertion | KU-05.02 | SA-05.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-051 |
| ER-05.03 | SA-05.03 — Membership Eligibility Assertion | KU-05.03 | SA-05.02 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-052 |
| ER-05.04 | SA-05.04 — Written Election Assertion | KU-05.04 | SA-05.02 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-053 |
| ER-05.05 | SA-05.05 — Collective Election Assertion | KU-05.05 | SA-05.01, SA-03.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-054 |
| ER-05.06 | SA-05.06 — Collective Member Consent Assertion | KU-05.06 | SA-05.05 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-055 |
| ER-05.07 | SA-05.07 — Business Group Collective Participation Assertion | KU-05.07 | SA-05.05, SA-05.06, SA-03.02 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-056 |
| ER-05.08 | SA-05.08 — Later Admission Assertion | KU-05.08 | SA-05.01, SA-05.03 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-057 |
| ER-05.09 | SA-05.09 — Lead Entity Consent to Join Assertion | KU-05.09 | SA-05.08, SA-07.16 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-058 |
| ER-05.10 | SA-05.10 — Automatic Admission Assertion | KU-05.10 | SA-05.07, SA-03.02 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-059 |
| ER-05.11 | SA-05.11 — Member Withdrawal Assertion | KU-05.11 | SA-05.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-060 |

### 9.6 KF-06 — Reporting Group Membership

**Governed inputs:** IN-EF-002, IN-EF-003, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-06.01 | SA-06.01 — Candidate Membership Assertion | KU-06.01 | SA-04.01, SA-05.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-060 |
| ER-06.02 | SA-06.02 — Membership Basis Assertion | KU-06.02 | SA-06.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-061 |
| ER-06.03 | SA-06.03 — Membership Commencement Assertion | KU-06.03 | SA-06.01, SA-06.02 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-062 |
| ER-06.04 | SA-06.04 — Membership Cessation Assertion | KU-06.04 | SA-06.03, SA-05.11 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-063 |
| ER-06.05 | SA-06.05 — Multiple Membership Assertion | KU-06.05 | SA-06.01 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-064 |
| ER-06.06 | SA-06.06 — Membership Precedence Assertion | KU-06.06 | SA-06.05 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-065 |
| ER-06.07 | SA-06.07 — Displaced Membership Assertion | KU-06.07 | SA-06.06 | IN-EF-002, IN-EF-003, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-066 |

### 9.7 KF-07 — Lead Entity Specification

**Governed inputs:** IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-07.01 | SA-07.01 — Candidate Lead Entity Assertion | KU-07.01 | SA-06.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-070 |
| ER-07.02 | SA-07.02 — Business Group Member Agreement Assertion | KU-07.02 | SA-07.01, SA-04.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-071 |
| ER-07.03 | SA-07.03 — Controlling Person Appointment Assertion | KU-07.03 | SA-07.01, SA-03.04 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-072 |
| ER-07.04 | SA-07.04 — Elected Group Lead Entity Agreement Assertion | KU-07.04 | SA-07.01, SA-05.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-073 |
| ER-07.05 | SA-07.05 — Control Independence Assertion | KU-07.05 | SA-07.01, SA-03.03 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-074 |
| ER-07.06 | SA-07.06 — Policy Development Capability Assertion | KU-07.06 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-075 |
| ER-07.07 | SA-07.07 — Policy Development Authority Assertion | KU-07.07 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-076 |
| ER-07.08 | SA-07.08 — Policy Decision Authority Assertion | KU-07.08 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-077 |
| ER-07.09 | SA-07.09 — Included Business Group Connection Assertion | KU-07.09 | SA-07.01, SA-05.07 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-078 |
| ER-07.10 | SA-07.10 — Australian Incorporated Body Connection Assertion | KU-07.10 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-079 |
| ER-07.11 | SA-07.11 — Registered Foreign Company Connection Assertion | KU-07.11 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-080 |
| ER-07.12 | SA-07.12 — Australian-Resident Trustee Connection Assertion | KU-07.12 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-081 |
| ER-07.13 | SA-07.13 — Australian-Resident Person Connection Assertion | KU-07.13 | SA-07.01 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-082 |
| ER-07.14 | SA-07.14 — Lead Entity Identity Assertion | KU-07.14 | SA-07.10, SA-07.11, SA-07.12, SA-07.13 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-083 |
| ER-07.15 | SA-07.15 — Lead Entity Commencement Assertion | KU-07.15 | SA-07.01, SA-07.02, SA-07.03, SA-07.05, SA-07.06, SA-07.07, SA-07.14 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-084 |
| ER-07.16 | SA-07.16 — Lead Entity Cessation Assertion | KU-07.16 | SA-07.01, SA-07.04, SA-07.05, SA-07.08, SA-07.09, SA-07.14 | IN-CSM-001, IN-CSM-002, IN-EF-002, IN-EF-003, IN-EF-004, IN-AK-001, IN-ERM-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-085 |

### 9.8 KF-08 — Reporting Group Lifecycle

**Governed inputs:** IN-EF-003, IN-EF-004, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-08.01 | SA-08.01 — Reporting Group Active Assertion | KU-08.01 | SA-04.07, SA-05.01, SA-07.15, SA-07.16 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-080 |
| ER-08.02 | SA-08.02 — Lead Entity Vacancy Assertion | KU-08.02 | SA-08.01 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-081 |
| ER-08.03 | SA-08.03 — Vacancy Commencement Assertion | KU-08.03 | SA-08.02 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-082 |
| ER-08.04 | SA-08.04 — Previous Lead Entity Assertion | KU-08.04 | SA-08.02, SA-07.15, SA-07.16 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-083 |
| ER-08.05 | SA-08.05 — Replacement Lead Entity Assertion | KU-08.05 | SA-08.02, SA-07.15, SA-07.16 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-084 |
| ER-08.06 | SA-08.06 — Vacancy Duration Assertion | KU-08.06 | SA-08.03 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-085 |
| ER-08.07 | SA-08.07 — Permitted Vacancy Assertion | KU-08.07 | SA-08.06 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-086 |
| ER-08.08 | SA-08.08 — Reporting Group Continuation Assertion | KU-08.08 | SA-08.02, SA-08.07 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-087 |
| ER-08.09 | SA-08.09 — Reporting Group Cessation Assertion | KU-08.09 | SA-08.01, SA-08.07 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-088 |
| ER-08.10 | SA-08.10 — Reporting Group Reactivation Assertion | KU-08.10 | SA-08.09 | IN-EF-003, IN-EF-004, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-089 |

### 9.9 KF-09 — Responsibility Attribution

**Governed inputs:** IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-09.01 | SA-09.01 — Partnership Obligation Attribution Assertion | KU-09.01 | SA-01.02 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-090 |
| ER-09.02 | SA-09.02 — Partner Discharge Capacity Assertion | KU-09.02 | SA-09.01 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-091 |
| ER-09.03 | SA-09.03 — Association Committee Obligation Attribution Assertion | KU-09.03 | SA-01.03 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-092 |
| ER-09.04 | SA-09.04 — Committee Member Discharge Capacity Assertion | KU-09.04 | SA-09.03 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-093 |
| ER-09.05 | SA-09.05 — Trustee Obligation Attribution Assertion | KU-09.05 | SA-01.04 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-094 |
| ER-09.06 | SA-09.06 — Trustee Discharge Capacity Assertion | KU-09.06 | SA-09.05 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-095 |
| ER-09.07 | SA-09.07 — Attribution Role Assertion | KU-09.07 | SA-09.01, SA-09.03, SA-09.05 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-096 |
| ER-09.08 | SA-09.08 — Attribution Commencement Assertion | KU-09.08 | SA-09.07 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-097 |
| ER-09.09 | SA-09.09 — Attribution Cessation Assertion | KU-09.09 | SA-09.07 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-098 |
| ER-09.10 | SA-09.10 — Effective Attribution Period Assertion | KU-09.10 | SA-09.08, SA-09.09 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-099 |

### 9.10 KF-10 — Legislative Identity Continuity

**Governed inputs:** IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-10.01 | SA-10.01 — Partnership Composition Change Assertion | KU-10.01 | SA-01.02 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-100 |
| ER-10.02 | SA-10.02 — Partnership Continuity Assertion | KU-10.02 | SA-10.01 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-101 |
| ER-10.03 | SA-10.03 — Continuous Partnership Legislative Person Assertion | KU-10.03 | SA-10.02 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-102 |
| ER-10.04 | SA-10.04 — Reporting Entity Status Continuity Concept Assertion | KU-10.04 | SA-10.03, SA-02.04 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-103 |
| ER-10.05 | SA-10.05 — Partner Attribution Transition Assertion | KU-10.05 | SA-10.01, SA-09.01 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-104 |
| ER-10.06 | SA-10.06 — Partnership Membership History Assertion | KU-10.06 | SA-10.01 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-105 |
| ER-10.07 | SA-10.07 — Continuity Lineage Assertion | KU-10.07 | SA-10.02, SA-10.03, SA-10.06 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-106 |
| ER-10.08 | SA-10.08 — Non-Partnership Continuity Boundary Assertion | KU-10.08 | SA-01.03, SA-01.04, SA-10.02 | IN-CSM-001, IN-EF-001, IN-EF-005, IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-107 |

### 9.11 KF-11 — Legislative Source and Traceability Model

**Governed inputs:** IN-AK-001

| Rule ID | Assertion | Authoritative Knowledge | Dependencies | Governed Inputs | Deterministic Result | Traceability |
|---|---|---|---|---|---|---|
| ER-11.01 | SA-11.01 — Source Version Register Assertion | KU-11.01 | None | IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-110 |
| ER-11.02 | SA-11.02 — Recovery Traceability Register Assertion | KU-11.02 | None | IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-111 |
| ER-11.03 | SA-11.03 — Legislative Boundary Register Assertion | KU-11.03 | None | IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-112 |
| ER-11.04 | SA-11.04 — Legislative Change Impact Register Assertion | KU-11.04 | None | IN-AK-001 | Apply the Knowledge Unit to the qualified subject and effective-period inputs; assign an explicit contract resolution state under ER-COM-001–006. | EA-T04-LSTM-TR-113 |

## 10. Package-Level Determination Rules

### 10.1 Legislative Person Resolution

| Rule ID | Deterministic rule | Output |
|---|---|---|
| ER-AGG-001 | Resolve the applicable ordinary-person or special statutory-person treatment and establish one governed Enterprise–Legislative Person correspondence. Mutually incompatible treatments for the same subject and period produce Unresolved. | Legislative Person assertion set |

### 10.2 Reporting Entity Establishment Pathways

| Rule ID | Deterministic rule | Output |
|---|---|---|
| ER-AGG-002 | Establish the Designated Service Provider pathway where at least one authoritative EA-T03 Designated Service determination applies to the resolved Legislative Person for the determination period. | SA-02.02 |
| ER-AGG-003 | Establish the Lead Entity pathway where a valid Reporting Group and effective Lead Entity relationship are established for the resolved Legislative Person. | SA-02.03 |
| ER-AGG-004 | Reporting Entity establishment is Established where either pathway is Established; Explicitly Absent where every applicable pathway is Explicitly Absent; Unresolved where none is Established and at least one material pathway is Unresolved or Unsupported by Facts. | SA-02.04 and contract aggregate |

### 10.3 Reporting Group and Lead Entity

| Rule ID | Deterministic rule | Output |
|---|---|---|
| ER-AGG-005 | Apply the Business Group Reporting Group conditions to the resolved Business Group, decline-notice state, Designated Service member state, Lead Entity state and lifecycle constraints. | Business Group Reporting Group assertion set |
| ER-AGG-006 | Apply the Elected Reporting Group election, eligibility, collective-participation, admission, withdrawal and Lead Entity conditions. | Elected Reporting Group assertion set |
| ER-AGG-007 | Resolve candidate memberships through the statutory precedence rule while preserving displaced relationships in lineage. | Reporting Group Membership assertion set |
| ER-AGG-008 | Apply the applicable Business Group or Elected Group Lead Entity conditions without substituting one test for the other. | Lead Entity assertion set |

### 10.4 Lifecycle

| Rule ID | Deterministic rule | Output |
|---|---|---|
| ER-AGG-009 | A Reporting Group with a ceased Lead Entity and no replacement enters Lead Entity Vacancy from the effective cessation time. | SA-08.02 and SA-08.03 |
| ER-AGG-010 | A continuous Lead Entity vacancy not exceeding 28 days satisfies Permitted Vacancy; a vacancy exceeding 28 continuous days does not. | SA-08.06 and SA-08.07 |
| ER-AGG-011 | Temporary Reporting Group continuation may be established during a permitted vacancy; the former Lead Entity role remains ceased. | SA-08.08 |

### 10.5 Responsibility Attribution and Continuity

| Rule ID | Deterministic rule | Output |
|---|---|---|
| ER-AGG-012 | Apply the attribution rule corresponding to the resolved statutory-person treatment and current role population. Do not substitute the attributed person for the Reporting Entity subject. | KF-09 assertion set |
| ER-AGG-013 | Apply partnership continuity to preserve the same Partnership Legislative Person across composition changes while separately updating partner-attribution effective periods. | KF-10 assertion set |
| ER-AGG-014 | Do not extend partnership continuity to trusts or unincorporated associations without a separate authoritative basis. | SA-10.08 |

## 11. Evaluation Dependencies and Ordering

Evaluation SHALL respect the assertion dependency graph declared by the Semantic Assertion Contract. An assertion SHALL not be evaluated as Established where a mandatory dependency is Unresolved, Unsupported by Facts or Deferred, unless a specific governed rule makes that dependency immaterial to the result.

Recommended deterministic order:

1. KF-11 source and traceability validity.
2. KF-01 Legislative Person Resolution.
3. KF-03 Business Group.
4. KF-04 and KF-05 Reporting Group formation concepts.
5. KF-06 Reporting Group Membership.
6. KF-07 Lead Entity Specification.
7. KF-08 Reporting Group Lifecycle.
8. KF-02 Reporting Entity Establishment.
9. KF-09 Responsibility Attribution.
10. KF-10 Legislative Identity Continuity.

## 12. Pattern, Composition and Aggregate Sufficiency

Evaluation SHALL calculate semantic sufficiency against the pattern instantiations, compositions and aggregates declared by the Semantic Assertion Contract.

| Sufficiency Level | Evaluation requirement |
|---|---|
| Assertion | Every applicable assertion has an explicit resolution state. |
| Pattern Instantiation | Every Required assertion and every applicable Conditional assertion in the pattern is resolved in a contract-permitted state. |
| Composition | Every constituent pattern is sufficient and all composition dependencies are eligible. |
| Aggregate | Every mandatory composition is sufficient for the determination period. |
| Canonical Model Eligibility | The Reporting Entity Determination aggregate is sufficient and no blocking Unresolved, Unsupported by Facts or Deferred assertion remains. |

## 13. Transformation Eligibility

Evaluation SHALL declare the assertion set **Eligible for Semantic Compilation** only when:

- every Required assertion is resolved;
- every applicable Conditional assertion is resolved;
- Not Applicable is governed through participation and is not treated as missing;
- all dependency and temporal constraints are satisfied;
- the Reporting Entity Determination aggregate is semantically sufficient;
- canonical identity, attachment scope and lineage are complete.

Evaluation SHALL declare the assertion set **Not Eligible for Semantic Compilation** where any blocking assertion is Unresolved, Unsupported by Facts or Deferred, or where required lineage is absent.

## 14. Legislative Traceability Reference

This specification does not reproduce provision-level legislative mappings. Each evaluation result references the authoritative Knowledge Unit and traceability identifier maintained in the EA-T04 Knowledge Architecture Legislative Source and Traceability Model.

Required lineage chain:

```text
Evaluation Result
↓
Evaluation Rule
↓
Semantic Assertion
↓
Knowledge Unit
↓
Traceability Identifier
↓
Authoritative Legislative Provision
```

## 15. Validation

| Validation | Requirement | Result |
|---|---|---|
| Determinism | Same governed inputs and versions produce the same assertion results. | PASS |
| Rule identity | Every result identifies a stable evaluation rule. | PASS |
| Knowledge authority | Every rule references an authoritative Knowledge Unit. | PASS |
| Fact authority | Every factual input retains its declared source and lineage. | PASS |
| Conflict handling | Conflicts produce explicit governed states. | PASS |
| Insufficiency handling | Missing and indeterminate facts are distinguished. | PASS |
| Attachment scope | Result attachment is inherited and preserved. | PASS |
| Temporal scope | Effective-period evaluation is explicit. | PASS |
| No hidden facts | No undeclared fact source is permitted. | PASS |
| No knowledge redefinition | Evaluation applies but does not redefine knowledge. | PASS |
| No compilation | No canonical-model transformation is performed. | PASS |

## 16. Standards Conformance Report

| SA-SES requirement | Implementation | Evidence | Result |
|---|---|---|---|
| Expert knowledge and authoritative facts establish assertions | Governed input and rule catalogues | Sections 4, 9 and 10 | PASS |
| Identical versions and facts produce identical results | Determinism rule | Section 7.1 | PASS |
| Every result identifies rule, facts and knowledge | Evaluation Result Model | Section 5 | PASS |
| Conflict, insufficiency and non-applicability explicit | Common Resolution Rules | Sections 6 and 7 | PASS |
| Attachment and temporal scope preserved | Result fields and temporal rules | Sections 5 and 7.4 | PASS |
| No hidden facts or ungoverned reasoning | Input catalogue and prohibitions | Sections 3, 4 and 15 | PASS |
| Does not acquire facts | Boundary declaration | Section 3.2 | PASS |
| Does not compile canonical model | Boundary declaration and eligibility-only output | Sections 3.2 and 13 | PASS |

## 17. Document Status

| Property | Value |
|---|---|
| Status | Candidate |
| Semantic Completeness | Complete for the EA-T04 assertion catalogue |
| Evaluation Rule Coverage | 90 assertion rules plus common and aggregate rules |
| Input Coverage | All governed inputs declared by EA-T04-SIP |
| Standards Conformance | PASS |
| Legislative Traceability | Referenced through EA-T04 Knowledge Architecture |
| Open Issues | None identified for Candidate publication |
| Promotion Condition | Review against the frozen Knowledge Architecture, Assertion Contract and Input Pattern; then promote to Frozen Candidate |
