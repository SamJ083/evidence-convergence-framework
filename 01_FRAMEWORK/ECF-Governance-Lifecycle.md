# ECF Governance Lifecycle

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Governance Lifecycle
**Last Updated:** August 2026

---

## 1. Purpose

The Evidence Convergence Framework (ECF) Governance Lifecycle defines how evidence-centric AI vendor governance operates over time.

The lifecycle extends beyond the initial vendor assessment.

It establishes how an organization:

* Identifies governance requirements
* Determines assessment scope
* Defines evidence requirements
* Collects evidence
* Validates evidence
* Maps evidence across applicable requirements
* Identifies gaps
* Evaluates risk
* Determines remediation
* Makes governance decisions
* Monitors evidence over time
* Reuses evidence in subsequent governance activities
* Reassesses when conditions change

The lifecycle is designed to prevent ECF from becoming a point-in-time questionnaire exercise.

---

# 2. Lifecycle Overview

The ECF Governance Lifecycle consists of nine stages:

```text id="6x5vqs"
1. Identify
      ↓
2. Scope
      ↓
3. Define
      ↓
4. Collect
      ↓
5. Validate
      ↓
6. Map & Assess
      ↓
7. Treat & Decide
      ↓
8. Monitor & Maintain
      ↓
9. Reuse & Reassess
      │
      └──────────────────────► back to Identify
```

The lifecycle is continuous.

A completed assessment does not terminate governance responsibility.

---

# 3. Stage 1 — Identify

The organization identifies the vendor, AI system, service, or governance event requiring assessment.

### Typical Triggers

* New AI vendor
* New AI-enabled product
* New AI use case
* Procurement activity
* Vendor renewal
* Material vendor change
* New regulatory requirement
* Internal policy change
* AI incident
* Security incident
* Material risk change

### Key Questions

* What vendor or service is involved?
* What AI capability is being introduced or changed?
* Who owns the business relationship?
* Why is an assessment required?
* What changed since the previous assessment?

### Outputs

* Assessment trigger
* Vendor record
* AI system/service record
* Business owner
* Initial assessment classification

---

# 4. Stage 2 — Scope

The organization determines the boundaries of the assessment.

Scope should consider:

* Vendor
* Product/service
* AI system
* Use case
* Data
* Deployment environment
* Geography
* Regulatory jurisdiction
* Business process
* Assessment period
* Risk tier

The scope decision prevents evidence from being collected without understanding what the evidence is intended to cover.

### Outputs

* Assessment scope
* Applicable AI system
* Applicable business process
* Applicable jurisdictions
* Assessment period
* Initial risk tier

---

# 5. Stage 3 — Define

The organization identifies the governance requirements that apply to the assessment.

Potential requirements include:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act
* Internal AI governance requirements
* Information security requirements
* Privacy requirements
* Contractual obligations
* Sector-specific requirements

The organization then defines what evidence would be necessary to evaluate those requirements.

```text id="l3f1go"
Applicable Requirements
        ↓
Evidence Needs
        ↓
Evidence Requirements
```

### Outputs

* Applicable requirements
* Evidence Requirement Catalog
* Evidence types
* Initial evidence-to-requirement relationships

---

# 6. Stage 4 — Collect

The organization obtains the required evidence.

Evidence may come from:

* Existing enterprise repositories
* Prior assessments
* Vendor submissions
* Contracts
* Audit reports
* Certifications
* Policies
* Procedures
* Technical documentation
* Testing results
* Monitoring records
* Risk assessments

The first question should be:

> **Does acceptable evidence already exist?**

If yes, the organization should evaluate whether it can be reused before requesting additional evidence.

### Outputs

* Evidence assets
* Evidence metadata
* Source records
* Collection records
* Vendor responses

---

# 7. Stage 5 — Validate

Evidence is evaluated for suitability.

Validation considers:

* Authenticity
* Relevance
* Completeness
* Currency
* Scope
* Reliability
* Applicability
* Consistency

Possible outcomes include:

* Validated
* Validated with limitations
* Pending
* Insufficient
* Invalid

Validation should be documented rather than inferred from the existence of an uploaded document.

### Outputs

* Validation status
* Evidence quality assessment
* Limitations
* Reuse eligibility
* Review date

---

# 8. Stage 6 — Map & Assess

Validated evidence is mapped to applicable requirements.

The mapping process establishes:

```text id="xg8tqa"
Evidence
   ↓
Requirement
   ↓
Framework
   ↓
Assessment Interpretation
```

The evidence may support multiple requirements.

However, each requirement remains subject to its own assessment criteria.

### Mapping Outcomes

* Direct
* Supporting
* Partial
* Insufficient
* Gap
* Not Applicable

The organization then determines whether the evidence provides sufficient support for the requirement.

### Outputs

* Evidence Mapping Matrix
* Requirement coverage
* Framework-specific gaps
* Assessment results

---

# 9. Stage 7 — Treat & Decide

Identified gaps and findings are evaluated through the organization's risk-management process.

The lifecycle becomes:

```text id="xot2bf"
Evidence
    ↓
Assessment
    ↓
Gap / Finding
    ↓
Risk Analysis
    ↓
Treatment
    ↓
Governance Decision
```

Possible decisions include:

* Remediate
* Accept
* Mitigate
* Transfer
* Avoid
* Escalate
* Request additional evidence
* Restrict deployment
* Reject onboarding

The appropriate decision depends on organizational risk appetite and governance authority.

### Outputs

* Risk Register
* Remediation plan
* Risk treatment
* Risk acceptance
* Governance decision

---

# 10. Stage 8 — Monitor & Maintain

Evidence remains subject to lifecycle management after the assessment.

Monitoring should identify:

* Evidence expiration
* Material changes
* Control changes
* AI system changes
* Vendor changes
* New incidents
* Regulatory changes
* New use cases
* Failed remediation
* Changes in risk profile

The objective is to prevent stale evidence from creating false assurance.

### Outputs

* Evidence review events
* Updated evidence
* Monitoring records
* Change triggers
* Updated risk information

---

# 11. Stage 9 — Reuse & Reassess

Validated evidence may become a reusable enterprise asset.

When a new assessment or governance requirement arises:

```text id="8v9kzn"
New Requirement
       ↓
Existing Evidence?
      / \
    Yes  No
     ↓    ↓
 Validate  Collect
     │      │
     └──┬───┘
        ↓
     Assess
```

Reuse must remain conditional.

The organization should confirm:

* Relevance
* Scope
* Currency
* Sufficiency
* Applicability
* Validation status

Material changes may require reassessment.

---

# 12. Lifecycle Feedback Loops

The lifecycle contains several feedback loops.

### Evidence Loop

```text id="g2gq9b"
Evidence
   ↓
Validate
   ↓
Maintain
   ↓
Reuse
   ↓
Revalidate
```

### Risk Loop

```text id="z1j2x5"
Risk
 ↓
Treatment
 ↓
Monitoring
 ↓
Risk Change
 ↓
Reassessment
```

### Requirement Loop

```text id="2b8m9r"
Regulatory / Policy Change
        ↓
Requirement Review
        ↓
Evidence Requirement Update
        ↓
Assessment Update
```

These loops allow the governance model to adapt without rebuilding the entire assessment process.

---

# 13. Governance Decision Points

Not every lifecycle stage is purely operational.

Important governance decisions include:

| Decision Point | Typical Decision                  |
| -------------- | --------------------------------- |
| Intake         | Is assessment required?           |
| Scope          | What must be assessed?            |
| Applicability  | Which requirements apply?         |
| Evidence       | Is evidence sufficient?           |
| Mapping        | Can evidence be reused?           |
| Gap            | Is a deficiency material?         |
| Risk           | What is the risk level?           |
| Treatment      | What action is required?          |
| Acceptance     | Who may accept the residual risk? |
| Monitoring     | When must reassessment occur?     |

Decision authority should be assigned according to the organization's governance structure.

---

# 14. Lifecycle Roles

A representative governance model includes:

### Business Owner

Accountable for the business relationship and business risk.

### Third-Party Risk

Coordinates vendor assessment and relationship risk.

### AI Governance

Provides AI-specific governance requirements and oversight.

### Information Security

Evaluates cybersecurity and technical risk.

### Privacy

Evaluates applicable privacy requirements and data risks.

### Compliance / Legal

Provides regulatory interpretation and compliance oversight.

### Internal Audit

Provides independent assurance where applicable.

The specific allocation of responsibilities should be adapted to organizational structure.

---

# 15. Lifecycle Records

A mature implementation should maintain records for material lifecycle events.

Examples include:

* Assessment initiation
* Scope approval
* Evidence request
* Evidence receipt
* Evidence validation
* Mapping decision
* Gap identification
* Risk decision
* Remediation
* Evidence review
* Reassessment

These records support auditability and accountability.

---

# 16. Evidence Reuse Within the Lifecycle

Evidence reuse is embedded throughout the lifecycle rather than treated as a final-stage optimization.

At each evidence requirement, the organization should ask:

```text id="8a9g2q"
Does evidence already exist?
        ↓
Is it relevant?
        ↓
Is it current?
        ↓
Is its scope appropriate?
        ↓
Is it sufficiently reliable?
        ↓
Can it support this requirement?
```

Only then should reuse occur.

This creates a controlled reuse model rather than a document-sharing model.

---

# 17. Lifecycle Metrics

Organizations may measure lifecycle effectiveness through metrics such as:

### Efficiency

* Assessment cycle time
* Average evidence requests per vendor
* Duplicate evidence requests avoided
* Percentage of evidence reused

### Evidence Quality

* Evidence validation rate
* Evidence expiration rate
* Evidence deficiency rate
* Percentage of evidence with complete metadata

### Governance

* Requirement coverage
* Framework-specific gaps
* Open material findings
* Remediation aging
* Reassessment completion

### Vendor Experience

* Vendor response cycles
* Repeated evidence requests
* Assessment burden

Metrics should be used to improve governance, not to maximize reuse at the expense of assurance.

---

# 18. Lifecycle Exit Criteria

An assessment may be considered operationally complete when:

* Scope is established.
* Applicable requirements are identified.
* Required evidence has been collected or formally marked unavailable.
* Evidence has been evaluated.
* Applicable mappings are documented.
* Material gaps are identified.
* Risk has been evaluated.
* Required remediation or acceptance decisions are documented.
* Governance approval is complete.
* Monitoring requirements are established.

Completion does not mean that all gaps must be closed.

A risk may remain open subject to an approved treatment or acceptance decision.

---

# 19. Reassessment Triggers

Reassessment should be triggered when material conditions change.

Examples include:

* New AI capability
* Material model change
* Change in AI use case
* New data type
* Material data-processing change
* New geographic deployment
* Regulatory change
* Material security incident
* Material AI incident
* Vendor ownership change
* Significant control change
* Contract renewal
* Expired evidence
* Failed remediation
* Significant change in risk tier

The reassessment should be proportionate to the change.

A minor evidence refresh does not necessarily require a complete vendor reassessment.

---

# 20. Lifecycle Principle

The lifecycle can be summarized as:

```text id="lq3d4k"
IDENTIFY
   ↓
SCOPE
   ↓
DEFINE
   ↓
COLLECT
   ↓
VALIDATE
   ↓
MAP & ASSESS
   ↓
TREAT & DECIDE
   ↓
MONITOR & MAINTAIN
   ↓
REUSE & REASSESS
   │
   └───────────────────────► IDENTIFY
```

The central governance principle is:

> **AI vendor governance should manage evidence as a lifecycle rather than as a one-time assessment artifact.**

The purpose of the lifecycle is to create a durable governance process in which validated evidence can be reused appropriately while changes, limitations, gaps, and risk remain visible.

---

# 21. Relationship to the ECF Operating Model

The **ECF Operating Model** describes how an assessment operates.

The **ECF Governance Lifecycle** describes how that assessment and its evidence remain governed over time.

The relationship is:

```text id="8k0mzr"
ECF Operating Model
       ↓
Assessment Execution
       ↓
Evidence Creation / Validation
       ↓
ECF Governance Lifecycle
       ↓
Maintenance / Reuse / Reassessment
```

Together, the two documents define the operational foundation for the ECF reference implementation.

