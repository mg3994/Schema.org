# Pest Control Services

Documentation for pest control and extermination businesses.

## Core Types

*   **LocalBusiness**: General type for pest control companies.
*   **Service**: Specific tasks like "Termite Inspection", "Ant Treatment", "Bed Bug Removal".

---

## Comprehensive Example: Pest Control (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Pest-Away Solutions",
  "description": "Safe and effective pest control for residential and commercial properties.",
  "telephone": "+15554445555",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Pest Control Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Standard Inspection" },
        "price": "75.00",
        "priceCurrency": "USD"
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Emergency Treatment" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "200.00",
          "priceCurrency": "USD",
          "description": "Starting price for immediate dispatch."
        }
      }
    ]
  }
}
```

## Tips for Pest Control
*   **Methods**: Describe your methods (e.g., "Heat treatment", "Chemical-free") in the `description`.
*   **Guarantees**: Use the `award` or `description` to mention service guarantees or warranties.
*   **Emergency Service**: Use `openingHoursSpecification` to show if you are available 24/7 for urgent infestations.

## Things to Avoid
*   **Vague Quotes**: Since treatment varies by pest type and area size, using `minPrice` is better than a fixed price.
*   **Missing License**: Pest control is a highly regulated field; ensure your license info is visible in the description.
