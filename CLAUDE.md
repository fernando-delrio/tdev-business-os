# CLAUDE.md — T·DEV Business OS

Read `AGENTS.md` first.

## Purpose

This repository is an operating system for business and delivery decisions. It is not the T·DEV website source repository and it must not become a dumping ground for client data.

## Before acting

1. Identify whether the request is strategy, research, sales, design, engineering, delivery or a combination.
2. Load only the relevant agents/skills.
3. Distinguish evidence from assumptions.
4. Define the desired business outcome and acceptance criteria.
5. Prefer a small coordinated workflow over invoking every specialist.

## Boundaries

- Never store secrets, credentials, webhooks or tokens.
- Never store identifiable prospect/client conversations in the public core.
- Never treat a legal-risk agent as a lawyer.
- Never invent competitor, SEO, market or pricing evidence.
- Never redesign or implement a product merely because a technical solution is available.
- Keep project-specific execution state outside the reusable core unless it is sanitized and intentionally committed.

## T·DEV website relationship

`tdev-business-os` decides and standardizes **how to reason and operate**.
The `t-dev` repository contains the actual website/product implementation.

For landing work, produce a brief/spec/quality-gate result here, then implement in the product repo. Preserve the current approved design unless the task explicitly authorizes redesign.

## Default workflow

`understand → research → diagnose → prioritize → scope → approve → execute → verify → learn`

Do not skip `verify`.

## Quality standard

Avoid generic AI aesthetics and generic agency advice. Recommendations should be specific enough that another agent can implement them without guessing intent.