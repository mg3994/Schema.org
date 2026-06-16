# Social & Sports Events

Documentation for social gatherings and sporting matches.

## Core Types

*   **SocialEvent**: Parties, weddings, social gatherings.
*   **SportsEvent**: Matches, games, tournaments.

---

## Comprehensive Example: SportsEvent (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SportsEvent",
  "name": "City Marathon 2025",
  "startDate": "2025-04-20T07:00:00Z",
  "location": {
    "@type": "Place",
    "name": "City Park",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Chicago",
      "addressRegion": "IL"
    }
  },
  "competitor": [
    { "@type": "Person", "name": "Runner A" },
    { "@type": "Person", "name": "Runner B" }
  ]
}
```

## Tips
*   **Teams vs Players**: Use `competitor` to list either `SportsTeam` or `Person`.
*   **Sport Type**: Use the `sport` property to specify the sport (e.g., "Football", "Basketball").

## Things to Avoid
*   **Missing Scores**: For completed events, use `result` to show the final score.
*   **Incorrect Location**: Marathons often have many locations; use the start point or the event's main hub.
