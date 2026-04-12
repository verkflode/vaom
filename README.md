# VAOM — Verkflöde Agent Operating Model

**The missing control layer between AI capability and business accountability.**

Organisations adopting NIST AI RMF or ISO/IEC 42001 often ask: *where do these controls actually live in workflows?* VAOM is one answer to that question.

---

## What is VAOM?

VAOM is a decision governance framework for structuring AI decision authority in enterprise workflows. It defines what AI systems are allowed to decide, under what conditions, with what confidence, and subject to whose authority.

VAOM does not build AI systems. It does not prescribe a tooling stack, a team structure, or a development methodology. It defines **delegation boundaries**: the routing logic, confidence thresholds, escalation paths, and audit requirements that determine whether a decision is automated, reviewed, or prohibited.

**Core principle:** High confidence does not automatically imply execution rights. Statistical confidence and organisational authority are independent gates.

### When do organisations need VAOM?

VAOM becomes relevant when AI systems begin to:

- make or shape decisions with financial, legal, or operational consequences
- auto-execute actions that were previously approved by humans
- participate in regulated workflows subject to audit or supervisory review

In these contexts, governance frameworks define what is allowed in principle, but teams still need to decide **what the AI may actually do** in practice.

## Key Concepts

- **The Delegation Gap** — the space between governance policy ("AI is allowed in this process") and operational control ("the AI may decide *this*, under *these conditions*")
- **Seven-Layer Control Architecture** — implementation-agnostic layers from Trigger & Intake through Human Oversight
- **Confidence Gate** — composite scoring (model certainty + rule match + data completeness + anomaly signals) evaluated against threshold policy to route decisions into auto-execute, human review, or escalation
- **Delegation Discovery & Design** — a four-stage method for identifying decision points, decomposing authority, selecting delegation patterns, and assessing readiness
- **Six Delegation Patterns** — from Prepare & Present (agent assembles context, human decides) to Coordinate & Escalate (multi-agent with cross-chain governance)
- **Calibration Anti-Patterns** — five named failure modes with symptoms, root causes, and signals to watch

## Documentation

| Document | Description |
|---|---|
| [`whitepaper/VAOM_v3_5_whitepaper.md`](whitepaper/VAOM_v3_5_whitepaper.md) | The complete VAOM v3.5 whitepaper |
| [`references/comparative_mapping_NIST_ISO.md`](references/comparative_mapping_NIST_ISO.md) | VAOM v3.5 mapped against NIST AI RMF and ISO/IEC 42001 |
| [`CHANGELOG.md`](CHANGELOG.md) | Version history from v1.0 to v3.5 |

## Interactive Version

The interactive version of VAOM, with stakeholder-specific views (Executive, Technical, Compliance, Discovery) and an explorable architecture diagram, is available at:

**[verkflode.com/vaom](https://verkflode.com/vaom)**

## Regulatory Alignment

VAOM embeds compliance into operational design. It maps to:

- **GDPR** — data minimisation, purpose limitation, transparent decision logic
- **DORA** — operational resilience, change control, audit evidence generation
- **NIS2** — security governance, monitoring, incident response
- **EU AI Act** — human oversight (Art. 14), transparency (Art. 13), risk management (Art. 9)

VAOM complements NIST AI RMF, ISO/IEC 42001, and existing enterprise governance frameworks. It does not replace them.

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

*Autonomy, bounded. Decisions, traceable. Accountability, preserved.*
