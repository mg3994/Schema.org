# Plumbing, Pipe & Fitting Services

Documentation for plumbers, pipe-fitters, and hydraulic specialists.

## Core Types

*   **Plumber**: The specific business type for plumbing.
*   **Service**: The specific task (e.g., "Leak Detection", "Pipe Fitting").
*   **PriceSpecification**: Used to distinguish labor, materials, and visiting fees.

---

## Comprehensive Example: Plumbing Business with Variable Pricing (JSON-LD)

This example covers a plumbing service that charges a fixed visiting fee plus an hourly rate, with different charges for materials.

```json
{
  "@context": "https://schema.org",
  "@type": "Plumber",
  "name": "Reliable Pipe & Fitting Co.",
  "image": "https://example.com/plumbing-van.jpg",
  "telephone": "+15551113333",
  "priceRange": "$$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Hydraulic Way",
    "addressLocality": "Springfield"
  },
  "areaServed": {
    "@type": "AdministrativeArea",
    "name": "Sangamon County"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Plumbing & Fitting Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Emergency Pipe Leak Repair",
          "description": "Fixing burst pipes and active leaks."
        },
        "priceSpecification": [
          {
            "@type": "UnitPriceSpecification",
            "price": "90.00",
            "priceCurrency": "USD",
            "description": "Call-out / Visiting Fee",
            "unitText": "visit"
          },
          {
            "@type": "UnitPriceSpecification",
            "price": "120.00",
            "priceCurrency": "USD",
            "description": "Hourly Labor Rate",
            "unitText": "hour"
          }
        ]
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Bathroom Fitting Installation",
          "description": "Installing new sinks, toilets, and showers."
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "200.00",
          "priceCurrency": "USD",
          "description": "Base labor charge per fixture."
        }
      }
    ]
  }
}
```

## Tips for Plumbers
*   **Multiple Price Specifications**: You can use an array for `priceSpecification` to show how a total cost is built (e.g., Visit Fee + Hourly Rate).
*   **24/7 Availability**: If you offer emergency services, use `openingHoursSpecification` to show 24/7 availability for specific services.
*   **Materials**: Mention if you provide materials or if they are charged separately in the `description`.

## Things to Avoid
*   **Hidden Fees**: Always be clear about "minimum charge" or "diagnostic fee".
*   **Vague Service Areas**: Be specific about where you travel to avoid confused customers.
