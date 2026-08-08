# ECF Operating Model

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Operating Model
**Last Updated:** August 2026

---

## 1. Purpose

The Evidence Convergence Framework (ECF) provides an evidence-centric operating model for AI vendor governance.

This document translates the ECF concepts and design principles into an operational lifecycle that an organization can use to assess an AI vendor, manage governance evidence, map that evidence across multiple requirements, identify gaps, and support risk decisions.

The operating model is designed to demonstrate how a single evidence-centric assessment can support multiple governance requirements without treating those requirements as interchangeable.

The reference implementation demonstrates the model across:

* NIST AI Risk Management Framework (AI RMF)
* ISO/IEC 42001
* European Union Artificial Intelligence Act (EU AI Act)

---

# 2. Operating Model Overview

The ECF operating model consists of eight interconnected stages:

```text
┌─────────────────────────────────────────────────────────────┐
│                    ECF OPERATING MODEL                      │
└─────────────────────────────────────────────────────────────┘

  1. Vendor & AI Intake
              ↓
  2. Scope & Requirement Identification
              ↓
  3. Evidence Requirement Design
              ↓
  4. Evidence Collection
              ↓
  5. Evidence Validation
              ↓
  6. Cross-Framework Evidence Mapping
              ↓
  7. Gap, Risk & Remediation Analysis
              ↓
  8. Reporting & Continuous Evidence Governance
              │
              └──────────────────────────────┐
                                             ↓
                                  Evidence Lifecycle
                                  & Reuse
```

The lifecycle is iterative rather than strictly linear.

New requirements, changes to an AI system, evidence expiration, material findings, or regulatory changes may trigger reassessment.

---

# 3. Stage 1 — Vendor & AI Intake

The process begins by establishing what is being assessed.

The intake process should identify:

* Vendor
* Product or service
* AI system or capability
* Business owner
* Intended use
* Deployment model
* Data involved
* Business criticality
* Geographic scope
* Regulatory exposure
* Existing contractual requirements

A simplified intake relationship is:

```text
Vendor
   ↓
Product / Service
   ↓
AI Capability
   ↓
Business Use Case
```

The purpose is to prevent evidence from being collected before the organization understands the object and context of the assessment.

### Primary Outputs

* AI Vendor Inventory record
* AI system / service profile
* Business owner
* Initial risk classification
* Assessment trigger

---

# 4. Stage 2 — Scope & Requirement Identification

The organization determines which governance requirements apply to the vendor and AI system.

Potential sources include:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act
* Internal AI governance policies
* Information security requirements
* Privacy requirements
* Contractual requirements
* Sector-specific requirements

The process should distinguish between:

```text
Applicable Requirement
        ↓
Assessment Scope
        ↓
Evidence Requirement
```

Not every requirement will apply to every vendor.

Applicability should therefore be determined before evidence collection begins.

### Primary Outputs

* Assessment scope
* Applicable frameworks
* Applicable requirements
* Framework-specific applicability decisions
* Initial evidence requirement set

---

# 5. Stage 3 — Evidence Requirement Design

Once applicable requirements are identified, the organization determines what evidence is needed to evaluate those requirements.

The focus should be on **evidence needs**, rather than immediately creating separate framework-specific questionnaires.

For example:

```text
Requirement
    ↓
What must be demonstrated?
    ↓
What evidence would demonstrate it?
    ↓
Can existing evidence satisfy the need?
```

A single evidence requirement may support multiple frameworks.

Example:

```text
Evidence Requirement:
Documented AI Risk Assessment

             │
      ┌──────┼──────┐
      ↓      ↓      ↓
    NIST   ISO    EU AI Act
```

The relationship does not imply identical requirements.

It identifies a potential common evidence asset.

### Primary Outputs

* Evidence Requirement Catalog
* Evidence types
* Evidence attributes
* Initial framework mappings
* Evidence collection strategy

---

# 6. Stage 4 — Evidence Collection

Evidence is requested from the vendor or obtained from existing internal sources.

Possible evidence sources include:

* Vendor policies
* Procedures
* Risk assessments
* System documentation
* Technical reports
* Testing results
* Certifications
* Audit reports
* Contracts
* Governance records
* Monitoring records
* Incident records
* Training records
* Other appropriate documentation

The organization should first determine whether acceptable evidence already exists before requesting new evidence.

```text
Evidence Requirement
        ↓
Existing Evidence Available?
       / \
     Yes   No
      ↓     ↓
 Validate   Request
      │     │
      └──┬──┘
         ↓
   Evidence Record
```

This is one of the principal mechanisms through which ECF reduces unnecessary duplication.

### Primary Outputs

* Evidence assets
* Evidence metadata
* Source information
* Collection records
* Vendor responses where applicable

---

# 7. Stage 5 — Evidence Validation

Received evidence should be evaluated before being treated as reusable.

Validation should consider:

* Authenticity
* Relevance
* Completeness
* Currency
* Scope
* Reliability
* Applicability
* Consistency

A useful validation sequence is:

```text
Evidence Received
       ↓
Authenticity Check
       ↓
Scope Check
       ↓
Currency Check
       ↓
Relevance Check
       ↓
Sufficiency Assessment
       ↓
Validation Decision
```

Possible validation outcomes include:

| Status                    | Meaning                                                       |
| ------------------------- | ------------------------------------------------------------- |
| Validated                 | Evidence is suitable for the intended assessment use          |
| Validated with Limitation | Evidence may be used subject to documented limitations        |
| Insufficient              | Evidence does not adequately address the intended requirement |
| Invalid                   | Evidence cannot reasonably be relied upon                     |
| Pending                   | Additional information or review is required                  |

Validation is requirement-specific.

Evidence validated for one purpose may require additional evaluation before being reused for another.

### Primary Outputs

* Validation status
* Evidence quality assessment
* Limitations
* Reuse eligibility

---

# 8. Stage 6 — Cross-Framework Evidence Mapping

Validated evidence is mapped to applicable governance requirements.

The mapping process should answer:

> **Which requirements can this evidence meaningfully support?**

The relationship is:

```text
Evidence Asset
      ↓
Requirement
      ↓
Framework
      ↓
Assessment Interpretation
```

A single evidence asset may map to multiple frameworks.

```text
                  E-015
             AI Risk Assessment
                     │
          ┌──────────┼──────────┐
          ↓          ↓          ↓
       NIST AI RMF  ISO 42001  EU AI Act
```

However, each mapping should preserve:

* Requirement ID
* Framework
* Evidence ID
* Mapping rationale
* Evidence relevance
* Limitations
* Assessment status

### Mapping Outcomes

A reference implementation may use statuses such as:

| Mapping Status | Meaning                                             |
| -------------- | --------------------------------------------------- |
| Direct         | Evidence directly addresses the requirement         |
| Supporting     | Evidence provides meaningful supporting information |
| Partial        | Evidence addresses only part of the requirement     |
| Insufficient   | Evidence is related but inadequate                  |
| Not Applicable | Requirement does not apply                          |
| Gap            | Required evidence is not available                  |

### Primary Outputs

* Evidence Mapping Matrix
* Framework coverage view
* Reuse candidates
* Framework-specific evidence requirements

---

# 9. Stage 7 — Gap, Risk & Remediation Analysis

Mapping identifies where evidence supports requirements and where gaps remain.

A gap may arise because:

* Evidence is missing.
* Evidence is insufficient.
* Evidence is outdated.
* Evidence has inappropriate scope.
* Evidence only partially addresses the requirement.
* A requirement is inherently framework-specific.

The process is:

```text
Requirement
     ↓
Evidence Mapping
     ↓
Coverage Assessment
     ↓
Gap / Finding
     ↓
Risk Analysis
     ↓
Treatment Decision
```

A gap should not automatically be treated as a material risk.

Risk evaluation should consider organizational context, impact, likelihood, existing controls, and other relevant risk factors.

### Primary Outputs

* Gap Register
* Findings
* Risk Register entries
* Remediation actions
* Risk treatment decisions

---

# 10. Stage 8 — Reporting & Continuous Evidence Governance

The final stage converts assessment information into governance outputs.

Potential outputs include:

### Operational

* Evidence status
* Open evidence requests
* Evidence expiration
* Vendor remediation status

### Management

* Vendor risk profile
* Framework coverage
* Material gaps
* Remediation status
* Residual risk

### Assurance

* Requirement-to-evidence traceability
* Evidence provenance
* Validation records
* Assessment conclusions
* Audit trail

The evidence lifecycle then continues.

```text
Assessment Complete
       ↓
Evidence Remains Valid?
       ↓
      Yes
       ↓
Available for Reuse
       ↓
Periodic Review
       ↓
Revalidation / Update
```

This turns ECF from a point-in-time assessment mechanism into an ongoing evidence governance model.

---

# 11. The ECF Evidence Flow

The complete evidence flow can be represented as:

```text
┌───────────────────┐
│ Governance        │
│ Requirements      │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Evidence          │
│ Requirements      │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Evidence          │
│ Collection        │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Evidence          │
│ Validation        │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Evidence          │
│ Register          │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Cross-Framework   │
│ Mapping           │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Coverage &        │
│ Gap Analysis      │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Risk &            │
│ Remediation       │
└─────────┬─────────┘
          ↓
┌───────────────────┐
│ Reporting &       │
│ Governance        │
└─────────┬─────────┘
          │
          └───────────────► Evidence Reuse
                              │
                              └──► Future Assessments
```

---

# 12. Evidence Reuse Decision Process

Evidence reuse is a controlled decision rather than an automatic consequence of mapping.

A reuse decision should consider:

```text
Existing Evidence
       ↓
Same Vendor / Scope?
       ↓
Same or Compatible AI System?
       ↓
Current?
       ↓
Relevant?
       ↓
Sufficient?
       ↓
Validated for Intended Use?
       ↓
Reuse
```

Where any material condition is not satisfied, the organization should determine whether:

* Additional evidence is required.
* The evidence needs revalidation.
* The evidence can only be used as supporting evidence.
* The evidence should not be reused.

---

# 13. Roles and Responsibilities

ECF may be implemented across multiple organizational functions.

A representative responsibility model is:

| Activity              | TPRM | AI Governance | Security | Privacy | Business Owner | Compliance |
| --------------------- | ---- | ------------- | -------- | ------- | -------------- | ---------- |
| Vendor Intake         | A/R  | C             | C        | C       | R              | C          |
| AI Classification     | C    | A/R           | C        | C       | R              | C          |
| Assessment Scope      | R    | A             | C        | C       | C              | C          |
| Evidence Requirements | R    | A             | C        | C       | C              | C          |
| Evidence Collection   | A/R  | R             | C        | C       | C              | C          |
| Evidence Validation   | R    | A             | R        | R       | C              | C          |
| Framework Mapping     | C    | A/R           | C        | C       | C              | R          |
| Gap Analysis          | R    | A/R           | C        | C       | C              | C          |
| Risk Decision         | C    | R             | C        | C       | A              | C          |
| Remediation           | R    | R             | R        | R       | A              | C          |
| Ongoing Monitoring    | R    | A             | R        | R       | C              | C          |

**Legend:**

* **A** — Accountable
* **R** — Responsible
* **C** — Consulted

This is a reference model.

Organizations should adapt accountability according to their governance structure.

---

# 14. ECF Data Objects

The operating model relies on a small set of interconnected governance objects.

```text
Vendor
   │
   ├── AI System
   │       │
   │       └── Assessment
   │                │
   │                ├── Requirement
   │                │       │
   │                │       └── Evidence Requirement
   │                │
   │                ├── Evidence
   │                │       │
   │                │       └── Mapping
   │                │
   │                └── Finding
   │                        │
   │                        └── Risk
   │
   └── Contract / Relationship
```

The core objects are:

1. **Vendor**
2. **AI System / Service**
3. **Assessment**
4. **Requirement**
5. **Evidence Requirement**
6. **Evidence Asset**
7. **Evidence Mapping**
8. **Finding / Gap**
9. **Risk**
10. **Remediation Action**

These objects will be implemented through the practical repository artifacts.

---

# 15. Assessment Once, Evidence Reuse Across Frameworks

The operating model is designed around the following pattern:

```text
                    AI Vendor
                       │
                       ↓
               Single Assessment
                       │
                       ↓
                Evidence Set
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
       NIST AI RMF  ISO 42001   EU AI Act
          │            │            │
          └────────────┼────────────┘
                       ↓
             Common Evidence Base
                       │
              ┌────────┴────────┐
              ↓                 ↓
        Shared Evidence     Specific Gaps
              │                 │
              └────────┬────────┘
                       ↓
                 Risk Analysis
```

The "single assessment" concept does not mean that every framework requirement is evaluated identically.

It means that the organization seeks to establish a common evidence foundation from which requirement-specific assessments can be performed.

---

# 16. Trigger Conditions for Reassessment

ECF should support both scheduled and event-driven reassessment.

Potential triggers include:

* Evidence expiration
* Material vendor change
* AI system change
* New AI use case
* Material model change
* New deployment environment
* Significant security incident
* Significant AI incident
* Regulatory change
* Contract renewal
* Material risk change
* Failed remediation
* Significant change in data processing

A reassessment trigger should determine whether the organization needs:

* New evidence
* Evidence revalidation
* Requirement remapping
* Full reassessment
* Targeted reassessment

---

# 17. Continuous Evidence Governance

The long-term operating model is:

```text
Assess
  ↓
Collect
  ↓
Validate
  ↓
Map
  ↓
Reuse
  ↓
Monitor
  ↓
Review
  ↓
Update
  ↓
Reassess
```

This creates a managed evidence lifecycle rather than a series of disconnected assessment events.

The objective is to increase the value of previously collected evidence while preventing stale evidence from creating false assurance.

---

# 18. ECF Operating Model Outputs

A complete implementation should be capable of producing:

### Vendor-Level Outputs

* Vendor risk profile
* AI system inventory
* Assessment status
* Evidence status
* Open requests

### Evidence-Level Outputs

* Evidence Register
* Evidence lifecycle status
* Evidence quality
* Reuse eligibility
* Evidence provenance

### Framework-Level Outputs

* Mapping Matrix
* Framework coverage
* Framework-specific gaps
* Requirement-level assessment results

### Risk-Level Outputs

* Findings
* Risk Register
* Remediation actions
* Residual risk
* Risk acceptance decisions

### Executive-Level Outputs

* Vendor risk summary
* Material governance gaps
* Evidence reuse
* Assessment efficiency
* Remediation status
* Risk trends

---

# 19. Implementation Boundary

The operating model defines **how governance evidence should flow**.

It does not prescribe:

* A specific GRC platform
* A specific database
* A specific questionnaire format
* A specific risk scoring methodology
* A specific evidence retention period
* A specific organizational structure
* A specific automation technology

Those are implementation decisions.

The repository provides one practical reference implementation.

---

# 20. Summary

The ECF Operating Model translates the framework's conceptual principles into an operational lifecycle:

```text
Vendor & AI Intake
        ↓
Scope & Requirements
        ↓
Evidence Requirements
        ↓
Evidence Collection
        ↓
Evidence Validation
        ↓
Cross-Framework Mapping
        ↓
Gap & Risk Analysis
        ↓
Reporting & Governance
        ↓
Evidence Reuse
        ↓
Continuous Review
```

The central operating principle is:

> **Establish a common, validated evidence foundation once, then evaluate and reuse that evidence across applicable governance requirements while preserving framework-specific differences and risk decisions.**

ECF therefore creates a controlled bridge between:

```text
Governance Requirements
        ↓
Evidence
        ↓
Assessment
        ↓
Risk
        ↓
Decision
```

The remaining artifacts in this repository operationalize this model through concrete data structures, workbooks, mappings, workflows, and reporting examples.

