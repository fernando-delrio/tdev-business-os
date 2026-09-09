# Intelligence storage policy

`intelligence/` is for durable, sourced, sanitized knowledge that improves future decisions. It is not a dumping ground for scraped pages, private conversations, or speculative AI summaries.

## Acceptable records

- dated market or competitor observations from lawful public sources;
- anonymized patterns from consented work;
- reviewed search/customer language evidence;
- invalidated hypotheses and lessons that prevent repeated mistakes.

## Required metadata

Every record must identify:

- subject and business/config scope;
- FACT / INFERENCE / UNKNOWN classification;
- direct source or sanitized origin;
- captured/accessed date and review-by date;
- confidence and material limitations;
- owner responsible for revalidation.

## Prohibited content

- credentials, secrets, tokens, or webhooks;
- prospect/client PII or private conversations;
- confidential pricing, margins, contracts, or analytics exports;
- copied material without a lawful reason to retain it;
- claims without provenance.

Business-specific intelligence should live under `intelligence/<business-id>/`. v0.2 ships no populated market dataset; create records only from real research.
