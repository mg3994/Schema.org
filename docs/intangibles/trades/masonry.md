# Masonry & Brickwork Schema

Documentation for masons, bricklayers, and stone workers.

## Comprehensive Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Master Masons Ltd",
  "description": "Specializing in stone walls and restoration.",
  "knowsAbout": ["Bricklaying", "Stone Carving"],
  "offers": {
    "@type": "Offer",
    "itemOffered": { "@type": "Service", "name": "Wall Restoration" },
    "price": "150.00",
    "priceCurrency": "USD",
    "priceSpecification": {
      "@type": "UnitPriceSpecification",
      "price": "150.00",
      "priceCurrency": "USD",
      "unitText": "hour"
    }
  }
}
```
