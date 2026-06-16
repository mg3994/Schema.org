# Cleaning & Janitorial Services

Documentation for residential and commercial cleaning services.

## Core Types

*   **LocalBusiness**: General type for cleaning companies.
*   **Service**: Specific tasks like "Deep Clean", "Office Janitorial", "Window Washing".
*   **PriceSpecification**: Used for per-room, per-hour, or square-footage rates.

---

## Comprehensive Example: Residential Cleaning (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Sparkle Home Services",
  "description": "Eco-friendly residential cleaning for homes and apartments.",
  "telephone": "+15557771234",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Cleaning Packages",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Standard Home Clean" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "120.00",
          "priceCurrency": "USD",
          "unitText": "clean"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Deep Cleaning" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "0.15",
          "priceCurrency": "USD",
          "unitText": "square foot"
        }
      }
    ]
  }
}
```

## Tips for Cleaning Services
*   **Pricing Units**: Use `unitText` to clarify if you charge per hour, per room, or per square foot.
*   **Booking Actions**: Use `potentialAction` with `ReserveAction` to allow users to book cleaning slots online.
*   **Eco-Friendly**: Mention certifications or specialized cleaning agents (e.g., "Non-toxic") in the `description`.

## Things to Avoid
*   **Ambiguous Terms**: "Move-in/Move-out clean" should have a clearly defined list of what's included.
*   **Unclear Cancellation Policy**: Mention your cancellation policy in the `description` of the offer.
