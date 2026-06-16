# Landscaping & Gardening Services

Documentation for landscapers, gardeners, and groundskeeping professionals.

## Core Types

*   **LocalBusiness**: General type for landscaping companies.
*   **Service**: Specific tasks like "Lawn Mowing", "Garden Design", "Tree Trimming".
*   **PriceSpecification**: Used for per-acre, per-hour, or recurring maintenance fees.

---

## Comprehensive Example: Landscaping Company (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Evergreen Landscape Design",
  "description": "Professional garden design and weekly lawn maintenance.",
  "telephone": "+15559998888",
  "areaServed": "West Springfield",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Landscaping Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Lawn Maintenance" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "50.00",
          "priceCurrency": "USD",
          "unitText": "week",
          "description": "Weekly mowing and edging."
        }
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Hardscape Installation" },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "1500.00",
          "priceCurrency": "USD",
          "description": "Patio and walkway design starting price."
        }
      }
    ]
  }
}
```

## Tips for Landscapers
*   **Seasonal Services**: Use different offer catalogs for "Winter (Snow Removal)" and "Summer (Gardening)".
*   **Recurring Fees**: Use `UnitPriceSpecification` with `unitText: week` or `month` for ongoing maintenance.
*   **Visuals**: Link to a gallery of completed landscape projects using the `image` property.

## Things to Avoid
*   **Vague Service Areas**: Since you travel to clients, `areaServed` is critical.
*   **Hidden Material Costs**: If plants or stones are extra, mention it in the `description`.
