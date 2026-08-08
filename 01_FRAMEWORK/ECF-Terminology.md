# ECF Terminology

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Controlled Vocabulary
**Last Updated:** August 2026

---

## 1. Purpose

This document establishes the controlled vocabulary for the Evidence Convergence Framework (ECF).

Consistent terminology is necessary because ECF distinguishes between concepts that are frequently conflated in traditional governance and compliance assessments.

In particular, ECF distinguishes between:

* Requirements
* Evidence requirements
* Evidence assets
* Evidence mappings
* Assessments
* Findings
* Gaps
* Risks
* Controls
* Frameworks
* Reuse
* Convergence

These terms should be used consistently throughout this repository.

Where an implementation uses different terminology, the implementation should document the relationship to the ECF terminology.

---

# 2. Core ECF Concepts

## 2.1 Evidence Convergence Framework (ECF)

An evidence-centric operating model for AI vendor governance that enables organizations to collect, validate, map, and appropriately reuse governance evidence across multiple requirements and frameworks.

ECF is **not** a competing regulatory or governance framework.

Its purpose is to improve the way governance evidence is managed and reused.

---

## 2.2 Evidence

Information or documentation that can provide support for evaluating whether a defined governance requirement has been addressed.

Examples include:

* Policies
* Procedures
* Risk assessments
* Audit reports
* Certifications
* Technical documentation
* Testing results
* Monitoring records
* Contracts
* Training records
* Governance records

Evidence has meaning only in relation to a defined assessment purpose or requirement.

---

## 2.3 Evidence Asset

A uniquely identifiable, governed instance of evidence maintained for potential use across one or more governance requirements.

An Evidence Asset is more than an uploaded document.

It includes metadata such as:

* Evidence ID
* Description
* Source
* Owner
* Scope
* Collection date
* Review date
* Validation status
* Lifecycle status
* Applicable mappings
* Limitations

**Example:**

```text
E-017
AI Risk Assessment Report
Vendor: ExampleAI
Scope: Production AI Platform
Status: Validated
Review Date: 2027-03-31
```

The Evidence Asset is the fundamental reusable object within ECF.

---

## 2.4 Evidence Requirement

A defined need for evidence associated with a governance requirement.

An Evidence Requirement answers:

> **What evidence would allow the organization to evaluate this requirement?**

An Evidence Requirement is not necessarily a questionnaire question.

**Example:**

```text
Evidence Requirement:
Documented AI risk assessment covering the assessed AI system,
its material risks, risk treatment, and responsible owners.
```

One Evidence Requirement may support multiple governance requirements.

---

## 2.5 Evidence Source

The origin from which an Evidence Asset was obtained.

Examples include:

* AI vendor
* Internal business unit
* Security team
* Privacy team
* External auditor
* Certification body
* Contract repository
* GRC platform

Source identifies where the evidence originated.

It does not necessarily identify who owns the underlying control.

---

## 2.6 Evidence Owner

The person or function accountable for maintaining, validating, or governing an Evidence Asset within the assessment process.

The Evidence Owner may differ from the Evidence Source.

---

## 2.7 Evidence Scope

The boundaries within which an Evidence Asset is considered applicable.

Scope may include:

* Vendor
* Product
* AI system
* Model
* Business process
* Geography
* Data environment
* Deployment environment
* Assessment period

Evidence should not be assumed to apply outside its defined scope.

---

## 2.8 Evidence Validation

The process of determining whether an Evidence Asset is sufficiently authentic, relevant, current, complete, reliable, and applicable for its intended assessment purpose.

Evidence validation does not automatically establish compliance.

---

## 2.9 Evidence Quality

The degree to which an Evidence Asset is suitable for supporting a particular governance assessment.

Relevant dimensions include:

* Authenticity
* Relevance
* Completeness
* Currency
* Scope
* Reliability
* Applicability
* Consistency

Evidence quality is contextual.

---

## 2.10 Evidence Lifecycle

The sequence through which an Evidence Asset is created, collected, validated, mapped, reused, reviewed, updated, superseded, or archived.

A representative lifecycle is:

```text
Required
   ↓
Requested
   ↓
Received
   ↓
Validated
   ↓
Mapped
   ↓
Available for Reuse
   ↓
Reviewed
   ↓
Updated / Superseded
   ↓
Archived
```

---

# 3. Governance and Framework Concepts

## 3.1 Governance Framework

A structured body of principles, requirements, practices, or guidance used to manage a particular governance domain.

Examples in this repository include:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act

ECF does not replace these frameworks.

It provides an evidence-management operating model that can support assessments against them.

---

## 3.2 Framework

A specific governance, regulatory, or standards-based structure against which requirements may be evaluated.

Within this repository, the principal frameworks are:

| Framework     | Type                       |
| ------------- | -------------------------- |
| NIST AI RMF   | Risk management framework  |
| ISO/IEC 42001 | Management system standard |
| EU AI Act     | Regulation                 |

These instruments differ in purpose, structure, terminology, and legal or normative status.

ECF preserves those differences.

---

## 3.3 Requirement

A defined expectation that must be evaluated within a particular governance, regulatory, contractual, or organizational context.

A Requirement should have a unique identifier where practical.

A requirement may originate from:

* A framework
* Regulation
* Internal policy
* Contract
* Standard
* Control objective

---

## 3.4 Framework Requirement

A Requirement originating from a specific external framework or regulatory instrument.

Examples include:

* NIST AI RMF requirement
* ISO/IEC 42001 requirement
* EU AI Act obligation

A Framework Requirement should retain its original context and identifier where possible.

---

## 3.5 Control

A policy, process, procedure, technical mechanism, organizational activity, or other measure designed to prevent, detect, mitigate, or manage a defined risk.

A control is **not the same thing as evidence**.

For example:

```text
Control:
AI systems undergo documented risk assessment.

Evidence:
Completed AI Risk Assessment Report.
```

The control describes what the organization does.

The evidence demonstrates what occurred or what exists.

---

## 3.6 Control Objective

A desired outcome that a control or set of controls is intended to achieve.

A control objective may be supported by multiple controls and multiple Evidence Assets.

---

## 3.7 Assessment

A structured evaluation of a vendor, AI system, control environment, or governance requirement against defined criteria.

An assessment may contain:

* Scope
* Requirements
* Evidence
* Evidence mappings
* Assessment interpretations
* Findings
* Risks
* Recommendations

An assessment is the **evaluation activity**.

It is not the evidence itself.

---

## 3.8 Assessment Scope

The defined boundaries of an assessment.

Scope determines what is included and excluded from the assessment.

---

## 3.9 Assessment Interpretation

The assessor's conclusion regarding what an Evidence Asset indicates when evaluated against a specific Requirement.

The distinction is:

```text
Evidence
   ↓
Requirement
   ↓
Assessment Interpretation
```

The interpretation should not alter the underlying Evidence Asset.

---

# 4. Mapping and Convergence Concepts

## 4.1 Evidence Mapping

The documented relationship between an Evidence Asset and a specific governance Requirement.

A mapping should identify:

* Evidence ID
* Requirement ID
* Framework
* Mapping status
* Mapping rationale
* Limitations where applicable

---

## 4.2 Mapping Status

The classification assigned to an Evidence-to-Requirement relationship.

The reference implementation uses:

| Status         | Definition                                               |
| -------------- | -------------------------------------------------------- |
| Direct         | Evidence directly addresses the requirement              |
| Supporting     | Evidence provides meaningful supporting information      |
| Partial        | Evidence addresses only part of the requirement          |
| Insufficient   | Evidence is relevant but inadequate                      |
| Gap            | Required supporting evidence is unavailable or deficient |
| Not Applicable | Requirement does not apply                               |

Mapping status should not be interpreted as a universal compliance rating.

---

## 4.3 Cross-Framework Mapping

The practice of mapping Evidence Assets to requirements originating from multiple governance frameworks.

Example:

```text
                  Evidence E-017
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
     NIST AI RMF   ISO/IEC 42001  EU AI Act
```

Cross-framework mapping identifies relationships between evidence and requirements.

It does not make the underlying frameworks equivalent.

---

## 4.4 Evidence Reuse

The controlled use of an existing Evidence Asset to support evaluation of an additional governance Requirement.

Reuse requires consideration of:

* Relevance
* Scope
* Currency
* Sufficiency
* Applicability
* Validation status
* Limitations

Evidence reuse is therefore a **decision**, not simply a document-sharing activity.

---

## 4.5 Reuse Eligibility

The determination that an Evidence Asset may reasonably be considered for reuse against another Requirement.

Eligibility does not guarantee that the evidence will satisfy the receiving requirement.

---

## 4.6 Evidence Convergence

The existence of legitimate overlap where a common Evidence Asset can support evaluation of multiple governance Requirements.

Convergence should be based on substantive evidentiary relationships.

It should not be manufactured to increase reuse metrics.

---

## 4.7 Appropriate Convergence

Convergence in which the relationship between an Evidence Asset and multiple Requirements is sufficiently relevant, defensible, and transparent.

ECF optimizes for **appropriate convergence**, not maximum convergence.

---

## 4.8 Framework-Specific Gap

A governance requirement for which existing common evidence does not provide sufficient support and additional evidence, activity, or assessment is required.

Framework-specific gaps are an expected outcome of ECF.

They demonstrate where convergence stops.

---

## 4.9 Evidence Convergence Ratio

A potential management metric representing the proportion of applicable evidence requirements that can be appropriately supported through existing reusable evidence.

A possible conceptual calculation is:

```text
Evidence Convergence Ratio =
Evidence Requirements Supported by Reusable Evidence
------------------------------------------------------
Total Applicable Evidence Requirements
```

This is an optional metric.

It should never be used as the sole measure of governance effectiveness.

---

# 5. Gap, Risk, and Remediation Concepts

## 5.1 Gap

A deficiency between a defined Requirement and the available evidence, control implementation, or governance practice needed to evaluate that Requirement adequately.

A gap may involve:

* Missing evidence
* Insufficient evidence
* Outdated evidence
* Inadequate scope
* Partial implementation
* Missing governance activity

A gap is not automatically a material risk.

---

## 5.2 Finding

A documented assessment observation indicating a deficiency, exception, weakness, inconsistency, or condition requiring attention.

A Finding may arise from:

* Evidence insufficiency
* Control deficiency
* Process weakness
* Documentation deficiency
* Governance inconsistency

Findings may or may not become formal risks.

---

## 5.3 Risk

The potential for an event or condition to affect the achievement of objectives.

Within ECF, assessment findings may become inputs into the organization's broader risk-management process.

The relationship is:

```text
Evidence
   ↓
Assessment
   ↓
Finding / Gap
   ↓
Risk Analysis
   ↓
Risk Decision
```

ECF does not prescribe a universal risk scoring methodology.

---

## 5.4 Residual Risk

The risk remaining after considering implemented controls and planned or completed risk treatments.

Residual risk should be evaluated using the organization's established risk methodology.

---

## 5.5 Risk Treatment

The action taken to address identified risk.

Potential treatments include:

* Mitigate
* Accept
* Transfer
* Avoid
* Escalate

Risk treatment is an organizational governance decision, not an automatic output of evidence mapping.

---

## 5.6 Remediation Action

A specific action intended to address a documented gap, finding, or risk treatment requirement.

A remediation action should ideally include:

* Action
* Owner
* Due date
* Status
* Expected outcome
* Verification method

---

# 6. Vendor and AI System Concepts

## 6.1 AI Vendor

A third-party organization that provides an AI-enabled product, service, model, platform, component, or capability to the organization.

The term may include:

* AI SaaS providers
* Model providers
* AI infrastructure providers
* AI platform providers
* AI-enabled software vendors
* AI service providers

---

## 6.2 AI System

A system that uses AI-related capabilities to perform defined functions or support decision-making.

The precise definition should follow the applicable governance or regulatory context.

The term should not be assumed to have identical meaning across NIST, ISO, EU regulatory, and organizational contexts.

---

## 6.3 AI Service

A service delivered by a vendor that incorporates AI capabilities.

An AI service may include:

* Models
* Applications
* APIs
* Infrastructure
* Managed services
* AI-enabled business processes

---

## 6.4 AI Use Case

The defined business purpose for which an AI system or AI service is used.

Use-case context can materially affect:

* Risk
* Applicability
* Required evidence
* Regulatory obligations
* Assessment scope

---

## 6.5 Vendor Risk Tier

A classification representing the relative level of risk associated with a vendor relationship.

Risk tiering may consider:

* Business criticality
* Data sensitivity
* AI use case
* Regulatory exposure
* Security risk
* Operational dependency
* Impact of failure

The specific scoring methodology is outside the scope of the ECF conceptual model.

---

# 7. Repository and Implementation Concepts

## 7.1 Evidence Register

A structured inventory of Evidence Assets and their associated metadata.

The Evidence Register is a core implementation artifact.

It should provide visibility into:

* What evidence exists
* Where it came from
* What it covers
* Whether it has been validated
* When it should be reviewed
* Where it is mapped
* Whether it can be reused

---

## 7.2 Evidence Mapping Matrix

A structured representation of relationships between Evidence Assets and governance Requirements.

It provides the primary cross-framework visibility within the reference implementation.

---

## 7.3 Evidence Requirement Catalog

A structured inventory of evidence needs associated with applicable governance Requirements.

It sits between governance requirements and collected evidence:

```text
Requirement
     ↓
Evidence Requirement
     ↓
Evidence Asset
```

---

## 7.4 Vendor Inventory

A structured inventory of AI vendors and associated products, services, and AI capabilities subject to governance.

It establishes the population from which assessments are initiated.

---

## 7.5 Assessment Workbook

A structured working artifact used to execute an assessment.

It may contain:

* Vendor information
* Assessment scope
* Requirements
* Evidence references
* Assessment results
* Findings
* Reviewer information
* Approval information

The workbook should reference Evidence Assets rather than duplicate evidence wherever practical.

---

## 7.6 Risk Register

A structured record of identified risks and their management status.

The Risk Register should reference findings and evidence where appropriate but remain logically distinct from the Evidence Register.

---

## 7.7 Crosswalk

A structured mapping between requirements, controls, evidence, or concepts across two or more frameworks.

In ECF, crosswalks should preferably operate through the Evidence layer rather than implying that frameworks are inherently equivalent.

---

## 7.8 Evidence Architecture

The logical structure governing how evidence is represented, related, stored, validated, mapped, reused, and maintained.

The Evidence Architecture is the foundation that enables ECF to function as an operating model rather than as a collection of questionnaires.

---

# 8. Important Distinctions

The following distinctions should be preserved throughout the repository.

| Do Not Conflate                    | Distinction                                                                               |
| ---------------------------------- | ----------------------------------------------------------------------------------------- |
| Evidence vs Control                | Evidence demonstrates or supports; a control describes an implemented measure             |
| Evidence vs Requirement            | Evidence supports evaluation; a requirement defines what must be evaluated                |
| Evidence vs Assessment             | Evidence is an input; assessment is the evaluation activity                               |
| Evidence vs Finding                | Evidence supports conclusions; a finding records an identified condition                  |
| Gap vs Risk                        | A gap is a deficiency; risk reflects potential impact                                     |
| Risk vs Remediation                | Risk describes exposure; remediation addresses the underlying condition                   |
| Mapping vs Compliance              | Mapping establishes evidentiary relevance; it does not automatically establish compliance |
| Reuse vs Equivalence               | Reusing evidence does not make two requirements equivalent                                |
| Convergence vs Compliance          | Evidence convergence does not establish regulatory or standards compliance                |
| Framework vs ECF                   | Frameworks establish governance requirements; ECF manages evidence across them            |
| Evidence Register vs Risk Register | Evidence manages governance evidence; risk register manages risk                          |
| Assessment vs Monitoring           | Assessment evaluates a defined scope; monitoring observes changes over time               |

---

# 9. ECF Relationship Model

The principal ECF objects can be represented as:

```text
┌───────────────┐
│    Vendor     │
└───────┬───────┘
        │
        ↓
┌───────────────┐
│   AI System   │
└───────┬───────┘
        │
        ↓
┌───────────────┐
│   Assessment  │
└───────┬───────┘
        │
        ↓
┌───────────────┐
│  Requirement  │
└───────┬───────┘
        │
        ↓
┌────────────────────┐
│ Evidence Requirement│
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│   Evidence Asset   │
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│ Evidence Mapping   │
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│ Assessment Result  │
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│ Finding / Gap      │
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│       Risk         │
└─────────┬──────────┘
          │
          ↓
┌────────────────────┐
│ Remediation /      │
│ Governance Decision│
└────────────────────┘
```

This relationship model should remain consistent with the repository's data structures and diagrams.

---

# 10. Terminology Governance

The terminology defined here should be treated as the repository's controlled vocabulary.

When adding new artifacts:

1. Prefer existing ECF terminology.
2. Do not introduce synonyms unnecessarily.
3. If an external framework uses different terminology, preserve the external term where required.
4. Clearly distinguish external terminology from ECF terminology.
5. Update this document when a new core ECF concept is introduced.
6. Ensure changes are reflected in dependent artifacts.

External frameworks may use terms differently.

For example, a term used by ISO/IEC 42001 should not automatically be assumed to have the same meaning under NIST AI RMF or the EU AI Act.

---

# 11. Core ECF Vocabulary at a Glance

| Term                  | Short Definition                                            |
| --------------------- | ----------------------------------------------------------- |
| ECF                   | Evidence-centric operating model for AI vendor governance   |
| Evidence              | Information supporting evaluation of a requirement          |
| Evidence Asset        | Governed, uniquely identifiable instance of evidence        |
| Evidence Requirement  | Defined need for evidence                                   |
| Evidence Source       | Origin of evidence                                          |
| Evidence Owner        | Accountable party for evidence governance                   |
| Evidence Scope        | Boundaries within which evidence applies                    |
| Evidence Validation   | Evaluation of evidence suitability                          |
| Evidence Lifecycle    | Management of evidence over time                            |
| Framework             | Governance, standards, or regulatory structure              |
| Requirement           | Defined expectation to be evaluated                         |
| Control               | Measure designed to manage risk                             |
| Assessment            | Structured evaluation against defined criteria              |
| Evidence Mapping      | Relationship between evidence and requirement               |
| Evidence Reuse        | Controlled use of existing evidence for another requirement |
| Evidence Convergence  | Legitimate overlap of evidence across requirements          |
| Gap                   | Deficiency relative to a requirement                        |
| Finding               | Documented assessment observation                           |
| Risk                  | Potential effect on objectives                              |
| Risk Treatment        | Action taken to address risk                                |
| Remediation           | Action intended to address a gap or finding                 |
| Crosswalk             | Mapping between frameworks or governance structures         |
| Evidence Architecture | Structure governing evidence relationships and lifecycle    |

---

# 12. Central Terminological Principle

The ECF vocabulary can be summarized through the following relationship:

```text
Framework
    ↓
Requirement
    ↓
Evidence Requirement
    ↓
Evidence Asset
    ↓
Evidence Mapping
    ↓
Assessment Interpretation
    ↓
Finding / Gap
    ↓
Risk
    ↓
Decision / Remediation
```

The central distinction is:

> **Requirements define what must be evaluated. Evidence provides the basis for evaluation. Assessments interpret that evidence. Risks and governance decisions determine what the organization does about the resulting conditions.**

Maintaining these distinctions is essential to preserving the integrity of the Evidence Convergence Framework.

