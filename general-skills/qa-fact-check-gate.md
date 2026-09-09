# QA and Fact-Check Gate

**Use when:** immediately before delivering any final research output,
recommendation, or report.

**Goal:** catch stale data, unsupported claims, and unauthorized actions
before they reach the end result.

## Prompt

```text
Quality-check the work before finalizing.

Verify:
1. Every material factual claim has an appropriate source.
2. Dates, prices, availability, rules, and market data are current enough
   for the request.
3. Primary sources were used for policies, financial filings, terms, and
   official requirements where available.
4. Facts are distinct from estimates, opinions, and recommendations.
5. Calculation inputs and assumptions are shown.
6. Conflicting evidence is disclosed rather than ignored.
7. Links, citations, ticker symbols, airport codes, names, dates, and
   currency are correct.
8. No booking, purchase, financial trade, account change, or data-sharing
   step occurs without explicit human approval.

Return:
- Findings verified
- Open questions
- Assumptions
- Risks
- Recommended next action
```

## Notes

- This is the last skill to run in every workflow, regardless of domain.
- If any check fails, fix the underlying research before delivering the
  output — do not just soften the language around it.
