# Architecture & Design Schema

Documentation for licensed architects and design studios.

## Comprehensive Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Ar. Elena Design",
  "jobTitle": "Licensed Architect",
  "hasOccupation": {
    "@type": "Occupation",
    "name": "Architect"
  },
  "offers": {
    "@type": "Offer",
    "itemOffered": { "@type": "Service", "name": "Initial Consultation" },
    "priceSpecification": {
      "@type": "PriceSpecification",
      "minPrice": "500.00",
      "maxPrice": "1500.00",
      "priceCurrency": "USD"
    }
  }
}
```
