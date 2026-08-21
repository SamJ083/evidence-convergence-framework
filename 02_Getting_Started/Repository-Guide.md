# ECF Repository Guide

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Repository Guide
**Last Updated:** August 2026

---

## 1. Purpose

This guide explains how to navigate and use the Evidence Convergence Framework (ECF) reference repository.

The repository is designed to serve three purposes:

1. Explain the ECF operating model.
2. Demonstrate how ECF can be operationalized for AI vendor governance.
3. Provide reusable reference artifacts that organizations can adapt to their own governance environments.

The repository is intentionally structured as an implementation reference rather than as a checklist library.

The central concept is:

> **Governance evidence should be designed and collected once, validated, mapped across applicable requirements, and reused wherever appropriate while preserving framework-specific gaps and decisions.**

---

# 2. Who Should Use This Repository?

The repository is intended for professionals involved in AI governance, third-party risk, cybersecurity, compliance, assurance, and enterprise risk management.

Primary audiences include:

* CISOs
* GRC leaders
* Third-Party Risk Management teams
* AI Governance professionals
* Risk consultants
* Internal Audit
* Compliance teams
* Enterprise architects
* Security architects
* Procurement and vendor management teams

Different users may enter the repository at different points depending on their objectives.

---

# 3. What This Repository Is

This repository is a **reference implementation of an evidence-centric AI vendor governance operating model**.

It demonstrates how an organization can:

```text id="8c0e2k"
Identify AI Vendor
       ↓
Define Requirements
       ↓
Define Evidence Needs
       ↓
Collect Evidence
       ↓
Validate Evidence
       ↓
Create Evidence Assets
       ↓
Map Evidence
       ↓
Assess Framework Requirements
       ↓
Identify Gaps
       ↓
Assess Risk
       ↓
Make Governance Decisions
       ↓
Reuse Evidence
```

The implementation uses three governance reference points:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act

The repository does not attempt to make these instruments equivalent.

---

# 4. What This Repository Is Not

This repository is not:

* A compliance certification.
* Legal advice.
* A substitute for regulatory interpretation.
* A universal AI governance framework.
* A replacement for NIST AI RMF.
* A replacement for ISO/IEC 42001.
* A replacement for the EU AI Act.
* A generic vendor questionnaire library.
* A claim that one piece of evidence automatically satisfies multiple requirements.
* A prescriptive implementation that every organization must follow.

The examples are intentionally illustrative and should be adapted before being used in a production environment.

---

# 5. Start Here

If you are new to ECF, follow this sequence:

```text id="l1yr8n"
01
Understand ECF
   ↓
02
Understand the Implementation Roadmap
   ↓
03
Read the Repository Guide
   ↓
04
Study the Evidence Architecture
   ↓
05
Review the Assessment Model
   ↓
06
Study Cross-Framework Mapping
   ↓
07
Follow the Reference Implementation
   ↓
08
Review Risk & Reporting
   ↓
09
Adapt the Implementation
```

Do not begin with the Excel workbooks.

The workbooks make more sense after understanding the evidence model and operating lifecycle.

---

# 6. Repository Structure

The repository is organized according to the implementation lifecycle.

```text id="f8q9xj"
ECF-Repository/
│
├── 01_Framework/
│
├── 02_Getting_Started/
│
├── 03_Evidence_Architecture/
│
├── 04_Assessment/
│
├── 05_Cross_Framework_Mapping/
│
├── 06_Reference_Implementation/
│
├── 07_Risk_and_Reporting/
│
├── 08_Implementation_Guide/
│
├── 09_Visuals/
│
└── README.md
```

Folder names may evolve as the repository develops.

The underlying dependency structure should remain:

```text id="j2brq6"
Framework
    ↓
Getting Started
    ↓
Evidence Architecture
    ↓
Assessment
    ↓
Cross-Framework Mapping
    ↓
Reference Implementation
    ↓
Risk & Reporting
    ↓
Implementation Guide
    ↓
Visuals
```

---

# 7. `01_Framework`

### Purpose

This folder establishes the conceptual foundation of ECF.

It explains what ECF is, how it operates, how governance evidence moves through its lifecycle, and which terminology should be used.

### Key Documents

| Document                      | Purpose                                    |
| ----------------------------- | ------------------------------------------ |
| `What-is-ECF.md`              | Defines the Evidence Convergence Framework |
| `ECF-Design-Principles.md`    | Establishes the design principles          |
| `ECF-Operating-Model.md`      | Explains how ECF operates                  |
| `ECF-Governance-Lifecycle.md` | Explains governance over time              |
| `ECF-Terminology.md`          | Establishes controlled vocabulary          |

### Read this folder if you want to understand:

> **What ECF is and how the model works.**

---

# 8. `02_Getting_Started`

### Purpose

This folder explains how to approach the repository and how an organization can progressively implement ECF.

### Key Documents

| Document                        | Purpose                                          |
| ------------------------------- | ------------------------------------------------ |
| `ECF-Implementation-Roadmap.md` | Defines the recommended implementation sequence  |
| `ECF-Repository-Guide.md`       | Explains how to navigate and use this repository |

### Read this folder if you want to understand:

> **How should I use this repository?**

---

# 9. `03_Evidence_Architecture`

### Purpose

This folder translates the ECF conceptual model into a concrete evidence architecture.

It should answer:

* What is an Evidence Asset?
* What metadata does it require?
* What is an Evidence Requirement?
* How is evidence validated?
* How is evidence governed over time?
* How is evidence made eligible for reuse?
* How are evidence objects related?

### Expected Artifacts

Examples include:

* Evidence Model
* Evidence Requirement Catalog
* Evidence Register
* Evidence Lifecycle
* Evidence Governance Model
* Evidence Metadata Specification

### Read this folder if you want to understand:

> **What exactly are we managing when we say "evidence"?**

---

# 10. `04_Assessment`

### Purpose

This folder demonstrates how ECF is applied during an AI vendor assessment.

Potential artifacts include:

* AI Vendor Inventory
* Vendor Risk Tiering
* Assessment Methodology
* Vendor Assessment Workbook
* Assessment Instructions
* Sample Assessment

The assessment should reference Evidence Assets rather than recreate the underlying evidence.

### Read this folder if you want to understand:

> **How does an ECF-enabled vendor assessment actually work?**

---

# 11. `05_Cross_Framework_Mapping`

### Purpose

This folder demonstrates evidence convergence across multiple governance frameworks.

The reference implementation focuses on:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act

Potential artifacts include:

* Framework requirement catalog
* Evidence Mapping Matrix
* Framework crosswalks
* Mapping rationale
* Framework-specific gap analysis

The central relationship is:

```text id="v5gy3x"
                    Evidence
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
       NIST AI RMF  ISO/IEC 42001  EU AI Act
          │            │            │
          └────────────┼────────────┘
                       ↓
               Common Evidence
                 + Specific Gaps
```

### Read this folder if you want to understand:

> **How can the same evidence support multiple governance requirements without pretending those requirements are identical?**

---

# 12. `06_Reference_Implementation`

### Purpose

This folder demonstrates ECF using a realistic but fictional organization and AI vendor.

The reference implementation should allow a reader to follow a complete assessment from beginning to end.

Potential components include:

* Sample organization
* Sample AI vendor
* AI system profile
* Vendor inventory record
* Assessment scope
* Evidence collection
* Evidence Register
* Completed assessment
* Evidence Mapping Matrix
* Findings
* Risk Register
* Remediation
* Final assessment output

### Read this folder if you want to understand:

> **What does ECF look like when applied to a real-world scenario?**

---

# 13. `07_Risk_and_Reporting`

### Purpose

This folder translates assessment and evidence results into risk and management outputs.

Potential artifacts include:

* Risk Register
* Assessment Report
* Executive Summary
* Findings Register
* Remediation Tracker
* Management Dashboard
* Evidence Coverage Analysis

The relationship is:

```text id="p8y7os"
Evidence
   ↓
Assessment
   ↓
Finding / Gap
   ↓
Risk
   ↓
Treatment
   ↓
Governance Decision
```

### Read this folder if you want to understand:

> **How does evidence ultimately support risk and executive decision-making?**

---

# 14. `08_Implementation_Guide`

### Purpose

This folder provides practical guidance for organizations adapting ECF to their own environment.

Potential topics include:

* Implementation prerequisites
* Governance roles
* Process design
* Evidence governance
* Tooling considerations
* GRC integration
* Operating model integration
* Implementation maturity
* Metrics
* Common implementation challenges
* Change management

### Read this folder if you want to understand:

> **How would I implement this in my organization?**

---

# 15. `09_Visuals`

### Purpose

This folder contains diagrams and visual representations of the ECF model.

Potential visuals include:

* ECF conceptual model
* Evidence lifecycle
* Evidence convergence model
* Operating model
* Governance lifecycle
* Evidence architecture
* Cross-framework mapping
* Assessment workflow
* Reuse decision flow
* Reference implementation architecture

Where appropriate, diagrams should be maintained in Mermaid so they remain version-controlled and editable.

---

# 16. Recommended Reading Paths

Different audiences can use different paths.

## Executive / CISO

Recommended:

```text id="q0k2yi"
What is ECF
    ↓
Design Principles
    ↓
Operating Model
    ↓
Reference Implementation
    ↓
Risk & Reporting
```

Focus:

* Governance efficiency
* Risk visibility
* Evidence reuse
* Assurance
* Executive decision-making

---

## GRC / TPRM Professional

Recommended:

```text id="8c7r0m"
What is ECF
    ↓
Operating Model
    ↓
Governance Lifecycle
    ↓
Evidence Architecture
    ↓
Assessment
    ↓
Cross-Framework Mapping
    ↓
Reference Implementation
```

Focus:

* Assessment process
* Evidence management
* Requirement mapping
* Vendor governance
* Risk treatment

---

## AI Governance Professional

Recommended:

```text id="8j1s0c"
What is ECF
    ↓
Design Principles
    ↓
Evidence Architecture
    ↓
Cross-Framework Mapping
    ↓
Reference Implementation
    ↓
Implementation Guide
```

Focus:

* AI governance requirements
* Evidence reuse
* Framework convergence
* AI vendor oversight

---

## Internal Audit / Assurance

Recommended:

```text id="1x5zqg"
Terminology
    ↓
Evidence Architecture
    ↓
Evidence Lifecycle
    ↓
Cross-Framework Mapping
    ↓
Assessment
    ↓
Risk & Reporting
```

Focus:

* Evidence provenance
* Traceability
* Validation
* Requirement coverage
* Auditability

---

## Enterprise Architect

Recommended:

```text id="5xq8la"
Operating Model
    ↓
Governance Lifecycle
    ↓
Evidence Architecture
    ↓
Reference Implementation
    ↓
Implementation Guide
```

Focus:

* Data objects
* Relationships
* Process architecture
* Integration
* Scalability

---

# 17. How to Use the Reference Artifacts

The repository contains different categories of artifacts.

### Conceptual Documents

These explain the ECF model.

Examples:

* Framework documents
* Operating model
* Governance lifecycle
* Terminology

These should be read before adapting implementation artifacts.

---

### Templates

Templates provide reusable structures without organization-specific data.

Examples:

* Evidence Register
* Assessment Workbook
* Risk Register
* Mapping Matrix

Templates should be copied and adapted rather than modified directly if they are intended to remain generic.

---

### Reference Data

Reference data demonstrates how a completed implementation might look.

Examples:

* Sample vendor
* Sample organization
* Sample evidence
* Completed assessment
* Sample findings

Reference data is fictional unless explicitly identified otherwise.

---

### Supporting Documentation

Supporting documentation explains how the artifacts work together.

Examples:

* Implementation Guide
* Workbook Instructions
* Methodology documents
* Process documentation

---

# 18. How to Follow an Assessment Through the Repository

A user should be able to trace a single vendor through the repository.

The expected path is:

```text id="v0j4i7"
AI Vendor
    ↓
AI System
    ↓
Vendor Inventory
    ↓
Risk Tier
    ↓
Assessment Scope
    ↓
Assessment
    ↓
Evidence Requirements
    ↓
Evidence Register
    ↓
Evidence Validation
    ↓
Evidence Mapping Matrix
    ↓
Framework Assessment
    ↓
Findings / Gaps
    ↓
Risk Register
    ↓
Remediation
    ↓
Assessment Report
```

This traceability is a core quality characteristic of the reference implementation.

---

# 19. How Evidence Moves Through the Repository

The evidence-centric architecture can be summarized as:

```text id="tq6gzi"
Requirement
      ↓
Evidence Requirement
      ↓
Evidence Collection
      ↓
Evidence Asset
      ↓
Validation
      ↓
Evidence Register
      ↓
Evidence Mapping
      ↓
Assessment
      ↓
Risk
      ↓
Reuse
```

The Evidence Asset should remain the stable reference point.

Assessment results, mappings, and risk decisions should reference the evidence rather than duplicate it.

---

# 20. How to Interpret Cross-Framework Mappings

A mapping should never be interpreted as:

> "This document makes the organization compliant with all three frameworks."

Instead, interpret it as:

> "This Evidence Asset provides relevant support for evaluating these requirements, subject to the documented mapping rationale, scope, limitations, and assessment interpretation."

This distinction is critical.

Different frameworks may require:

* Different organizational activities
* Different scope
* Different evidence
* Different implementation conditions
* Different legal or normative conclusions

ECF provides a common evidence foundation while preserving those differences.

---

# 21. How to Adapt the Repository

Organizations should adapt the implementation according to:

* Regulatory jurisdiction
* Industry
* Risk appetite
* AI use cases
* Vendor population
* Organizational maturity
* Existing GRC tooling
* Existing TPRM processes
* Existing AI governance structures
* Evidence retention requirements

The recommended adaptation sequence is:

```text id="5tq1u3"
Understand
   ↓
Assess Current State
   ↓
Identify Gaps
   ↓
Adapt Data Model
   ↓
Adapt Processes
   ↓
Configure Tooling
   ↓
Pilot
   ↓
Validate
   ↓
Scale
```

Avoid implementing the entire repository unchanged.

The repository is a reference architecture and operating model, not a mandatory configuration.

---

# 22. Working With the Excel Artifacts

Excel workbooks in this repository are reference implementation artifacts.

Before using a workbook operationally:

1. Review the methodology.
2. Review the data dictionary.
3. Review assumptions.
4. Confirm scoring logic.
5. Confirm applicable requirements.
6. Confirm organizational ownership.
7. Confirm formulas and validation rules.
8. Test with representative data.
9. Establish version control.
10. Approve the workbook for operational use.

Where possible, calculations should be transparent and auditable.

---

# 23. Working With Mermaid Diagrams

Mermaid diagrams are used where a process or relationship is easier to understand visually.

They should:

* Represent the documented ECF model accurately.
* Use consistent terminology.
* Avoid introducing concepts that do not exist elsewhere in the repository.
* Remain editable.
* Reflect the current version of the underlying process.

When a process changes, update both the relevant documentation and its associated diagram.

---

# 24. Repository as a Reference Implementation

The repository should be understood as three layers:

```text id="6l2m8e"
┌──────────────────────────────────────┐
│         CONCEPTUAL LAYER             │
│ What ECF is and why it exists        │
└──────────────────┬───────────────────┘
                   ↓
┌──────────────────────────────────────┐
│         OPERATING LAYER              │
│ How ECF processes operate            │
└──────────────────┬───────────────────┘
                   ↓
┌──────────────────────────────────────┐
│        IMPLEMENTATION LAYER          │
│ Workbooks, registers, mappings,      │
│ assessments and reporting            │
└──────────────────────────────────────┘
```

The conceptual layer should not be confused with the implementation choices made in the reference scenario.

---

# 25. Quality and Governance Expectations

All repository artifacts should meet the following expectations:

### Consistency

Terminology should align with `ECF-Terminology.md`.

### Traceability

Material conclusions should be traceable to requirements and evidence.

### Transparency

Assumptions should be documented.

### Reproducibility

A reviewer should be able to follow the reference assessment from input to conclusion.

### Version Control

Material changes should be reflected in document versions and repository history.

### Separation of Concepts

Evidence, requirements, assessments, findings, and risks should remain logically distinct.

### Auditability

Important decisions should have a documented basis.

---

# 26. What a New Contributor Should Do

If you are contributing to this repository for the first time:

### Step 1

Read:

`01_Framework/What-is-ECF.md`

### Step 2

Read:

`01_Framework/ECF-Design-Principles.md`

### Step 3

Read:

`01_Framework/ECF-Operating-Model.md`

### Step 4

Read:

`01_Framework/ECF-Governance-Lifecycle.md`

### Step 5

Read:

`01_Framework/ECF-Terminology.md`

### Step 6

Read:

`02_Getting_Started/ECF-Implementation-Roadmap.md`

### Step 7

Review the Evidence Architecture.

### Step 8

Review the reference implementation.

### Step 9

Before creating a new artifact, determine whether an existing ECF object or artifact already addresses the requirement.

This prevents unnecessary duplication within the repository itself.

---

# 27. What a Reviewer Should Be Able to Determine

A reviewer evaluating the repository should be able to answer:

1. What is ECF?
2. What problem does it solve?
3. How does it differ from a governance framework?
4. What is the core evidence object?
5. How is evidence validated?
6. How is evidence mapped?
7. How is reuse determined?
8. How are framework-specific gaps preserved?
9. How does assessment connect to risk?
10. How does the model operate over time?
11. Can the reference implementation be reproduced?
12. Could the model reasonably be adapted to an enterprise environment?

If these questions cannot be answered from the repository, additional documentation or traceability should be added.

---

# 28. Repository Navigation at a Glance

```text id="d8n0qv"
                    START
                      │
                      ↓
              ┌───────────────┐
              │ 01 Framework  │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 02 Getting    │
              │    Started    │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 03 Evidence   │
              │ Architecture  │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 04 Assessment │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 05 Cross-     │
              │ Framework     │
              │ Mapping       │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 06 Reference  │
              │ Implementation│
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 07 Risk &     │
              │ Reporting     │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 08 Implement. │
              │ Guide         │
              └───────┬───────┘
                      ↓
              ┌───────────────┐
              │ 09 Visuals    │
              └───────────────┘
```

---

# 29. Final Principle

The repository should not be approached as a collection of independent documents.

It is an interconnected reference implementation.

The intended relationship is:

```text id="s0p3az"
Concept
  ↓
Operating Model
  ↓
Evidence Architecture
  ↓
Assessment
  ↓
Evidence Mapping
  ↓
Risk
  ↓
Reporting
  ↓
Continuous Governance
```

The individual artifacts demonstrate different parts of the same operating model.

The strongest way to evaluate the repository is therefore not to ask:

> "How many templates are included?"

Instead, ask:

> **"Can I trace a governance requirement from its definition, to the evidence needed to evaluate it, to a validated Evidence Asset, through cross-framework mapping, into an assessment conclusion, risk decision, and subsequent evidence reuse?"**

That traceability is the defining characteristic of the ECF reference implementation.

