# Moving & Relocation Services

Documentation for professional moving companies and relocation services.

## Core Types

*   **MovingCompany**: The specific business type for movers.
*   **Service**: Tasks like "Local Moving", "Long Distance Move", "Packing Services".

---

## Comprehensive Example: Moving Company (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MovingCompany",
  "name": "Smooth Moves Ltd",
  "description": "Licensed and insured movers for homes and offices.",
  "telephone": "+15553332222",
  "areaServed": ["Illinois", "Missouri", "Iowa"],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Moving Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Standard Studio Move" },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "400.00",
          "priceCurrency": "USD"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Packing Service" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "60.00",
          "priceCurrency": "USD",
          "unitText": "hour"
        }
      }
    ]
  }
}
```

## Tips for Movers
*   **Insurance**: Explicitly state that you are "Licensed and Insured" in your `description`.
*   **Distance**: Clearly define your service area (local vs. long distance).
*   **Items**: Mention if you specialize in piano moving, fine art, or heavy machinery.
*   **Quotes**: Use `potentialAction` with `QuoteAction` to allow users to request estimates based on their specific move.

## Things to Avoid
*   **Missing Prices**: Even if estimates vary, providing a "starting from" price builds trust.
*   **Generic Descriptions**: Specify if you provide boxes, bubble wrap, or other supplies.
