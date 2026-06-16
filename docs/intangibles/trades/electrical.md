# Electrical Services Schema

Documentation for electricians and electrical contractors.

## Comprehensive Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Electrician",
  "name": "PowerUp Electrical",
  "telephone": "+15551234567",
  "priceRange": "$$$",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Electrical Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Diagnostic Visit" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "75.00",
          "priceCurrency": "USD",
          "unitText": "visit"
        }
      }
    ]
  }
}
```
