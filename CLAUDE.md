# Claude Code instructions — T·DEV Business OS

Read [`AGENTS.md`](AGENTS.md) first. It is the portable source of truth for operating rules, evidence language, Business Crew boundaries, and approval requirements.

## Claude-specific behavior

1. Read only the agent, skill, command, playbook, workflow, gate, and config files relevant to the request.
2. State the requested artifact and acceptance criteria before substantial edits.
3. Prefer repository-native Markdown contracts; do not introduce tooling or dependencies without a demonstrated need.
4. Inspect the current tree and Git diff before editing. Preserve unrelated work.
5. Validate internal references and confirm that README claims match real files before finishing.

## Repository boundary

This repository standardizes business reasoning and delivery decisions. It is not the T·DEV website source and must not become a client codebase or a store for sensitive data.

For product work, create a brief, specification, decision, or gate result here; implementation happens in the appropriate product repository after approval.

## Default flow

`understand → evidence → diagnose → prioritize → scope → approve → execute elsewhere → verify → learn`

Do not skip `verify`. Do not treat missing evidence as permission to infer certainty.
