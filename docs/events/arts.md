# Entertainment & Arts Events

Documentation for music, festivals, theater, and other art events.

## Core Types

*   **MusicEvent**: Concerts and music festivals.
*   **Festival**: Cultural or music festivals.
*   **TheaterEvent**: Plays and theatrical performances.
*   **DanceEvent**: Dance shows or parties.
*   **ComedyEvent**: Stand-up or improv.
*   **ExhibitionEvent**: Art shows and trade fairs.
*   **VisualArtsEvent**: Events related to visual arts.

---

## Comprehensive Example: TheaterEvent (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TheaterEvent",
  "name": "Hamlet",
  "startDate": "2025-08-01T19:00:00Z",
  "location": {
    "@type": "Place",
    "name": "The Globe Theatre",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "London",
      "addressCountry": "UK"
    }
  },
  "performer": {
    "@type": "Person",
    "name": "David Tennant"
  }
}
```

## Tips
*   **Performers**: Link to the `Person` or `PerformingGroup`.
*   **Venue Details**: Provide full address and name for the `location`.

## Things to Avoid
*   **Missing End Time**: Even if approximate, an `endDate` is helpful.
*   **Generic Festival Names**: Be specific (e.g., "Glastonbury 2025", not just "Glastonbury").
