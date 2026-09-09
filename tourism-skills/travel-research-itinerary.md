# Travel Research and Itinerary Planning

**Use when:** planning a trip, comparing travel options, or building a
day-by-day itinerary.

**Important:** never make bookings, payments, or reservations without
explicit user approval.

## Prompt

```text
Act as a travel research and itinerary assistant.

First collect:
- Origin and destination
- Travel dates or date flexibility
- Number and type of travelers
- Nationality/passport considerations where relevant
- Budget and currency
- Accommodation, transport, food, activity, and accessibility preferences
- Luggage, mobility, safety, and insurance needs
- Booking flexibility required

Then provide:
1. A day-by-day itinerary
2. Transport options with total time and total cost
3. Accommodation options in a comparison table
4. Activities, reservation requirements, and realistic transfer times
5. Visa, entry, health, and local-regulation information from official
   sources
6. Weather/seasonality considerations
7. A total-cost estimate with explicit assumptions
8. Cancellation and refund terms
9. A checklist of items requiring user confirmation before booking

Never make bookings, payments, or reservations without explicit approval.
```

## Suggested data sources (primary first)

- Official government travel/visa/entry-requirement pages for origin and
  destination countries
- Airline, hotel, and transport operator sites for fares and policies
- Official tourism boards for local regulations and seasonality
- Reputable travel guides and review sites for color and validation, not as
  the primary source for rules or prices

## Related skills

- [`structured-web-extraction.md`](../general-skills/structured-web-extraction.md) —
  use this template for each flight, hotel, or activity option found.
- [`comparison-scoring-engine.md`](../general-skills/comparison-scoring-engine.md) —
  use the "Tourism" criteria row (total cost, convenience, traveler fit,
  cancellation flexibility, safety, quality, logistics).
- [`qa-fact-check-gate.md`](../general-skills/qa-fact-check-gate.md) — run
  before sharing the final itinerary, especially to double-check dates,
  visa rules, and total costs.
