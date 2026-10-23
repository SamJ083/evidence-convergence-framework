# Framework Mapping Methodology

## 1. Purpose

This document defines the methodology used by the Evidence Convergence Framework (ECF) to establish, evaluate, document, review, and maintain relationships between governance evidence and requirements across multiple frameworks.

ECF supports evidence convergence across the NIST AI Risk Management Framework (AI RMF), ISO/IEC 42001, and the EU Artificial Intelligence Act (EU AI Act). It provides a consistent method for determining what evidence may support a requirement, the limitations of that evidence, and where additional assessment or evidence is necessary.

ECF does not replace the source frameworks, establish legal interpretations, provide certification, or presume that requirements across frameworks are equivalent.

**Core principle:** Evidence may be reusable across requirements, but every evidence-to-requirement relationship must be evaluated independently.

## 2. Scope

This methodology governs:

- Representation and identification of framework requirements.
- Relationships between framework requirements, evidence requirements, and registered evidence assets.
- Mapping strength, rationale, limitations, and review status.
- Applicability analysis and conditional mappings.
- Evidence reuse and framework-specific gap identification.
- Traceability to assessments, findings, risks, remediation, and governance decisions.
- Mapping maintenance when requirements, evidence, or organizational circumstances change.

Evidence registration, classification, metadata, validation, and lifecycle management are defined in `05_Evidence_Model/`. This document uses those capabilities rather than redefining them.

## 3. Mapping principles

ECF applies the following principles to every mapping:

1. **Evidence convergence is supported; requirement convergence is not assumed.** Similar evidence needs do not establish equivalent obligations or outcomes.
2. **Mappings represent documented relationships.** A mapping indicates that evidence may support the evaluation of a requirement; it does not prove compliance or control effectiveness.
3. **Each relationship is assessed independently.** An evidence asset may support multiple requirements to different degrees.
4. **Partial coverage remains visible.** Evidence that supports only part of a requirement must not be presented as complete coverage.
5. **Applicability precedes conclusions about coverage.** Applicable legal, regulatory, contractual, and organizational conditions must be evaluated.
6. **Evidence characteristics constrain reuse.** Scope, provenance, currency, assurance, limitations, and assessment context affect suitability.
7. **Framework-specific gaps remain explicit.** Shared evidence does not eliminate requirements for additional documentation, testing, validation, or interpretation.
8. **Mapping, assessment, and governance remain distinct.** Mapping informs assessment; assessment informs findings and risk evaluation; authorized decision-makers determine risk treatment and acceptance.
9. **Mappings are traceable and maintainable.** Every material mapping decision must have an identifiable basis and review history.

## 4. Mapping entities and relationships

ECF uses the following logical entities.

| Entity | Purpose |
|---|---|
| Framework | Identifies the governing framework or regulation. |
| Framework Version | Identifies the specific edition, release, or legal text used. |
| Framework Requirement | Represents a specific clause, control, category, subcategory, article, or other source-defined provision. |
| Evidence Requirement | Describes what information, demonstration, or assurance is needed to evaluate a requirement. |
| Evidence Asset | Identifies a registered evidence item maintained under the evidence model. |
| Evidence-to-Requirement Mapping | Records the relationship between an evidence asset and a framework requirement, including its rationale and limitations. |
| Assessment | Records the evaluation of evidence against the applicable requirement and assessment criteria. |
| Finding / Gap | Records an identified deficiency, unresolved question, or coverage shortfall. |
| Risk | Represents the assessed exposure associated with a finding or other risk scenario. |
| Remediation | Records planned or completed actions to address a finding or treat a risk. |
| Governance Decision | Records an authorized decision, its rationale, accountable owner, and relevant conditions. |

An **evidence requirement** is not the same as a framework requirement. A framework requirement expresses an obligation, expected outcome, or control objective as defined by its source. An evidence requirement translates that need into the information or demonstration necessary for an assessment.

One framework requirement may require several evidence items. One evidence asset may also support several requirements.

The logical traceability chain is:

`Framework Requirement → Evidence Requirement → Evidence Asset → Mapping Rationale → Assessment Interpretation → Finding / Gap → Risk → Remediation → Governance Decision`

Not every mapping produces a finding or risk. Relationships should be recorded where applicable, without manufacturing downstream records merely to complete the chain.

## 5. Mapping workflow

ECF applies the following sequence.

### Step 1 — Identify the requirement

Record the framework name, version, authoritative identifier, source reference, requirement summary, and relevant applicability conditions.

Preserve the source framework's own structure and terminology. Do not create substitute identifiers that could be mistaken for official requirement identifiers.

### Step 2 — Determine applicability

Establish whether the requirement applies to the organization, AI system, vendor, activity, or assessment scope.

Record the basis for the determination and identify unresolved questions. Where applicability depends on legal interpretation, obtain appropriate legal or compliance review.

A requirement that is not applicable must not be classified as satisfied simply because evidence is available.

### Step 3 — Define the evidence requirement

Describe what must be demonstrated to evaluate the requirement. Identify the expected evidence characteristics, such as scope, period, system coverage, control ownership, or independent assurance, where relevant.

The evidence requirement should be specific enough to support a meaningful assessment without assuming that a particular document is always sufficient.

### Step 4 — Identify candidate evidence

Retrieve relevant assets from the ECF Evidence Register. Review their identity, provenance, validation status, lifecycle status, currency, scope, assurance level, and recorded limitations.

An evidence asset may be considered for mapping even if additional validation is needed. Its limitations and validation status must remain visible.

### Step 5 — Evaluate and document the mapping

Assign a mapping strength using Section 6. Record the rationale, coverage boundaries, limitations, applicable conditions, and any outstanding evidence needs.

The rationale must explain why the evidence is relevant to the specific requirement. A shared keyword, document title, or general subject matter is not sufficient justification.

### Step 6 — Review and interpret

Submit mappings for review according to their materiality, complexity, and risk. Evaluate evidence sufficiency and control effectiveness separately from the mapping relationship.

Record the assessment outcome and link any resulting findings, risks, remediation actions, and governance decisions.

### Step 7 — Maintain the mapping

Reassess affected mappings when framework versions change, evidence expires or is superseded, system scope changes, new limitations emerge, or applicability assumptions are revised.

Retain sufficient history to explain material changes and previous decisions.

## 6. Mapping strength

Mapping strength describes the relationship between an evidence asset and a particular framework requirement. It does not describe evidence quality, compliance status, or control effectiveness.

| Label | Definition | Application |
|---|---|---|
| Direct | The evidence is directly relevant to the requirement and addresses the identified evidence need within its documented scope. | Use when a clear, defensible relationship exists without a material coverage gap in the specific aspect being mapped. |
| Partial | The evidence addresses only some elements of the requirement or leaves a material portion unaddressed. | Record the supported elements and identify the remaining evidence or assessment needs. |
| Conditional | The evidence may support the requirement only if specified conditions or assumptions are satisfied. | Record the conditions, dependencies, and validation steps needed before relying on the evidence. |
| Unsupported | No defensible evidentiary relationship has been established for the requirement. | Use when candidate evidence does not support the requirement, or when the proposed relationship lacks an adequate rationale. |

These labels describe the mapping relationship, not a universal scoring scale. `Unsupported` does not necessarily mean that the organization has failed a requirement; it may mean that no relevant evidence has been identified or that the proposed mapping is unjustified.

Where an item is not applicable, record that determination separately. Do not use `Unsupported` as a substitute for applicability analysis.

### 6.1 Mapping strength versus other statuses

Maintain the following distinctions:

- **Evidence validation status:** whether the asset's identity, provenance, integrity, and other required validation checks have been completed.
- **Evidence quality:** the reliability, completeness, relevance, and assurance characteristics of the asset.
- **Evidence lifecycle status:** whether the asset is current, under review, superseded, expired, or otherwise governed under the evidence model.
- **Applicability status:** whether the requirement applies, does not apply, or requires further determination.
- **Mapping review status:** whether the mapping is a draft, under review, approved, rejected, or otherwise subject to governance workflow.
- **Assessment outcome:** the conclusion reached after evaluating the evidence against the applicable requirement and assessment criteria.
- **Control effectiveness:** whether the relevant control is appropriately designed and operating as intended, based on the assessment performed.
- **Compliance conclusion:** a conclusion made by an appropriately authorized function using applicable criteria and sufficient supporting information.

A `Direct` mapping can rely on stale, incomplete, or insufficiently validated evidence. Conversely, evidence of high quality may be only partially relevant to a particular requirement.

## 7. Mapping rationale and limitations

Each mapping record must contain enough information for an independent reviewer to understand and challenge the decision.

At minimum, record:

- Mapping identifier and linked evidence identifier.
- Framework requirement identifier and framework version.
- Evidence requirement or the specific requirement element being supported.
- Mapping strength and rationale.
- Coverage boundaries and known limitations.
- Applicability conditions or assumptions, where relevant.
- Mapping review status, reviewer, and review date.
- Relevant assessment, finding, risk, or remediation references, where applicable.
- Record version or change history sufficient to maintain traceability.

The rationale should answer three questions:

1. What specific aspect of the requirement does the evidence support?
2. Why is the evidence relevant and appropriate for that purpose?
3. What does the evidence fail to demonstrate, or what conditions constrain reliance on it?

For example, OrionRoute AI's SOC 2 report (`EVID-0002`) may provide relevant assurance about specified controls during the report period and within its stated scope. It does not automatically establish that OrionRoute AI satisfies every AI governance requirement applicable to NovaTide Logistics.

The mapping must account for report scope, period, exceptions, complementary user entity controls, and other relevant limitations.

## 8. Evidence reuse across frameworks

Evidence reuse reduces unnecessary duplication of collection and review effort. It does not eliminate the need to assess the evidence separately against each requirement.

Reuse is appropriate when:

- The asset is relevant to the target requirement and assessment scope.
- Its provenance, integrity, currency, and assurance characteristics are suitable for the intended use.
- The asset covers the relevant system, activity, organizational boundary, and period.
- Its limitations and dependencies are understood.
- Any additional framework-specific interpretation or evidence needs are identified.

Reuse must be restricted or supplemented when evidence has a different scope, does not cover the relevant AI system or activity, relies on unverified assumptions, is no longer current, or fails to demonstrate a required outcome.

For example, OrionRoute AI's architecture diagram (`EVID-0005`) may support an assessment of system boundaries and data flows. It does not independently demonstrate that risk management processes operate effectively, that model performance has been validated, or that a particular legal obligation has been met.

The receiving assessment must document its own rationale for relying on reused evidence. Reuse eligibility is not a blanket approval that applies to every framework, requirement, or assessment.

## 9. Framework-specific considerations

### 9.1 NIST AI RMF

Reference the applicable AI RMF version and preserve its source-defined structure. For AI RMF 1.0, distinguish the Govern, Map, Measure, and Manage functions and their associated categories and subcategories.

The AI RMF is a voluntary risk management framework. Mapping evidence to an AI RMF subcategory does not itself establish that an outcome has been achieved.

Official source: [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)

### 9.2 ISO/IEC 42001

Reference the applicable edition of ISO/IEC 42001 and distinguish clauses containing management system requirements from Annex A reference controls. Record the specific provision and applicable scope.

Do not assume that a document supporting one clause demonstrates implementation of the entire management system or establishes conformity with the standard.

Official source: [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html)

### 9.3 EU AI Act

Reference Regulation (EU) 2024/1689 and the applicable legal text. Identify the relevant article, paragraph, point, or other provision as appropriate.

Applicability must be evaluated in light of the relevant actors, AI system classification, activity, territorial scope, and applicable conditions. Obligations may differ by role, including provider, deployer, importer, or distributor, where relevant.

A mapping must not presume that all AI vendors or AI use cases are subject to the same obligations. Unresolved legal applicability or interpretation questions must be referred for appropriate review.

Official source: [EU AI Act — EUR-Lex](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)

## 10. Governance and change management

Mapping records must be reviewable, version-aware, and updated when material changes affect their validity.

Review triggers include:

- Publication or adoption of a new framework or regulatory version.
- Changes to requirement wording, interpretation, or applicability.
- New evidence, expired evidence, or material changes in evidence scope.
- Changes to the AI system, vendor relationship, processing activities, or organizational context.
- Newly identified evidence limitations, exceptions, findings, or risk conditions.
- Changes to an earlier mapping rationale, review decision, or assessment conclusion.

The mapping owner is responsible for maintaining the record and initiating review when a trigger occurs. Reviewers should be sufficiently independent of the mapping decision for the level of risk and organizational policy involved. Legal interpretations and risk acceptance decisions remain with the appropriate authorized functions.

Where a mapping changes, retain the prior decision or an adequate change record, including the reason for the change, the affected relationships, the review outcome, and any downstream assessments or decisions requiring reassessment.

## 11. Relationship to the mapping workbooks

This methodology governs the following artifacts in `06_Framework_Mappings/`:

- `NIST-AI-RMF-Mapping.xlsx`
- `ISO-42001-Mapping.xlsx`
- `EU-AI-Act-Mapping.xlsx`
- `Unified-Evidence-Mapping-Matrix.xlsx`

The framework-specific workbooks organize mappings for their respective frameworks. The unified matrix provides the cross-framework view of evidence-to-requirement relationships, reuse conditions, limitations, and outstanding gaps.

The unified matrix should serve as the authoritative mapping dataset. Framework-specific workbooks should be curated views or extracts of that dataset, with mapping identifiers and requirement references preserved. Any independently maintained copy must have an explicit reconciliation process to prevent conflicting records.

All workbook records must use the mapping strength definitions in this document and keep mapping strength separate from review status, evidence validation, applicability, and assessment outcomes.

## 12. Expected outcome

A mapping is defensible when its requirement reference is accurate, applicability is addressed, the evidence relationship is explicitly justified, limitations are visible, review status is known, and downstream assessment decisions remain traceable.

ECF uses these controls to reduce duplicative evidence collection while preserving framework-specific interpretation and accountability.

**Evidence convergence improves reuse and traceability. It does not establish requirement equivalence or replace the assessment needed to determine whether a requirement has been satisfied.**
