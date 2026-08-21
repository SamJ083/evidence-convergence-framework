# ECF Implementation Roadmap

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Implementation Roadmap
**Last Updated:** August 2026

---

## 1. Purpose

This roadmap provides a practical sequence for implementing the Evidence Convergence Framework (ECF) for AI vendor governance.

It is intended to help an organization move from the conceptual ECF model to an operational evidence-centric governance process.

The roadmap is also the recommended sequence for navigating this reference repository.

The implementation follows the central ECF principle:

> **Design governance evidence once, validate it, map it across applicable requirements, and reuse it where appropriate while preserving framework-specific gaps and risk decisions.**

---

# 2. Implementation Approach

ECF implementation can be organized into six phases:

```text
Phase 1
Understand ECF
      ↓
Phase 2
Design Evidence Architecture
      ↓
Phase 3
Establish Assessment Model
      ↓
Phase 4
Implement Cross-Framework Mapping
      ↓
Phase 5
Execute Vendor Assessment
      ↓
Phase 6
Operationalize & Improve
```

Each phase builds on the previous one.

Organizations do not need to implement every repository artifact exactly as demonstrated here. The repository represents a practical reference implementation that can be adapted to organizational maturity, risk profile, technology environment, and regulatory requirements.

---

# 3. Phase 1 — Understand ECF

### Objective

Establish a common understanding of ECF before implementing the evidence architecture.

### Key Activities

* Understand the ECF conceptual model.
* Review ECF design principles.
* Review the operating model.
* Review the governance lifecycle.
* Establish common terminology.
* Understand the distinction between evidence, requirements, controls, assessments, findings, and risks.

### Repository Artifacts

```text
01_Framework/
├── What-is-ECF.md
├── ECF-Design-Principles.md
├── ECF-Operating-Model.md
├── ECF-Governance-Lifecycle.md
└── ECF-Terminology.md
```

### Completion Criteria

The implementation team should be able to explain:

* What ECF is.
* What ECF is not.
* Why evidence is the primary reusable asset.
* How evidence can support multiple frameworks.
* Why evidence reuse is conditional.
* Why framework-specific requirements remain visible.

---

# 4. Phase 2 — Design the Evidence Architecture

### Objective

Translate ECF concepts into a structured evidence architecture.

### Key Activities

* Define Evidence Assets.
* Define Evidence Requirements.
* Define evidence metadata.
* Establish evidence lifecycle states.
* Establish evidence validation criteria.
* Define evidence relationships.
* Establish evidence identifiers.
* Define evidence ownership and scope.
* Define reuse criteria.

### Repository Artifacts

```text
03_Evidence_Architecture/
├── ECF-Evidence-Model.md
├── ECF-Evidence-Requirement-Catalog.md
├── ECF-Evidence-Lifecycle.md
└── ECF-Evidence-Governance.md
```

The exact filenames may evolve during implementation.

### Completion Criteria

The organization should have a clear answer to:

> **What constitutes a reusable governance evidence asset, and how is it governed throughout its lifecycle?**

---

# 5. Phase 3 — Establish the Assessment Model

### Objective

Create the operational structure used to assess AI vendors.

### Key Activities

* Define the AI vendor population.
* Define AI system inventory requirements.
* Establish vendor risk tiering.
* Define assessment scope.
* Define assessment questions or evidence requests where necessary.
* Connect assessment activities to Evidence Assets.
* Establish assessment result categories.

### Repository Artifacts

Potential artifacts include:

```text
04_Assessment_Model/
├── AI-Vendor-Inventory.xlsx
├── Vendor-Risk-Tiering.md
├── Vendor-Assessment-Methodology.md
└── Vendor-Assessment-Workbook.xlsx
```

The assessment model should reference Evidence Assets rather than repeatedly reproducing evidence.

---

# 6. Phase 4 — Implement Cross-Framework Mapping

### Objective

Demonstrate how one evidence base can support multiple governance frameworks.

The reference implementation uses:

* NIST AI RMF
* ISO/IEC 42001
* EU AI Act

### Key Activities

* Identify applicable framework requirements.
* Define requirement identifiers.
* Identify common evidence requirements.
* Map Evidence Assets to requirements.
* Document mapping rationale.
* Identify partial mappings.
* Identify framework-specific gaps.
* Preserve framework-specific interpretation.

### Repository Artifacts

Potential artifacts include:

```text
05_Cross_Framework_Mapping/
├── Framework-Requirements.md
├── Evidence-Mapping-Matrix.xlsx
├── Crosswalk-NIST-AI-RMF.md
├── Crosswalk-ISO-42001.md
├── Crosswalk-EU-AI-Act.md
└── Cross-Framework-Analysis.md
```

### Completion Criteria

The implementation should demonstrate:

```text
                    Evidence Base
                         │
          ┌──────────────┼──────────────┐
          ↓              ↓              ↓
       NIST AI RMF   ISO/IEC 42001   EU AI Act
          │              │              │
          └──────────────┼──────────────┘
                         ↓
                Shared Evidence
                + Specific Gaps
```

---

# 7. Phase 5 — Execute the Reference Vendor Assessment

### Objective

Demonstrate ECF using a realistic AI vendor scenario.

The reference implementation should include:

* A fictional organization.
* A fictional AI vendor.
* A realistic AI service.
* A defined business use case.
* A vendor risk profile.
* A completed assessment.
* Evidence artifacts.
* Evidence mappings.
* Findings.
* Risks.
* Remediation actions.
* Final assessment report.

### Key Activities

1. Establish organization profile.
2. Establish AI vendor profile.
3. Establish AI system profile.
4. Perform vendor risk tiering.
5. Define assessment scope.
6. Collect evidence.
7. Validate evidence.
8. Populate Evidence Register.
9. Map evidence across frameworks.
10. Identify gaps.
11. Assess risks.
12. Define remediation.
13. Produce assessment report.

### Expected Result

A reviewer should be able to follow a complete chain:

```text
Vendor
  ↓
AI System
  ↓
Assessment
  ↓
Requirement
  ↓
Evidence Requirement
  ↓
Evidence Asset
  ↓
Framework Mapping
  ↓
Finding / Gap
  ↓
Risk
  ↓
Remediation
  ↓
Governance Decision
```

---

# 8. Phase 6 — Operationalize and Improve

### Objective

Demonstrate how ECF operates beyond a single assessment.

### Key Activities

* Monitor evidence expiration.
* Track evidence reuse.
* Revalidate evidence.
* Monitor vendor changes.
* Monitor AI system changes.
* Monitor regulatory changes.
* Trigger reassessment.
* Measure assessment efficiency.
* Measure evidence quality.
* Measure appropriate evidence convergence.
* Improve the evidence architecture.

### Potential Metrics

#### Evidence

* Evidence validation rate
* Evidence completeness
* Evidence expiration rate
* Evidence reuse rate
* Evidence convergence ratio

#### Assessment

* Assessment cycle time
* Evidence requests per assessment
* Duplicate evidence requests avoided
* Open evidence requests

#### Risk

* Material findings
* Remediation aging
* Residual risk
* Risk acceptance volume

Metrics should support governance improvement rather than create incentives to maximize evidence reuse artificially.

---

# 9. Implementation Maturity

ECF can be implemented progressively.

## Level 1 — Foundational

Characteristics:

* Central Evidence Register
* Defined evidence metadata
* Basic requirement mapping
* Manual validation
* Manual reuse decisions

---

## Level 2 — Integrated

Characteristics:

* Evidence linked to vendor assessments
* Cross-framework mapping
* Defined evidence lifecycle
* Standardized validation
* Reuse workflows
* Risk integration

---

## Level 3 — Operationalized

Characteristics:

* Centralized evidence repository
* Automated lifecycle notifications
* GRC integration
* Automated mapping assistance
* Reuse recommendations
* Dashboards
* Continuous monitoring

---

## Level 4 — Optimized

Characteristics:

* Enterprise evidence architecture
* Dynamic regulatory mapping
* Automated evidence discovery
* Advanced analytics
* Continuous control and evidence monitoring
* Risk-informed assessment orchestration

Automation maturity should follow governance maturity.

An organization should not automate an undefined or poorly controlled evidence process.

---

# 10. Reference Implementation Sequence

The repository should be built in the following order:

```text
01_Framework
       ↓
02_Getting_Started
       ↓
03_Evidence_Architecture
       ↓
04_Assessment
       ↓
05_Cross_Framework_Mapping
       ↓
06_Reference_Implementation
       ↓
07_Risk_and_Reporting
       ↓
08_Implementation_Guide
       ↓
09_Visuals
```

The exact folder names may vary depending on the repository structure already established.

The important dependency is:

```text
Concept
  ↓
Operating Model
  ↓
Evidence Architecture
  ↓
Assessment
  ↓
Mapping
  ↓
Risk
  ↓
Reporting
  ↓
Implementation
```

---

# 11. Implementation Principles

Throughout implementation, maintain the following rules.

### 1. Evidence First

Do not allow questionnaires to become the primary architecture.

### 2. Reuse Before Request

Before requesting evidence, determine whether suitable existing evidence is available.

### 3. Validate Before Reuse

Do not reuse evidence merely because it exists.

### 4. Map at the Requirement Level

Avoid high-level claims that a document "covers" an entire framework.

### 5. Preserve Framework Differences

Do not force convergence where requirements are substantively different.

### 6. Separate Evidence From Interpretation

Do not modify evidence records to represent assessment conclusions.

### 7. Separate Findings From Risk

A finding may become a risk input but is not inherently equivalent to risk.

### 8. Maintain Traceability

Material conclusions should be traceable back to evidence.

### 9. Design for Change

Evidence, requirements, vendors, AI systems, and regulations change.

### 10. Optimize for Appropriate Convergence

The objective is defensible reuse, not maximum reuse.

---

# 12. Definition of Implementation Success

An ECF implementation is successful when an organization can demonstrate that:

1. AI vendor governance requirements are clearly defined.
2. Evidence requirements are identified before evidence collection.
3. Evidence Assets are uniquely identifiable and governed.
4. Evidence quality and scope are documented.
5. Evidence can be mapped to multiple applicable requirements.
6. Reuse decisions are explicit and defensible.
7. Framework-specific gaps remain visible.
8. Assessment results are traceable to evidence.
9. Findings can flow into risk management.
10. Evidence remains governed after assessment completion.
11. New assessments can reuse appropriate existing evidence.
12. The organization can demonstrate reduced duplication without reducing assurance.

---

# 13. Final Implementation Principle

The implementation should continually answer one question:

> **How can the organization obtain stronger governance assurance while reducing unnecessary duplication of evidence collection?**

ECF addresses this through an evidence-centric architecture:

```text
Requirements
     ↓
Evidence Requirements
     ↓
Evidence Assets
     ↓
Validation
     ↓
Mapping
     ↓
Reuse
     ↓
Framework-Specific Gaps
     ↓
Risk & Governance Decisions
```

The repository is a reference implementation of this model, not a universal prescription.

Organizations should adapt the model to their regulatory obligations, risk appetite, governance maturity, technology environment, and operating model.

