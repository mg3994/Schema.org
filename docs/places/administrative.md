# Administrative Areas Documentation

Documentation for cities, countries, states, and other administrative regions.

## Core Types

*   **AdministrativeArea**: The base type for regions.
*   **City**: A city or town.
*   **Country**: A nation.
*   **State**: A state or province.
*   **SchoolDistrict**: A school district.
*   **DefinedRegion**: A region defined by specific rules (e.g., postal codes).

---

## Comprehensive Example: Country with Stats (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Country",
  "name": "Japan",
  "alternateName": "日本 (Nippon)",
  "logo": "https://example.com/flags/jp.png",
  "address": {
    "@type": "PostalAddress",
    "addressCountry": "JP"
  },
  "geo": {
    "@type": "GeoShape",
    "addressCountry": "JP"
  },
  "url": "https://www.japan.go.jp/"
}
```

## Tips for Administrative Areas
*   **ISO Codes**: For `Country`, always use [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) codes.
*   **Hierarchy**: Use `containsPlace` and `containedInPlace` to show relationships (e.g., a `City` inside a `State`).
*   **Statistical Data**: Combine with `Observation` to show population or economic data.

## Things to Avoid
*   **Incorrect Codes**: Ensure you use the correct 2-letter country code.
*   **Confusing with Place**: While an `AdministrativeArea` is a `Place`, it usually represents a political/geographic region rather than a specific physical building.
