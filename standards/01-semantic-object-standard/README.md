---
id: SA-SOS
version: 1.0.0
status: Publication Candidate
authority: Normative
---

# Semantic Object Standard

## 1. Purpose

This standard defines the minimum normative content required to establish a Semantic Object as an architectural responsibility.

## 2. Required sections

| Section | Requirement |
|---|---|
| Catalogue entry | Stable identifier, name, version, status and authority. |
| Canonical question | The singular semantic question discharged by the object. |
| Responsibility | The semantic responsibility owned by the object. |
| High-level grammar | Constituent semantic components only. |
| Boundary | Meaning explicitly included and excluded. |
| Dependencies | Upstream and downstream semantic dependencies. |

## 3. Principles

| ID | Requirement |
|---|---|
| SO-P-001 | A Semantic Object SHALL own one coherent semantic responsibility. |
| SO-P-002 | It SHALL recover only the minimum semantic knowledge necessary to discharge that responsibility. |
| SO-P-003 | It SHALL NOT define Knowledge Units, acquisition behaviour or compiler rules. |
| SO-P-004 | It SHALL reference the package Semantic Specification for detailed meaning. |

## 4. Conformance

A Semantic Object conforms when its canonical question, responsibility, boundary and dependencies are explicit and do not duplicate content owned by downstream package specifications.
