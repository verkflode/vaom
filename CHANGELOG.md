# Changelog

All notable changes to the Verkflöde Agent Operating Model (VAOM) are documented in this file.

## [4.0] - 2026-07

The enforcement release: **delegation boundaries that compile.** VAOM 4.0 extends the framework from declared boundaries to enforced boundaries: every entry in the Delegation Authority Matrix must be technically bound to agent identity, credentials, and tool permissions.

### Added
- **Seventh design principle: Boundaries Compile to Enforcement** — policy that cannot be compiled into scopes, credentials, and runtime enforcement is documentation, not control.
- **Section 9: Delegation Identity & Credentialing** — the delegated execution context (accountable role × agent identity × task × scopes × band × expiry, evaluated at every tool call); compiling matrix rows into scopes and tool manifests; structural non-delegability (tool absence as the strongest boundary); the agent identity lifecycle (registration, credentialing, derivation, rotation/revocation, retirement) and agent registry cross-referenced with the model registry.
- **Dynamic Delegation & Authority Attenuation** (Section 5.3, Pattern 6) — three inheritance rules for runtime-spawned sub-agents: the attenuation rule (child authority is a strict subset, enforced via credential derivation), spawn-as-decision (spawning has its own matrix row), and chain accountability (named human owns the whole chain; depth/fan-out limits).
- **Fourth multi-agent failure mode: Delegation Laundering** — decisions escaping constraints by routing through looser-bounded agents; defense: authority attaches to decision types, not agents.
- **Section 10: Continuous Assurance and the Guardian Function** — third cross-cutting concern (alongside Governance and Human Oversight): enforcement telemetry, behavioral envelopes, chain integrity monitoring, circuit breakers; the guardian-agent pattern with recursive governance (guardians contain but never expand, do not guard themselves, and have accountable humans).
- **Section 11: The Delegation Scorecard** — ten metrics with healthy ranges across calibration health (band distribution, Band B approval rate, exception share, dimension correlation, verifier disagreement), operational health (band drift, escalation SLA, Band A audit error), and enforcement health (scope-denial rate, chain integrity incidents).
- **Fifth confidence dimension: Independent Verification** — verifier distinct from the proposer (different-family model, deterministic checker, or dry-run); verifier-independence requirement; new implementation challenge: verification theater (track verifier disagreement rates).
- **Worked example 7D: Autonomous Incident Remediation** — IT operations agent with dynamically spawned sub-agents; demonstrates delegated execution contexts, credential attenuation, chain-level confidence, structural non-delegability, and circuit breakers end to end.

### Changed
- **Regulatory alignment rewritten for 2026–2028** (Section 13): post-Digital-Omnibus EU AI Act timeline (Annex III high-risk → 2 December 2027; Annex I → 2 August 2028; Article 50(2) marking → 2 December 2026; GPAI obligations in force since August 2025), framed as a design window, not relief. Added alignment mappings: Singapore IMDA Model AI Governance Framework for Agentic AI, OWASP Top 10 for Agentic Applications, NIST AI Agent Standards Initiative / SP 800-53 agent overlays (forward-compatibility), and levels-of-autonomy research (autonomy certificates ↔ signed matrix entries).
- **Section 2** — added "VAOM Among the 2026 Agentic Frameworks": VAOM positioned as the design method that produces the delegation artifact security, identity, and standards frameworks presuppose.
- **Section 1** — added market validation (Gartner agentic project cancellation forecast; Forrester governance-gap survey).
- **Implementation roadmap** — Phase 3 now includes identity compilation (agent registry, scope compilation, execution context design); Phase 4 wires circuit breakers and credential revocation; Phase 5 establishes the scorecard baseline and includes a structural-denial enforcement test.
- Tagline extended: *Autonomy, bounded. Decisions, traceable. Accountability, preserved. Boundaries, enforced.*

## [3.5] - 2026-04

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

## [3.0] - 2026-04

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
