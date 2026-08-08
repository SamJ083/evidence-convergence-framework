# ECF Design Principles

**Status:** Reference Implementation
**Version:** 1.0
**Document Type:** Framework Design Principles
**Last Updated:** August 2026

---

## 1. Purpose

The Evidence Convergence Framework (ECF) is an evidence-centric operating model for AI vendor governance.

The design principles in this document establish the rules that should govern an implementation of ECF.

They are derived from the ECF conceptual model defined in [`What-is-ECF.md`](./What-is-ECF.md).

The principles are intended to ensure that an implementation remains:

* Evidence-centric
* Framework-agnostic at the evidence layer
* Reusable
* Traceable
* Risk-informed
* Auditable
* Practical for enterprise governance

These principles distinguish the **ECF operating model** from the implementation choices used to demonstrate it.

---

# 2. Foundational Principles

## Principle 1 — Evidence Is the Primary Governance Asset

ECF treats governance evidence as the primary reusable asset of the assessment process.

Traditional assessment models often organize activity around:

```text
Framework
    ↓
Control
    ↓
Question
    ↓
Response
    ↓
Evidence
```

ECF shifts the center of gravity toward:

```text
Governance Requirement
        ↓
Evidence Requirement
        ↓
Evidence Asset
        ↓
Evidence Evaluation
        ↓
Framework Mapping
```

Questions and questionnaires remain useful collection mechanisms, but they are not the primary governance asset.

**Design implication:** The repository, workflow, and assessment artifacts should be organized around identifiable evidence assets rather than independent questionnaires.

---

## Principle 2 — Collect Evidence Once Where Practical

Where substantially similar evidence is required across multiple governance requirements, organizations should seek to collect and validate the evidence once rather than repeatedly requesting equivalent information.

The intended pattern is:

```text
Identify Evidence Need
        ↓
Collect Evidence
        ↓
Validate Evidence
        ↓
Determine Reusability
        ↓
Reuse Where Appropriate
```

This principle exists to reduce:

* Duplicate assessment activity
* Vendor burden
* Internal assessment effort
* Fragmented evidence repositories

**Design implication:** The implementation should provide mechanisms for identifying evidence that has already been collected.

---

## Principle 3 — Reuse Must Be Conditional

Evidence should not be reused merely because it appears related to another requirement.

Reuse should consider:

* Relevance
* Scope
* Currency
* Completeness
* Reliability
* Applicability
* Validation status
* Receiving requirement

Therefore:

```text
Evidence Exists
      ↓
Is it Relevant?
      ↓
Is it Within Scope?
      ↓
Is it Current?
      ↓
Is it Sufficient?
      ↓
Reuse Where Appropriate
```

**Design implication:** The Evidence Register and Mapping Matrix should capture enough information to support an explicit reuse decision.

---

## Principle 4 — Evidence Reuse Does Not Equal Compliance Equivalence

A common evidence asset may support multiple governance requirements without demonstrating compliance with all of them.

For example:

```text
                    Evidence E-012
                          │
             ┌────────────┼────────────┐
             ↓            ↓            ↓
        NIST AI RMF  ISO/IEC 42001  EU AI Act
```

The mapping represents evidentiary relevance.

Each receiving requirement must still be evaluated according to its own criteria and context.

Therefore:

> **One evidence asset does not equal one compliance result.**

**Design implication:** Crosswalks must map evidence to specific requirements rather than simply declaring a document "compliant with" multiple frameworks.

---

# 3. Evidence Architecture Principles

## Principle 5 — Keep the Evidence Layer Separate From the Framework Layer

ECF separates reusable evidence from the frameworks and requirements that consume that evidence.

Conceptually:

```text
                    Evidence Layer
                         │
          ┌──────────────┼──────────────┐
          ↓              ↓              ↓
     NIST AI RMF    ISO/IEC 42001   EU AI Act
```

The evidence model should therefore remain as framework-agnostic as reasonably possible.

**Design implication:** Evidence should have its own identifiers, metadata, lifecycle, and ownership independent of framework mappings.

---

## Principle 6 — Evidence Must Be Traceable

Every material evidence asset should have a unique identifier and sufficient metadata to establish its provenance, scope, lifecycle, and use.

At minimum, the evidence model should support:

* Evidence ID
* Evidence description
* Evidence type
* Source
* Owner
* Scope
* Collection date
* Review or expiration date
* Validation status
* Applicable mappings
* Reuse status
* Limitations

Example:

```text
E-017
 │
 ├── Description
 ├── Source
 ├── Owner
 ├── Scope
 ├── Collection Date
 ├── Review Date
 ├── Validation Status
 ├── Framework Mappings
 └── Limitations
```

**Design implication:** Evidence should never exist only as an untracked attachment or questionnaire response.

---

## Principle 7 — Evidence Quality Must Be Evaluated

The existence of evidence does not establish that it is sufficient.

ECF distinguishes between:

```text
Evidence Exists
```

and:

```text
Evidence Is Sufficient for a Specific Purpose
```

Evidence quality should consider:

| Attribute     | Evaluation Question                       |
| ------------- | ----------------------------------------- |
| Authenticity  | Can the source reasonably be established? |
| Relevance     | Does it address the requirement?          |
| Completeness  | Is material information missing?          |
| Currency      | Is it sufficiently current?               |
| Scope         | Does it cover the assessed context?       |
| Reliability   | Is the source sufficiently trustworthy?   |
| Applicability | Does it apply to the requirement?         |
| Consistency   | Is it consistent with other evidence?     |

**Design implication:** The implementation should distinguish evidence receipt from evidence validation.

---

## Principle 8 — Evidence Must Be Evaluated Against a Defined Requirement

Evidence does not have universal meaning.

The value of an evidence asset depends on what the organization is attempting to establish.

The same evidence may provide:

* Strong support for one requirement
* Partial support for another
* Contextual support for another
* No meaningful support for another

The relationship should therefore be represented as:

```text
Evidence
    ↓
Specific Requirement
    ↓
Assessment Interpretation
```

**Design implication:** Mappings should operate at the requirement level wherever practical, rather than stopping at the framework level.

---

## Principle 9 — Evidence Must Have an Explicit Scope

Evidence should be evaluated against a defined scope.

Scope may include:

* Vendor
* AI system
* Model
* Product
* Service
* Business process
* Geographic region
* Data environment
* Deployment environment
* Regulatory jurisdiction
* Assessment period

Evidence applicable to one product or AI system should not automatically be generalized to another.

**Design implication:** Scope must be represented in the Evidence Register and considered during reuse decisions.

---

## Principle 10 — Evidence Ownership Must Be Explicit

Material evidence should have an identifiable owner.

Ownership may reside with:

* The vendor
* AI Governance
* Information Security
* Privacy
* Third-Party Risk
* Compliance
* A business owner
* Another accountable control function

Ownership should be distinguished from storage.

The repository holding an artifact does not necessarily own the evidence or the underlying control.

**Design implication:** Evidence records should identify both source and accountable owner where applicable.

---

# 4. Convergence and Mapping Principles

## Principle 11 — Seek Legitimate Convergence

ECF seeks to identify genuine overlap between evidence requirements across frameworks.

For example:

```text
NIST AI RMF
        │
        │
ISO/IEC 42001 ───► Common Evidence
        │
        │
EU AI Act
```

Convergence should be based on substantive evidentiary relationships rather than superficial keyword similarity.

**Design implication:** Mapping decisions should be explainable and defensible.

---

## Principle 12 — Preserve Framework-Specific Requirements

ECF does not attempt to make different frameworks equivalent.

Where a requirement has unique evidentiary characteristics, those characteristics must remain visible.

The implementation should therefore recognize:

```text
Common Evidence
Partial Evidence
Framework-Specific Evidence
Missing Evidence
```

**Design implication:** The Mapping Matrix must allow requirements to remain framework-specific when shared evidence is insufficient.

---

## Principle 13 — Do Not Manufacture Convergence

The objective of ECF is not to maximize the percentage of reused evidence.

A mapping should only be established where there is a defensible relationship between the evidence and the receiving requirement.

Organizations should be comfortable identifying:

* No common evidence
* Insufficient evidence
* Partial evidence
* Additional evidence requirements
* Framework-specific requirements

> **Accurate convergence is more important than maximum convergence.**

**Design implication:** Metrics should not reward artificial mappings simply because they increase evidence reuse.

---

## Principle 14 — Mapping Must Be Bidirectional

ECF should support both:

### Evidence → Requirement

```text
Evidence E-024
    ↓
NIST Requirement
ISO Requirement
EU AI Act Requirement
```

### Requirement → Evidence

```text
NIST Requirement
    ↓
Evidence E-024
Evidence E-031
Evidence E-042
```

Bidirectional traceability supports:

* Assessment execution
* Evidence reuse
* Gap analysis
* Internal audit
* Management reporting
* Regulatory response

**Design implication:** The data model should allow navigation from both evidence and requirements.

---

# 5. Evidence Lifecycle Principles

## Principle 15 — Evidence Is a Lifecycle-Managed Asset

Evidence should not be treated as a static attachment.

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

Evidence may cease to be reusable because:

* It has expired.
* The underlying control changed.
* The AI system changed.
* The vendor changed its process.
* Its scope changed.
* A new requirement applies.
* Its quality is no longer sufficient.

**Design implication:** Evidence records should include lifecycle and review information.

---

# 6. Assessment and Risk Principles

## Principle 16 — Separate Evidence From Interpretation

ECF distinguishes between:

### Evidence

What was obtained or observed.

### Interpretation

What the evidence indicates relative to a specific requirement.

This distinction is important because the same evidence may support different conclusions under different requirements.

```text
Evidence
    ↓
Requirement-Specific Interpretation
```

**Design implication:** Assessment workbooks should not overwrite the original evidence record with the assessor's interpretation.

---

## Principle 17 — Separate Assessment From Risk Decision

ECF does not treat evidence collection or assessment results as automatic risk decisions.

The intended relationship is:

```text
Evidence
    ↓
Assessment Interpretation
    ↓
Gap / Finding
    ↓
Risk Analysis
    ↓
Risk Treatment
    ↓
Governance Decision
```

Risk acceptance, remediation, escalation, and treatment remain organizational decisions.

**Design implication:** The Risk Register should remain distinct from the Evidence Register.

---

## Principle 18 — Use a Risk-Based Assessment Scope

ECF should operate within the organization's broader risk methodology.

The appropriate evidence requirements may depend on:

* AI use case
* Vendor criticality
* AI system risk
* Data sensitivity
* Business impact
* Regulatory exposure
* Geographic scope
* Deployment model
* Degree of autonomy
* Human oversight

Therefore:

```text
Risk Profile
    ↓
Assessment Scope
    ↓
Evidence Requirements
```

**Design implication:** ECF should support differentiated assessment depth rather than treating every AI vendor identically.

---

# 7. Governance and Implementation Principles

## Principle 19 — Integrate With Existing GRC Processes

ECF should complement existing governance processes rather than create unnecessary parallel structures.

Potential integration points include:

* Third-Party Risk Management
* Enterprise Risk Management
* AI Governance
* Information Security
* Privacy
* Compliance
* Procurement
* Vendor Management
* Internal Audit
* GRC platforms

**Design implication:** ECF should be implemented as an evidence-centric layer within the organization's existing governance ecosystem where practical.

---

## Principle 20 — Automation Supports Governance; It Does Not Replace Judgment

ECF may be supported by automation for:

* Evidence cataloging
* Metadata management
* Evidence mapping
* Expiration tracking
* Workflow
* Duplicate detection
* Reuse recommendations
* Reporting
* Dashboarding

Automation should not independently determine:

* Legal compliance
* Regulatory interpretation
* Evidence sufficiency
* Materiality
* Risk acceptance
* Risk treatment

**Design implication:** Automated recommendations should remain subject to appropriate human review.

---

## Principle 21 — Design for Auditability

A material assessment conclusion should be traceable through the governance chain:

```text
Assessment Result
       ↓
Requirement
       ↓
Evidence
       ↓
Evidence Source
       ↓
Validation
       ↓
Assessment Interpretation
       ↓
Risk / Decision
```

Auditability is therefore a design characteristic, not an after-the-fact reporting requirement.

**Design implication:** The repository should make it possible for an independent reviewer to reconstruct how a material conclusion was reached.

---

## Principle 22 — Efficiency Must Not Reduce Assurance

ECF seeks to reduce duplicated effort.

However, efficiency must not come at the expense of evidence quality or governance rigor.

The intended outcome is:

> **Less repeated work, not less governance.**

Evidence should be reused when doing so:

* Reduces unnecessary duplication.
* Maintains sufficient assurance.
* Preserves traceability.
* Remains appropriate to the requirement.
* Does not obscure material differences.

**Design implication:** Reuse metrics should be interpreted alongside evidence quality, gaps, and risk outcomes.

---

# 8. Principles Applied to the Reference Implementation

The repository should demonstrate the principles through concrete artifacts.

| ECF Principle                        | Reference Implementation               |
| ------------------------------------ | -------------------------------------- |
| Evidence as primary asset            | Evidence Register                      |
| Collect once / reuse                 | Evidence reuse fields and mapping      |
| Conditional reuse                    | Evidence validation and reuse criteria |
| No compliance equivalence            | Requirement-level Mapping Matrix       |
| Framework-independent evidence       | Evidence taxonomy                      |
| Traceability                         | Unique Evidence IDs                    |
| Evidence quality                     | Validation fields                      |
| Requirement-specific evaluation      | Assessment Workbook                    |
| Explicit scope                       | Vendor and AI System Inventory         |
| Explicit ownership                   | Evidence metadata                      |
| Legitimate convergence               | Cross-framework Mapping Matrix         |
| Framework-specific gaps              | Gap analysis                           |
| No manufactured convergence          | Mapping status / rationale             |
| Bidirectional mapping                | Evidence and requirement references    |
| Evidence lifecycle                   | Review / expiry tracking               |
| Separate interpretation              | Assessment Workbook                    |
| Separate risk decisions              | Risk Register                          |
| Risk-based scope                     | Vendor Risk Tiering                    |
| GRC integration                      | TPRM / AI Governance workflow          |
| Human judgment                       | Review and approval fields             |
| Auditability                         | End-to-end traceability                |
| Efficiency without reduced assurance | Assessment metrics                     |

This table provides the bridge between the conceptual ECF model and the practical repository implementation.

---

# 9. Implementation Conformance

A repository or enterprise implementation does not need to reproduce every artifact in this reference implementation to use ECF.

However, an implementation should demonstrate the core characteristics of the model:

1. Governance evidence is represented as a reusable asset.
2. Evidence can be linked to multiple requirements.
3. Evidence reuse is conditional rather than automatic.
4. Framework-specific requirements remain visible.
5. Evidence quality and lifecycle are considered.
6. Evidence can be traced to its source.
7. Requirements can be traced to supporting evidence.
8. Assessment interpretation remains distinct from evidence.
9. Risk decisions remain distinct from evidence.
10. The model supports auditability.

These characteristics are more important than the specific technology used to implement them.

---

# 10. Summary

The ECF design principles establish a common discipline for implementing an evidence-centric AI vendor governance model.

They can be summarized as:

```text
                  ECF Principles
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
     Evidence       Convergence      Risk
     Governance      & Mapping      Governance
        │              │              │
        ↓              ↓              ↓
   Collect Once     Reuse Where     Interpret
   Validate         Appropriate     Evidence
   Track            Preserve Gaps   Assess Risk
   Maintain         Avoid False     Decide
                    Equivalence
        │              │              │
        └──────────────┼──────────────┘
                       ↓
                Defensible AI
                Governance
```

The central principle remains:

> **Governance evidence should be designed, collected, validated, mapped, reused, and governed as a reusable asset—while preserving the distinct requirements and risk decisions associated with each governance framework.**

ECF therefore optimizes for **appropriate convergence**, not maximum convergence; **evidence reuse**, not evidence dilution; and **governance efficiency**, not reduced assurance.

