# Entertainment & Leisure Businesses

Documentation for businesses in the entertainment, arts, and nightlife sectors.

## Core Types

*   **AmusementPark**: A park with rides and attractions.
*   **ArtGallery**: A place where art is displayed or sold.
*   **Casino**: A facility for gambling.
*   **MovieTheater**: A cinema for showing films.
*   **NightClub**: A place for late-night entertainment and dancing.
*   **ComedyClub**: A venue for stand-up comedy.

---

## Comprehensive Example: Movie Theater with Showtimes (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MovieTheater",
  "name": "Starlight Cinema",
  "image": "https://example.com/theater.jpg",
  "telephone": "+15551239999",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "42 Cinema Way",
    "addressLocality": "Hollywood",
    "addressRegion": "CA"
  },
  "openingHours": "Mo-Su 10:00-23:30",
  "event": [
    {
      "@type": "ScreeningEvent",
      "name": "Interstellar",
      "startDate": "2025-10-15T19:00:00-07:00",
      "location": { "@id": "https://example.com/#theater" },
      "offers": {
        "@type": "Offer",
        "url": "https://example.com/tickets/interstellar",
        "price": "15.00",
        "priceCurrency": "USD"
      }
    }
  ]
}
```

## Tips for Entertainment Businesses
*   **Events**: Use the `event` property to list specific showtimes, exhibits, or performances.
*   **Tickets**: Link to ticket purchase pages using `Offer` within the `event` object.
*   **Price Range**: Use `priceRange` to indicate the general cost (e.g., "$$").
*   **Accessibility**: Always include accessibility details for public venues (see the [Accessibility Guide](../advanced/accessibility-safety.md)).

## Things to Avoid
*   **Outdated Showtimes**: Ensure the `event` list is updated daily or weekly.
*   **Missing Addresses**: These are physical locations; a full address is mandatory for local search.
*   **Vague Naming**: Use the specific theater or gallery name, not just "The Theater".
