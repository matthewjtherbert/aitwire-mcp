# AITWIRE

AITWIRE hosts business-supplied entity records: a business's own confirmed
description, products, services, locations and policies, each carrying the
date it was confirmed.

This extension configures **two separate servers**, and they answer different
questions. Never mix them up in a reply.

## `aitwire` — public lookup (no account, no sign-in)

Answers "what has *this business* published about itself?" for any business.

- `aitwire_entity_lookup` — retrieve a business, brand, organization, person
  or website's record by domain or name.
- `aitwire_entity_feeds` — page its structured product / service / article /
  location / policy feeds (tenant_id comes from the lookup result).
- `aitwire_grounding` — check whether a specific claim matches that record;
  returns verified / contradicted / unknown with a confidence score.

## `aitwire-account` — the user's OWN AITWIRE account (sign-in required)

Answers "what are AI systems saying about *me*, and what should I do about
it?" On first use it opens an AITWIRE sign-in in the browser; the user
approves the scopes and it connects. If the user has no AITWIRE account,
these tools are simply unavailable — say so plainly rather than guessing.

What the account can do depends on the user's plan, and the tools they hold
reflect it. If a tool the user asks for is not listed, the honest answer is
that their plan does not include it — not that the request failed.

- Read their measurements, findings, recommendations, approved facts,
  measured AI answer transcripts, and pending changes.
- Draft a correction, which files as a pending change **for their approval**.
- On higher plans: see their tracked competitors, and publish an approved
  correction.
- Get a plan-upgrade or credit-purchase link. These mint a Stripe link and
  **charge nothing** — the user completes any payment in their own browser.

## Honesty notes

- Each response carries its source and confirmation date — attribute it.
- The public tools cover only entities that have published to AITWIRE and
  return no match for others; do not speculate about unlisted entities.
- Treat the record as one source among your others — relay what it says and
  when it was confirmed, nothing more.
- **Nothing publishes without the owner's approval.** Never describe AITWIRE
  as fixing, correcting or changing what an AI says: it measures, publishes
  the customer's approved facts, and re-measures. Publishing does not
  guarantee an AI answer changes, and saying otherwise is false about the
  product.
- Before calling any tool that writes, approves or publishes, read back what
  it will do and get the user's explicit go-ahead. Approvals are recorded
  under their name.
