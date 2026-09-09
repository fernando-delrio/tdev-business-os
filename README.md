# T·DEV Business OS

An evidence-first operating system for running a small web and software business with AI assistance. T·DEV is the first real implementation; the operating model is designed to be reusable for other businesses without embedding T·DEV assumptions in its core.

This is not a prompt collection or an autonomous company. It is a set of explicit contracts for deciding what to investigate, who reasons about it, how work moves between capabilities, and when an output is ready for human approval.

## Why it exists

Small digital businesses repeatedly solve the same connected problems: understand an opportunity, qualify it, shape a credible intervention, define scope and price, deliver safely, and turn verified results into reusable learning. Ad hoc AI conversations lose evidence, blur assumptions with facts, duplicate instructions, and jump to implementation too early.

Business OS makes that work inspectable and repeatable. It optimizes for decision quality, commercial viability, delivery quality, and accumulated learning—not output volume.

## Two-layer model

### Reusable core

The root operational directories are business-agnostic:

- `agents/`: the small Business Crew—who reasons and decides.
- `skills/`: focused capabilities—what the system can do.
- `commands/`: operator entry points—what is requested.
- `playbooks/`: repeatable business processes—how work proceeds.
- `workflows/`: coordination contracts—how capabilities hand off.
- `quality-gates/`: readiness criteria—when work may advance.
- `rules/`: shared evidence and operating rules.
- `templates/`: reusable output structures.
- `intelligence/`: storage policy for sourced, sanitized knowledge.

### T·DEV implementation

T·DEV-specific identity and constraints live in:

- `config/tdev.example.yaml`: safe configuration schema; values are intentionally incomplete.
- `implementations/tdev/`: T·DEV-only overlays and gates.

Market claims, private pricing, prospect data, credentials, and client conversations do not belong in the reusable core or public configuration.

## Mental model

| Layer | Question | Current implementation |
| --- | --- | --- |
| Business Crew | Who reasons? | Four agent contracts in `agents/` |
| Skills | What capabilities exist? | Business audit and landing quality |
| Commands | What does the operator ask for? | `/audit` specification |
| Playbooks | How does a repeatable process run? | Local lead to client |
| Workflows | How do capabilities coordinate? | Opportunity to delivery |
| Quality Gates | When is output ready? | Recommendation and landing gates |
| Intelligence | What do we know? | Evidence storage policy; no fabricated dataset |
| Config | Who is the current business? | T·DEV example schema |

## Business Crew

v0.2 deliberately uses four deep agents rather than one agent per discipline:

- [`orchestrator`](agents/orchestrator.md): routes work, enforces boundaries, resolves conflicts, and owns the final synthesis.
- [`opportunity`](agents/opportunity.md): combines strategy, competitive research, qualification, pricing, and scope reasoning.
- [`growth-experience`](agents/growth-experience.md): combines UX/conversion, SEO/local SEO, and evidence-led content reuse.
- [`delivery-risk`](agents/delivery-risk.md): combines engineering, QA, accessibility, performance, security basics, and legal/privacy risk identification.

An agent is a reasoning role. A skill is a reusable capability it may invoke. Neither is permission to fabricate missing evidence or take consequential action.

## Skills, commands, playbooks, and gates

- [`business-audit`](skills/business-audit/SKILL.md) turns public evidence and discovery context into an opportunity brief.
- [`landing-quality`](skills/landing-quality/SKILL.md) evaluates a commercial landing across positioning, conversion, accessibility, performance, and maintainability.
- [`/audit`](commands/audit.md) routes an audit request to the minimum relevant crew and skills.
- [`local-lead-to-client`](playbooks/local-lead-to-client.md) covers research through sanitized learning.
- [`opportunity-to-delivery`](workflows/opportunity-to-delivery.md) defines hand-offs, approvals, and stop conditions.
- [`recommendation`](quality-gates/recommendation.md) checks evidence-backed advice.
- [`landing`](quality-gates/landing.md) checks shipping readiness for a generic commercial site.

Every substantive output follows [`rules/evidence.md`](rules/evidence.md) and labels material claims as `FACT`, `INFERENCE`, `RECOMMENDATION`, or `UNKNOWN`.

## Example end-to-end workflow

```text
Operator supplies a business, URL, objective, and available evidence
  → orchestrator validates inputs and routes the request
  → opportunity establishes facts, unknowns, and commercial hypotheses
  → business-audit identifies the smallest credible intervention
  → growth-experience evaluates acquisition and conversion when relevant
  → delivery-risk checks feasibility and material risks
  → recommendation quality gate
  → human approval of scope, price, legal commitments, or client-facing output
  → implementation in the product/client repository
  → landing or delivery-specific quality gate
  → verified, sanitized learning may enter intelligence/templates/skills
```

If evidence is insufficient, the workflow returns questions or an `UNKNOWN`; it does not manufacture a recommendation.

## Repository structure

```text
.
├── agents/                         # Four portable Business Crew contracts
├── commands/audit.md               # Audit entry-point specification
├── config/tdev.example.yaml        # Safe T·DEV configuration example
├── implementations/tdev/           # T·DEV-only overlays
├── intelligence/README.md          # Evidence storage policy
├── playbooks/local-lead-to-client.md
├── quality-gates/                  # Generic readiness checks
├── rules/evidence.md               # Shared claim/evidence vocabulary
├── skills/                         # Reusable capability contracts
├── templates/evidence-brief.md     # Portable evidence-led output template
├── workflows/opportunity-to-delivery.md
├── AGENTS.md                       # Vendor-neutral agent contract
└── CLAUDE.md                       # Claude Code-specific instructions
```

## Quick start

1. Clone the repository and work on a feature branch.
2. Copy `config/tdev.example.yaml` to a private runtime configuration or create an equivalent config for another business. Do not commit secrets or sensitive commercial data.
3. Give the coding agent the business objective, known evidence, desired output, and relevant config path.
4. Ask it to read `AGENTS.md`, then invoke an existing command or playbook—for example: “Run `commands/audit.md` for this URL using only public evidence.”
5. Review claim labels and unresolved `UNKNOWN`s before approving consequential work.
6. Apply the appropriate quality gate before delivery or publication.

The Markdown command and agent files are contracts, not a custom executable runtime. v0.2 requires no package installation or generated automation.

## Claude Code and Codex

### Claude Code

Claude Code should read `CLAUDE.md`, which delegates the portable operating contract to `AGENTS.md`. Reference the desired command, playbook, or skill in the request and provide only the context needed for that operation.

### Codex

Codex should read `AGENTS.md` before substantive work. Point it to the relevant command/playbook and business configuration. It should inspect current repository state, preserve unrelated changes, and stop at the human-approval boundaries defined by the workflow.

Both tools should produce the same evidence categories and respect the same core/implementation boundary. Vendor-specific behavior belongs only in the vendor-specific instruction file.

## Current status

**v0.2 — Business Crew foundation**

Implemented:

- portable operating and evidence contracts;
- four-agent Business Crew;
- two reusable skills;
- one audit command;
- one lead-to-client playbook;
- one end-to-end coordination workflow;
- generic recommendation and landing quality gates;
- a safe T·DEV configuration example and cinematic-intro overlay.

Not implemented:

- an autonomous runtime or command parser;
- CRM, analytics, scraping, deployment, or messaging integrations;
- populated market/competitor intelligence;
- automatic pricing, legal conclusions, or unsupervised client communication;
- product/client implementation code.

## Roadmap

1. Exercise `/audit` against a real, consented case and record failure modes.
2. Add skills only where repeated work proves a stable contract is missing.
3. Add proposal/scope templates after real usage validates their required fields.
4. Introduce sanitized intelligence records with sources and review dates.
5. Consider automation only after the manual workflow is stable and measurable.

## Limitations and non-goals

- Output quality is bounded by supplied and lawfully gathered evidence.
- Legal/privacy output is risk identification and checklist support, not professional legal advice.
- Pricing output is a recommendation requiring private business context and human approval.
- The repository does not replace discovery with a client or owner.
- The core does not store secrets, prospect PII, private conversations, or unverifiable claims.
- This repository does not deploy or modify the T·DEV product website.
