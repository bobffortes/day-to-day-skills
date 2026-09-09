# Comparison and Scoring Engine

**Use when:** deciding between multiple options — stocks, trips, vendors,
tools, or any set of alternatives — using consistent, weighted criteria.

**Goal:** avoid picking an option based on a single attractive feature while
ignoring disqualifying conditions.

## Prompt

```text
Create a comparison table using only verified information.

For each option:
- Score each criterion from 1 to 5.
- Explain the score in one short evidence-based sentence.
- Apply the criterion weights supplied by the user.
- Calculate a weighted overall score.
- Do not hide disqualifying conditions behind a high score.
- Identify the best option for value, lowest risk, premium quality, and best
  fit for the stated goal.
- State what new information could change the recommendation.
```

## Scoring formula

\[
\text{Overall Score} = \frac{\sum_{i=1}^{n} (\text{criterion score}_i \times \text{weight}_i)}{\sum_{i=1}^{n} \text{weight}_i}
\]

## Default criteria by project type

| Project type | Suggested criteria |
|---|---|
| Investment research | Financial quality, valuation, growth, competitive position, catalysts, downside risk, liquidity, governance |
| Tourism | Total cost, convenience, traveler fit, cancellation flexibility, safety, quality, logistics |
| Software/vendor | Cost, capabilities, implementation effort, integrations, security, support, scalability |
| E-commerce sourcing | Unit economics, reliability, lead time, product quality, minimum order quantity, return risk |

## Notes

- Weights should be set by the user (or inferred from the research plan)
  before scoring, not adjusted afterward to fit a preferred answer.
- Run [`qa-fact-check-gate.md`](./qa-fact-check-gate.md) after scoring to
  double-check the inputs.
