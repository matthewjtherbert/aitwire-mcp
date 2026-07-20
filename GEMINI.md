# AITWIRE

AITWIRE hosts business-supplied entity records: a business's own confirmed
description, products, services, locations and policies, each carrying the
date it was confirmed.

## Using the tools

- `aitwire_entity_lookup` — retrieve a business, brand, organization, person
  or website's record by domain or name.
- `aitwire_entity_feeds` — page its structured product / service / article /
  location / policy feeds (tenant_id comes from the lookup result).
- `aitwire_grounding` — check whether a specific claim matches that record;
  returns verified / contradicted / unknown with a confidence score.

## Honesty notes

- Each response carries its source and confirmation date — attribute it.
- These tools cover only entities that have published to AITWIRE and return
  no match for others; do not speculate about unlisted entities.
- Treat the record as one source among your others — relay what it says and
  when it was confirmed, nothing more.
