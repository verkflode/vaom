# VAOM — Verkflöde Agent Operating Model

**The missing control layer between AI capability and business accountability.**

**v4.0: delegation boundaries that compile.**

Organisations adopting NIST AI RMF, ISO/IEC 42001, or the emerging agentic frameworks (Singapore IMDA, OWASP Agentic Top 10, CSA agent identity) often ask: *where do these controls actually live in workflows?* VAOM is one answer to that question.

---

## What is VAOM?

VAOM is a decision governance framework for structuring AI decision authority in enterprise workflows. It defines what AI systems are allowed to decide, under what conditions, with what confidence, and subject to whose authority.

VAOM does not build AI systems. It does not prescribe a tooling stack, a team structure, or a development methodology. It defines **delegation boundaries**: the routing logic, confidence thresholds, escalation paths, and audit requirements that determine whether a decision is automated, reviewed, or prohibited. Since v4.0 it also defines how those boundaries **compile into agent identity, scoped credentials, and tool permissions**, so that what an agent is allowed to do and what it is able to do are the same thing by construction.

**Core principles:** High confidence does not automatically imply execution rights: statistical confidence and organisational authority are independent gates. And boundaries must compile to enforcement: policy that is not bound to the agent's identity and tools is documentation, not control.

### When do organisations need VAOM?

VAOM becomes relevant when AI systems begin to:

- make or shape decisions with financial, legal, or operational consequences
- auto-execute actions that were previously approved by humans
- participate in regulated workflows subject to audit or supervisory review

In these contexts, governance frameworks define what is allowed in principle, but teams still need to decide **what the AI may actually do** in practice.

## Key Concepts

- **The Delegation Gap** — the space between governance policy ("AI is allowed in this process") and operational control ("the AI may decide *this*, under *these conditions*")
- **Seven-Layer Control Architecture** — implementation-agnostic layers from Trigger & Intake through Human Oversight, with three cross-cutting concerns: Governance, Human Oversight, and Continuous Assurance
- **Confidence Gate** — composite scoring (model certainty + rule match + data completeness + anomaly signals + independent verification) evaluated against threshold policy to route decisions into auto-execute, human review, or escalation
- **Delegation Discovery & Design** — a four-stage method for identifying decision points, decomposing authority, selecting delegation patterns, and assessing readiness
- **Six Delegation Patterns** — from Prepare & Present (agent assembles context, human decides) to Coordinate & Escalate (multi-agent with cross-chain governance, dynamic sub-agent spawning, and authority attenuation)
- **Delegation Identity & Credentialing** *(new in v4.0)* — delegated execution contexts, matrix-to-scope compilation, and structural non-delegability: the strongest form of "no" is a tool the agent cannot reach
- **Continuous Assurance & Guardian Agents** *(new in v4.0)* — runtime verification of delegation boundaries, behavioral envelopes, circuit breakers, and guardian agents governed as delegated agents themselves
- **The Delegation Scorecard** *(new in v4.0)* — ten metrics that turn delegation health into an operating dashboard
- **Calibration Anti-Patterns** — five named failure modes with symptoms, root causes, and signals to watch

## Documentation

| Document | Description |
|---|---|
| [`whitepaper/VAOM_v4_0_whitepaper.md`](whitepaper/VAOM_v4_0_whitepaper.md) | The complete VAOM v4.0 whitepaper |
| [`whitepaper/VAOM_v3_5_whitepaper.md`](whitepaper/VAOM_v3_5_whitepaper.md) | The previous v3.5 whitepaper (superseded) |
| [`references/comparative_mapping_NIST_ISO.md`](references/comparative_mapping_NIST_ISO.md) | VAOM mapped against NIST AI RMF and ISO/IEC 42001 |
| [`CHANGELOG.md`](CHANGELOG.md) | Version history from v1.0 to v4.0 |

## Interactive Version

The interactive version of VAOM, with stakeholder-specific views (Executive, Technical, Compliance, Discovery) and an explorable architecture diagram, is available at:

**[verkflode.com/vaom](https://verkflode.com/vaom)**

## Regulatory Alignment

VAOM embeds compliance into operational design. It maps to:

- **GDPR** — data minimisation, purpose limitation, transparent decision logic
- **DORA** — operational resilience, change control, audit evidence generation
- **NIS2** — security governance, monitoring, incident response
- **EU AI Act** — human oversight (Art. 14), transparency (Art. 13), risk management (Art. 9), on the post-Digital-Omnibus timeline (Annex III high-risk obligations apply from 2 December 2027)
- **Singapore IMDA Model AI Governance Framework for Agentic AI** — dimension-by-dimension mapping in the v4.0 whitepaper
- **OWASP Top 10 for Agentic Applications** — VAOM structures as controls against the agentic threat taxonomy

VAOM complements NIST AI RMF (including the forthcoming NIST agent control overlays), ISO/IEC 42001, and existing enterprise governance frameworks. It does not replace them.

## Who is VAOM for?

VAOM is designed for regulated enterprises deploying AI agents into workflows with operational, financial, or regulatory consequences. It is not designed for low-stakes use cases such as internal chatbots or productivity assistants.

Typical users: enterprise architects, AI governance leads, compliance officers, risk managers, and the teams implementing AI-enabled workflows.

## License

VAOM is published as an open framework under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to adopt, adapt, and build on VAOM with attribution to Verkflöde AB.

## Contributing

Feedback, implementation case studies, and contributions are welcome.

- Open an issue for questions, suggestions, or critique
- Submit a pull request for proposed improvements
- Contact: hello@verkflode.com

## About

VAOM is developed and maintained by [Verkflöde AB](https://verkflode.com), a European AI governance and L&D consultancy.

The whitepaper and the Delegation Lab simulation are produced with Claude Fable 5 under the framework's own Draft & Approve pattern: the model drafts, the accountable author reviews and approves. Details in the whitepaper colophon.

*Autonomy, bounded. Decisions, traceable. Accountability, preserved. Boundaries, enforced.*
