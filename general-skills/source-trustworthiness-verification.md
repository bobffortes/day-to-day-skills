# Source Trustworthiness Verification

**Use when:** evaluating any claim, statistic, price, or policy found online,
before it is used to support a recommendation or decision.

**Goal:** prevent treating every web page as equally credible, and keep facts
separated from inference, estimate, and opinion.

## Prompt

```text
For each material claim, classify the source:

Tier 1 — Primary:
Official government sites, regulator filings, company filings, official
product/provider pages, original datasets, airline/hotel/supplier booking
terms, and direct policy pages.

Tier 2 — High-quality independent:
Established journalism, recognized research organizations, industry bodies,
major databases, and reputable academic publications.

Tier 3 — Useful but verification required:
Reviews, blogs, forums, social posts, aggregators, affiliate pages, and AI
summaries.

For every important fact:
- Prefer Tier 1 sources.
- Record publication or update date.
- Separate fact, inference, estimate, and opinion.
- Flag conflicts between sources.
- Do not make a recommendation based on a single weak source.
- Provide the exact source link or citation beside each important claim.
```

## Quick checklist

- [ ] Is this a Tier 1, Tier 2, or Tier 3 source?
- [ ] Is the publish/update date recent enough for this decision?
- [ ] Does a second, independent source agree?
- [ ] Is this a fact, an estimate, or an opinion?
- [ ] Would the conclusion change if this source were removed?

## Notes

- This skill applies to every domain: financial filings, travel/visa rules,
  product specs, vendor terms, and general news claims.
- Pair with [`qa-fact-check-gate.md`](./qa-fact-check-gate.md) before
  delivering a final answer.
