# Comparative Mapping: VAOM v4.0 vs NIST AI RMF vs ISO/IEC 42001

**Purpose.** This document provides a direct, implementation-level comparison between **VAOM v4.0** (Verkflöde Agent Operating Model), the **NIST AI Risk Management Framework (AI RMF 1.0)**, and **ISO/IEC 42001**. The mapping is grounded in concrete VAOM worked examples (Customer Complaints, AML Transaction Triage, HR Policy Assessment) and is intended for enterprise architects, risk leaders, auditors, and regulators.

> **v4.0 update (July 2026).** VAOM 4.0 adds Delegation Identity & Credentialing (Section 9), Continuous Assurance and the guardian function (Section 10), and the Delegation Scorecard (Section 11). These strengthen the mappings below: identity-bound delegated execution contexts provide MEASURE/MANAGE evidence at tool-call granularity, and the scorecard operationalizes ISO 42001 continual improvement. Section 5 of this document adds mappings to the frameworks published since early 2026. A control-by-control mapping to NIST's SP 800-53 agent overlays (COSAiS) will be added when the overlays reach final form.

## 1. Role Separation and Complementarity

| Framework | Core Question Answered | Primary Output |
|---|---|---|
| NIST AI RMF | Have AI risks been identified, measured, and managed? | Risk taxonomy, controls guidance, lifecycle activities |
| ISO/IEC 42001 | Is there a management system governing AI consistently and improving over time? | Policies, roles, processes, audit & continual improvement |
| VAOM v4.0 | Who is allowed to decide what, under which conditions, with what confidence, and under whose authority — right now? | Executable delegation boundaries, confidence gates, escalation logic, audit evidence |

**Key takeaway:** NIST and ISO define *what must exist*; VAOM defines *how decisions operate* inside live workflows.

## 2. VAOM ↔ NIST AI RMF Mapping

### 2.1 Function-Level Alignment

| NIST AI RMF Function | What the RMF Requires | VAOM v4.0 Implementation | Example Illustration |
|---|---|---|---|
| GOVERN | Policies, roles, accountability, oversight | Layer 6 (Governance & Control); Readiness Condition 5 (Named accountable human) | HR policy violations: senior HR role explicitly accountable for outcomes; automation restricted |
| MAP | Context, stakeholders, impact identification | Delegation Discovery & Design (Decision Inventory + Authority Decomposition) | Customer complaints: classification, response drafting, and regulatory reporting mapped as distinct decisions |
| MEASURE | Metrics, confidence, error, drift | Composite Confidence Score; calibration signals; drift management | AML triage: composite score combining rule match, certainty, anomalies |
| MANAGE | Risk treatment, escalation, controls | Confidence Gate routing (Bands A/B/C); non-delegable zones | AML: auto-dismiss low-risk alerts; mandatory escalation for PEP/sanctions |

**What VAOM adds:** RMF-aligned functions enforced at *decision time*, not just assessed periodically.

## 3. VAOM ↔ ISO/IEC 42001 Mapping

### 3.1 Management-System Alignment

| ISO/IEC 42001 Theme | ISO Requirement (Simplified) | VAOM v4.0 Mechanism | Example Illustration |
|---|---|---|---|
| Leadership & Accountability | Clear ownership of AI outcomes | Readiness Condition 5; override/suspension authority | HR workflow: named HR decision-maker with override power |
| Operational Controls | Defined, repeatable AI controls | Seven-layer operating structure | AML monitoring with bounded automated dismissal |
| Risk Treatment | Controls proportional to risk | Delegation Patterns (Prepare & Present → Execute & Audit) | Customer complaints: Draft & Approve for responses |
| Change Management | Controlled changes to AI systems | Layer 5 learning pipeline; model registry; regression tests | AML typology update validated pre-promotion |
| Continual Improvement | Monitoring, review, corrective action | Calibration anti-patterns; scheduled recalibration | Review-queue flood triggers threshold tuning |
| Auditability | Evidence and traceability | Immutable decision logs; provenance tracking | FCA-ready audit trail for complaints |

**What VAOM adds:** ISO-aligned controls translated into executable routing, thresholds, and evidence.

## 4. Example-Grounded Deep Dives

### 4.1 Customer Complaint Escalation

- **Risk Profile:** External-relational; regulatory SLA exposure
- **NIST RMF:** Flags moderate-high impact use; requires oversight
- **ISO 42001:** Requires documented process and roles
- **VAOM Execution:**
  - Classification → Triage & Route (Pattern 3)
  - Response drafting → Draft & Approve (Pattern 2) regardless of confidence
  - Regulatory reporting → Non-delegable (Prepare & Present only)

**VAOM advantage:** Enforced separation between what AI may classify, draft, and never decide.

### 4.2 AML Transaction Triage

- **Risk Profile:** High-volume, high-regulatory exposure
- **NIST RMF:** High-risk AI use; strong monitoring expectations
- **ISO 42001:** Requires controls, auditability, change management
- **VAOM Execution:**
  - Continuous screening → Monitor & Intervene (Pattern 5)
  - Low-risk alerts → Execute & Audit
  - High-risk typologies → Human review / escalation
  - Hard overrides for PEPs, sanctions, thresholds

**VAOM advantage:** Defensible automation zones regulators accept; noise reduction without authority creep.

### 4.3 HR Policy Violation Assessment

- **Risk Profile:** Individual rights; legal and ethical exposure
- **NIST RMF:** Human impact, fairness, explainability required
- **ISO 42001:** Human oversight and governance required
- **VAOM Execution:**
  - Intake classification → Triage & Route with human confirmation
  - Evidence assembly → Prepare & Present
  - Outcome determination → Explicitly non-delegable

**VAOM advantage:** Designed refusal to automate, with technically enforced boundaries and audit justification.

## 5. Mappings to the 2026 Agentic Frameworks (v4.0)

The agentic governance frameworks published since early 2026 assess, secure, or standardize agent systems; VAOM produces the delegation artifact they presuppose.

### 5.1 Singapore IMDA Model AI Governance Framework for Agentic AI (January 2026)

| IMDA dimension | VAOM v4.0 mechanism |
|---|---|
| Assess and bound risks upfront | Delegation Discovery & Design; Authority Decomposition |
| Make humans meaningfully accountable | Readiness Condition 5 (named accountable role); Layer 7; chain accountability for sub-agents |
| Technical controls and processes | Confidence Gate; delegated execution contexts and scope compilation (Section 9); Continuous Assurance (Section 10) |
| Tiered autonomy (fully automated / human-approved / off-limits) | Bands A / B / non-delegable, at decision-point rather than system granularity, with confidence as an independent gate |

### 5.2 OWASP Top 10 for Agentic Applications (2026)

OWASP catalogs agentic threats; VAOM structures function as controls. Illustrative pairings:

- **Agent identity & privilege abuse** → delegated execution contexts; short-lived scoped credentials; no standing or shared agent credentials (Section 9)
- **Excessive autonomy / unauthorized actions** → Delegation Authority Matrix band ceilings; structural non-delegability (tool absence)
- **Multi-agent exploitation** → attenuation rule enforced via credential derivation; chain depth/fan-out limits; delegation-laundering defense (authority attaches to decision types, not agents)
- **Runtime compromise (e.g., injection steering an agent toward its boundary)** → scope-denial telemetry and behavioral envelopes with circuit breakers (Section 10)

Security teams should treat the OWASP taxonomy as an adversarial test suite for a VAOM implementation.

### 5.3 NIST AI Agent Standards Pipeline

NIST's AI Agent Standards Initiative and the SP 800-53 control overlays for AI systems (including single-agent and multi-agent overlays) were in draft at time of writing. VAOM artifacts (matrix entries, execution contexts, decision traces, spawn logs, the Delegation Scorecard) are designed to serve as workflow-level evidence for system-level controls. A control-by-control mapping will be added when the overlays are final.

## 6. Calibration as a Governance Control (Cross-Framework)

VAOM's **Calibration Anti-Patterns** operationalize what both NIST AI RMF and ISO/IEC 42001 require but do not specify:

- **Review Queue Flood** → Signals ineffective risk treatment
- **Confidence Mirage** → Signals poor measurement discipline
- **Exception Graveyard** → Signals governance erosion
- **Stale Threshold** → Signals failure of continual improvement
- **Dimension Collapse** → Signals control weakness

Each anti-pattern provides **observable signals** that trigger corrective action under ISO-style management review and RMF-style risk management.

## 7. Safe Positioning Statement

VAOM v4.0 operationalizes NIST AI RMF risk controls and ISO/IEC 42001 management requirements at the level where AI decisions actually occur, inside live enterprise workflows, and binds them to enforcement through agent identity and scoped credentials.

## 8. Summary

- **NIST AI RMF** provides the risk language and expectations.
- **ISO/IEC 42001** provides the governance system and assurance model.
- **VAOM v4.0** provides the missing execution layer: explicit delegation, confidence gating, escalation, identity-bound enforcement, runtime assurance, and evidence.

Together, they form a complete stack for responsible, auditable AI delegation.
