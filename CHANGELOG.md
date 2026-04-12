# Changelog

All notable changes to the Verkflöde Agent Operating Model (VAOM) are documented in this file.

## [3.5] - 2026

### Added
- **Section 2: What VAOM Is (and What It Is Not)** — clarifies VAOM as a decision governance framework, not an organisational design model. Includes credit risk decisioning analogy for financial services audiences.
- **Hidden Decisions guidance** (Section 5.1) — acknowledges that structured workshops surface 70-80% of decision points. Adds three discovery techniques for the remaining 20-30%: exception mining, shadow observation, and adversarial scenario testing.
- **Multi-agent failure modes** (Pattern 6: Coordinate & Escalate) — three named failure modes: authority conflicts, cascading confidence erosion, and coordination state loss.
- **Contested ownership guidance** (Section 5.4, Readiness Condition 5) — practical guidance for navigating politically contested authority assignment, including framing accountability as override authority rather than blame.
- **Implementation Challenges and Calibration Risks** (Section 8) — honest acknowledgment that model confidence is poorly calibrated, anomaly detection is noisy, and rules can conflict with model reasoning.
- **Calibration Anti-Patterns** (Section 8) — five named anti-patterns with symptoms, root causes, and signals: Review Queue Flood, Confidence Mirage, Exception Graveyard, Stale Threshold, Dimension Collapse.
- **Three worked examples beyond finance:**
  - 7A: Customer Complaint Escalation (retail banking) — three delegation patterns operating simultaneously within one workflow
  - 7B: AML Transaction Triage — high-volume regulatory context; value through noise reduction
  - 7C: HR Policy Violation Assessment — predominantly non-delegable; value through boundary clarity
- **Comparative mapping** (separate document) — VAOM v3.5 mapped against NIST AI RMF and ISO/IEC 42001 with example-grounded deep dives.

## [3.0] - 2026

### Added
- **Section 4: Delegation Discovery & Design** — four-stage method: Decision Inventory, Authority Decomposition, Delegation Pattern Selection, Delegation Readiness Assessment.
- **Six named Delegation Patterns** — Prepare & Present, Draft & Approve, Triage & Route, Execute & Audit, Monitor & Intervene, Coordinate & Escalate.
- **Five-dimension Authority Decomposition** — Reversibility, Consequence Scope, Regulatory Exposure, Confidence Measurability, Accountability Clarity.
- **Delegation Readiness Assessment** — five conditions, three outcomes (Ready, Conditionally Ready, Not Ready).

### Changed
- Implementation roadmap updated to reference the Delegation Discovery method.
- Worked example updated to trace through the discovery process.

## [2.5] - 2026

### Added
- **How the Composite Confidence Score Works** — four-dimension scoring model (model certainty, rule match strength, data completeness, anomaly signals) with weighted averages and hard floors.
- **Managing Foundation Model Drift** — regression testing, threshold recalibration, shadow periods, model registry.

## [2.0] - 2026

### Added
- **Delegation Gap scenario** — accounts payable worked example illustrating what happens without delegation design.
- **"Why This Is Not Workflow Automation"** section — distinguishing VAOM from RPA and rules-based orchestration.

### Changed
- Expanded executive summary with scope definition and architectural neutrality statement.

## [1.0] - 2026

### Added
- Initial release.
- Seven-layer control architecture (Trigger & Intake, Orchestration, Decision & Confidence Gate, Controlled Execution, Knowledge & Learning, Governance & Control, Human Oversight).
- Confidence Gate with three authority bands (Auto-execute, Human Review, Escalation) plus non-delegable zone.
- Delegation Authority Matrix with vendor invoice approval example.
- Worked example: Invoice €3,200 traced through all seven layers.
- Regulatory alignment mapping (GDPR, DORA, NIS2).
- Complementary framework positioning (EU AI Act, NIST AI RMF, ISO 42001).
- 90-day implementation roadmap (five phases).
- Published under CC BY 4.0.
