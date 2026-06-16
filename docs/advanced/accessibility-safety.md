# Accessibility & Public Safety

Documentation for describing the accessibility of places and sharing critical public safety information.

## Core Properties for Accessibility

*   **amenityFeature**: Used to list accessibility features like "Wheelchair Accessible".
*   **publicAccess**: Whether the place is open to the public (Boolean).
*   **isAccessibleForFree**: Whether entrance is free (Boolean).
*   **accessibilitySummary**: A human-readable summary of the accessibility of the item.

## Public Safety & Emergency

*   **SpecialAnnouncement**: A timely update for public safety (e.g., COVID-19, Weather alerts).
*   **emergencyService**: Linked via `Organization` or `LocalBusiness`.

---

## Comprehensive Example: Accessible Venue (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Museum",
  "name": "City History Museum",
  "publicAccess": true,
  "isAccessibleForFree": false,
  "accessibilitySummary": "Wheelchair accessible entrance, elevators to all floors, and braille signage.",
  "amenityFeature": [
    {
      "@type": "LocationFeatureSpecification",
      "name": "Wheelchair Accessible",
      "value": true
    },
    {
      "@type": "LocationFeatureSpecification",
      "name": "Assistive Listening Systems",
      "value": true
    }
  ]
}
```

---

## Comprehensive Example: Public Safety Announcement (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SpecialAnnouncement",
  "name": "Winter Storm Warning",
  "text": "Extreme cold and heavy snow expected. Please stay indoors.",
  "datePosted": "2025-01-15T08:00:00Z",
  "expires": "2025-01-16T20:00:00Z",
  "category": "Public Safety",
  "announcementLocation": {
    "@type": "AdministrativeArea",
    "name": "Northern Illinois"
  },
  "url": "https://example.gov/alerts/winter-storm"
}
```

## Tips for Accessibility & Safety
*   **Be Specific**: Instead of just "Accessible", specify "Wheelchair Accessible", "Braille Signage", etc.
*   **Expiration**: For `SpecialAnnouncement`, always use the `expires` property so the alert is removed automatically.
*   **Link to Authority**: Announcements should ideally come from an `Organization` with high authority (e.g., Government agency).

## Things to Avoid
*   **Outdated Announcements**: Never leave an emergency alert active after the danger has passed.
*   **Vague Accessibility**: "Accessible" can mean many things; use `accessibilitySummary` to clarify.
