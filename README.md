# Andrew Green

![Focus](https://img.shields.io/badge/Focus-AI%20Governance-1f3a5f) ![Made in Canada](https://img.shields.io/badge/Made%20in-Canada-d52b1e) ![Thesis](https://img.shields.io/badge/Trust%20Problems-Have%20Engineering%20Solutions-555)

Fifteen years running broadcast systems that were not allowed to fail. Now building **[Hydrogenuine](https://hydrogenuine.ca)**, a governed runtime for AI agents and workflows.

## Background

Before AI: broadcast engineering at Newfoundland Broadcasting (NTV), keeping HD television transmission running for half a million households. Led a diverse IT field support team across Atlantic Canada. Designed and built embedded Linux broadcast appliances, and implemented a national emergency alerting setup for community radio. Co-created a televised charity bingo operation that has raised over $1M for Newfoundland charities, with software that generated and serialized hundreds of thousands of unique cards.

The throughline: broadcast, emergency alerting, and live production are domains where the system has to work, has to be auditable, and has to fail gracefully in front of an audience. Governed AI is the same discipline pointed at a new problem.

## What I Build

**Hydrogenuine** gives agent work a place to run, a boundary to stop at, and a record you can read later. Models propose actions, draft text, call tools, and route work; Hydrogenuine decides what is allowed, records what it refused, and keeps memory changes under review.

The core loop:

`Model / agent proposal` → `output + source gate` → `memory quarantine (candidate, not truth)` → `authority chain` → `receipt or refusal, recorded either way` → `operator review`

The authority chain (SOAR, HAL, GPP, UEAK, OEA) is five separate stages, so no stage authorizes itself. Full breakdown: [Authority](https://hydrogenuine.ca/authority/)

A refusal is a first-class, named result (`DENIED_SELF_MINT`, `DENIED_EXPIRED`, `DENIED_SCOPE_MISMATCH`, `DENIED_MISSING_PROOF`, `DENIED_REPLAY`), not a swallowed error.

## Status

Hydrogenuine publishes claim boundaries instead of a generic "production ready" badge. No layer is claimed as more finished than it is. As of the current site:

**GREEN (implemented and tested)**
Native DAG/task-graph execution · memory quarantine · contradiction ledger · proof-bundle/tamper-detection tooling · permit/refusal logic through the authority pipeline · local/OpenAI-compatible model routing · command/tool denial patterns

**YELLOW (sandboxed, stubbed, or hardening)**
UEAK/OEA terminal execution adapters · authenticated operator identity and review UI · external anchoring/receipt chain enforcement · TLA+ TLC CI enforcement · ROS2/Isaac physical backends

**Roadmap**
Temporal/GitHub Actions/Airflow wrappers · proof walkthrough page · DAG kill/resume demo · operator console walkthrough · external-anchor completion

Full detail: [Current status on hydrogenuine.ca](https://hydrogenuine.ca/#status) · [Claim boundaries](https://hydrogenuine.ca/proof/)

## Open Core

The trust grammar (receipt schemas, refusal vocabulary, proof bundle patterns, claim boundary docs) is kept open and inspectable. The commercial layer is the supported enterprise runtime around it: operator console, deployment support, policy packaging, compliance export. No license, price, or availability date is promised ahead of being decided. Details: [Open Core](https://hydrogenuine.ca/open-core/)

## Writing

- **[Hydrogenuine Overview](./Hydrogenuine_Overview.pdf)**: two pages, no math. What the system is and why it exists.
- **[Steer, Don't Silence v3](./SteerDontSilence_v3.pdf)**: a human-centered safety framework for agentic AI. Proportional response instead of binary bans, accountable handoffs instead of silent disappearance. Grounded in months of operating Hydrogenuine, with a machine-side correction ladder that mirrors the human one. Lives in [AI_Oversight_Framework](https://github.com/andrew867/AI_Oversight_Framework) with a skeleton implementation.

## Thesis

The hardest problems in AI are not capability problems. They are trust problems. Trust problems have engineering solutions.

If the governance layer isn't the deepest part of the stack, the stack is built upside down.

## Elsewhere

When I'm not doing this, I build weird solutions for unique problems: fleet management for 1990s payphones, running their Z180 firmware on a cycle-accurate emulator, and controlling broadcast CRT monitors over IP. I like systems that have to account for themselves.

## Contact

[me@andrewgreen.ca](mailto:me@andrewgreen.ca) · [hydrogenuine.ca](https://hydrogenuine.ca)
