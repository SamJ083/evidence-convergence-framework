# Evidence Convergence Framework (ECF)

**Status:** Reference Implementation  
**Version:** 1.0  
**Document Type:** Framework Definition  
**Last Updated:** August 2026

---

## 1. Overview

The **Evidence Convergence Framework (ECF)** is an evidence-centric operating model for AI vendor governance.

ECF enables organizations to assess an AI vendor once, collect governance evidence through a structured process, map that evidence across multiple applicable frameworks, and reuse validated evidence wherever appropriate.

The framework is designed to reduce duplicated assessment activity while preserving framework-specific accountability, traceability, and gap identification.

ECF is **not a replacement for, or competitor to, established AI governance frameworks or regulations**. It operates above and across them as a practical evidence management and assessment model.

This reference implementation demonstrates how ECF can be applied to evidence supporting:

- NIST AI Risk Management Framework (AI RMF)
- ISO/IEC 42001
- EU Artificial Intelligence Act (EU AI Act)

The implementation is illustrative and should be adapted to an organization's regulatory obligations, risk appetite, governance model, contractual requirements, and assessment methodology.

---

## 2. The Problem ECF Addresses

Organizations increasingly assess the same AI vendors against multiple governance requirements.

A typical assessment environment may involve:

- Third-party risk assessments
- AI governance assessments
- Information security questionnaires
- Privacy assessments
- Regulatory compliance reviews
- Internal control assessments
- Customer assurance requirements
- Framework-specific control evaluations

These processes frequently request overlapping information from the same vendor.

For example, a vendor may be asked separately to provide:

- AI governance policies
- Risk management procedures
- Model documentation
- Security testing results
- Data governance documentation
- Human oversight procedures
- Incident management processes
- Training and competency records

The underlying evidence may be substantially the same even when the questions, controls, or regulatory obligations differ.

This creates several problems:

1. **Assessment duplication** — vendors repeatedly answer substantively similar questions.
2. **Evidence fragmentation** — governance evidence is distributed across assessment processes.
3. **Inconsistent conclusions** — different teams may evaluate the same evidence differently.
4. **Higher assessment burden** — both organizations and vendors spend additional time responding to overlapping requests.
5. **Weak traceability** — it becomes difficult to determine which evidence supports which governance requirement.
6. **Poor evidence reuse** — validated evidence is often not systematically reused.
7. **Framework silos** — each framework is treated as a separate assessment universe.

ECF addresses these problems by changing the primary unit of analysis from the **questionnaire** to the **governance evidence asset**.

---

## 3. Core Concept

The central proposition of ECF is:

> **Governance evidence should be designed, collected, validated, mapped, and governed as a reusable enterprise asset.**

The operating model can be summarized as:

```text
Assess Once
     ↓
Collect Evidence
     ↓
Validate Evidence
     ↓
Map Evidence
     ↓
Reuse Evidence
     ↓
Identify Framework-Specific Gaps
     ↓
Report Risk and Coverage
