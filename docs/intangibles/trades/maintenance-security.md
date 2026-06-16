# Home Maintenance & Security Trades

Documentation for skilled trades focused on building maintenance, security, and climate control.

## Core Types

*   **Locksmith**: A professional who works with locks and security systems.
*   **HVACBusiness**: Heating, Ventilation, and Air Conditioning services.
*   **RoofingContractor**: Specialists in roof repair and installation.
*   **HousePainter**: Professional painting services.

---

## Comprehensive Example: Locksmith (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Locksmith",
  "name": "SecureLock 24/7",
  "telephone": "+15550005555",
  "areaServed": "Springfield Metro",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Security Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Emergency Lockout" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "150.00",
          "priceCurrency": "USD",
          "unitText": "visit"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Smart Lock Installation" },
        "price": "99.00",
        "priceCurrency": "USD",
        "description": "Labor charge per lock."
      }
    ]
  }
}
```

## Tips for Maintenance Trades
*   **Emergency Services**: If you offer 24/7 service, use `openingHoursSpecification` to highlight emergency availability.
*   **Service Area**: Be precise about your `areaServed` to avoid irrelevant calls.
*   **Photos**: Use photos of your service van or completed work (e.g., a freshly painted house) to build trust.

## Things to Avoid
*   **Missing Licenses**: Mention licenses or certifications in the `description` or `award` properties.
*   **Vague Quotes**: For roofing or large HVAC projects, use `potentialAction` with `QuoteAction` instead of fixed prices.
