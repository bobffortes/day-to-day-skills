# Investment Research

**Use when:** researching a company, ticker, or sector to support (not
replace) an investment decision.

**Important:** this is research support only — not personalized financial
advice, and not automated trade execution.

## Prompt

```text
Act as an investment-research assistant.

For [COMPANY / TICKER / SECTOR], produce:
1. Company overview and business model
2. Revenue drivers and key operating metrics
3. Financial trend summary
4. Valuation context versus appropriate peers
5. Bull case
6. Bear case
7. Catalysts over the next 6-18 months
8. Key risks: business, valuation, macroeconomic, regulatory, governance,
   and liquidity
9. Evidence table with source, date, and confidence
10. Open diligence questions

Rules:
- Prioritize filings, earnings releases, earnings-call transcripts, and
  official investor materials.
- Identify the reporting period for every financial metric.
- Label consensus estimates separately from reported results.
- Do not state a buy/sell recommendation unless explicitly requested.
- Do not execute trades.
```

## Suggested data sources (primary first)

- Company 10-K / 10-Q / annual report and investor relations page
- Earnings call transcripts and press releases
- Regulator filings (e.g. SEC EDGAR, CVM for Brazilian issuers)
- Market data providers for quotes, historical prices, and peer comparisons
- Reputable financial journalism for context, not as the primary evidence

## Related skills

- [`source-trustworthiness-verification.md`](../general-skills/source-trustworthiness-verification.md) —
  apply the Tier 1/2/3 classification to every financial claim.
- [`comparison-scoring-engine.md`](../general-skills/comparison-scoring-engine.md) —
  use the "Investment research" criteria row when comparing peers.
- [`qa-fact-check-gate.md`](../general-skills/qa-fact-check-gate.md) — run
  before sharing any thesis or memo.
