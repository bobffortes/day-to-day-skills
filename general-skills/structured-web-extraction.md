# Structured Web Extraction

**Use when:** converting a web page, listing, or document into usable
research notes, for any type of entity (company, hotel, flight, product,
supplier, job listing, visa rule, etc.).

**Goal:** capture information in a consistent format so it can later be
compared and audited.

## Prompt

```text
Extract only information relevant to the project and return it in this
structure:

- Entity or option:
- URL:
- Source type:
- Date accessed:
- Last updated or effective date:
- Key facts:
- Price or cost:
- Conditions and exclusions:
- Availability or timing:
- Advantages:
- Drawbacks:
- Risks or uncertainties:
- Evidence quote or source location:
- Confidence level: High / Medium / Low
- Verification needed: Yes / No
```

## Applies to

- A hotel or short-term rental listing
- An airline fare or route
- A publicly traded company or ETF
- A competitor or market entrant
- A SaaS product or vendor
- A visa or entry requirement
- A job listing or contract opportunity

## Notes

- Always fill in "Date accessed" — freshness matters for prices, rules, and
  market data.
- Feed the resulting records into
  [`comparison-scoring-engine.md`](./comparison-scoring-engine.md).
