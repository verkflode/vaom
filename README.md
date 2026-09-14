# VAOM: Verkflöde Agent Operating Model

**The missing control layer between AI capability and business accountability.**

> **This repository is archived.** VAOM is maintained at **[verkflode.com/vaom](https://verkflode.com/vaom)**, which is the single canonical source for the framework. This repository is kept read-only so that existing links continue to resolve.

## Where the framework lives

| Resource | Link |
|---|---|
| The framework, current version | [verkflode.com/vaom](https://verkflode.com/vaom) |
| Whitepaper, markdown | [verkflode.com/vaom.md](https://verkflode.com/vaom.md) |
| Whitepaper, PDF | [verkflode.com/vaom-whitepaper](https://verkflode.com/vaom-whitepaper) |
| Version history and changelog | In the whitepaper, under Version History |

## What is VAOM?

VAOM is a decision governance framework for structuring AI decision authority in enterprise workflows. It defines what AI systems are allowed to decide, under what conditions, with what confidence, and subject to whose authority.

VAOM does not build AI systems. It does not prescribe a tooling stack, a team structure, or a development methodology. It defines **delegation boundaries**: the routing logic, confidence thresholds, escalation paths, and audit requirements that determine whether a decision is automated, reviewed, or prohibited. It also defines how those boundaries **compile into agent identity, scoped credentials, and tool permissions**, so that what an agent is allowed to do and what it is able to do are the same thing by construction.

**Core principles:** high confidence does not automatically imply execution rights, because statistical confidence and organisational authority are independent gates; and boundaries must compile to enforcement, because policy that is not bound to the agent's identity and tools is documentation, not control.

### When do organisations need VAOM?

VAOM becomes relevant when AI systems begin to:

- make or shape decisions with financial, legal, or operational consequences
- auto-execute actions that were previously approved by humans
- participate in regulated workflows subject to audit or supervisory review

In these contexts, governance frameworks define what is allowed in principle, but teams still need to decide **what the AI may actually do** in practice.

## Key concepts

- **The Delegation Gap**: the space between governance policy ("AI is allowed in this process") and operational control ("the AI may decide *this*, under *these conditions*")
- **Seven-Layer Control Architecture**: implementation-agnostic layers from Trigger & Intake through Human Oversight, with three cross-cutting concerns: Governance, Human Oversight, and Continuous Assurance
- **Confidence Gate**: composite scoring evaluated against threshold policy to route decisions into auto-execute, human review, or escalation
- **Delegation Discovery & Design**: a four-stage method for identifying decision points, decomposing authority, selecting delegation patterns, and assessing readiness
- **Delegation Identity & Credentialing**: delegated execution contexts, matrix-to-scope compilation, and structural non-delegability, where the strongest form of "no" is a tool the agent cannot reach
- **Continuous Assurance & Guardian Agents**: runtime verification of delegation boundaries, behavioral envelopes, circuit breakers, and guardian agents governed as delegated agents themselves
- **Calibration Anti-Patterns**: named failure modes with symptoms, root causes, and signals to watch

## Who is VAOM for?

VAOM is designed for regulated enterprises deploying AI agents into workflows with operational, financial, or regulatory consequences. It is not designed for low-stakes use cases such as internal chatbots or productivity assistants.

Typical users: enterprise architects, AI governance leads, compliance officers, risk managers, and the teams implementing AI-enabled workflows.

## License

VAOM is published as an open framework under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to adopt, adapt, and build on VAOM with attribution to Verkflöde AB.

## Contact

Issues and pull requests are closed on this archived repository. Feedback, implementation case studies, and questions are welcome at hello@verkflode.com.

## About

VAOM is developed and maintained by [Verkflöde AB](https://verkflode.com), a European AI governance and L&D consultancy.

*Autonomy, bounded. Decisions, traceable. Accountability, preserved. Boundaries, enforced.*
