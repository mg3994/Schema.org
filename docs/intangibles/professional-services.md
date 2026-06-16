# Professional Services & Skilled Trades

Documentation for independent contractors and skilled tradespeople like electricians, plumbers, masons, architects, and laborers.

## Core Types

*   **Person**: For the individual professional.
*   **LocalBusiness / HomeAndConstructionBusiness**: For the service business entity.
*   **Service**: The specific service offered.
*   **Offer**: The financial terms of the service.
*   **PriceSpecification**: For complex pricing like visiting fees vs. hourly rates.

---

## Example: Electrician with Complex Pricing (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Electrician",
  "name": "PowerUp Electrical Services",
  "telephone": "+15550001111",
  "areaServed": "Greater Springfield Area",
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
      },
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Hourly Labor" },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "120.00",
          "priceCurrency": "USD",
          "unitText": "hour"
        }
      }
    ]
  }
}
```

---

## Example: Architect (JSON-LD)

Architects provide professional design services and often work from a studio but also conduct site visits.

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Ar. Elena Design",
  "jobTitle": "Licensed Architect",
  "hasOccupation": {
    "@type": "Occupation",
    "name": "Architect",
    "occupationalCategory": "17-1011.00"
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Design Studio Way",
    "addressLocality": "Metropolis"
  },
  "offers": {
    "@type": "Offer",
    "itemOffered": {
      "@type": "Service",
      "name": "Architectural Consultation",
      "description": "Initial design consultation and site feasibility study."
    },
    "priceSpecification": {
      "@type": "PriceSpecification",
      "minPrice": "500.00",
      "maxPrice": "2000.00",
      "priceCurrency": "USD"
    }
  }
}
```

---

## Example: Specialized Niche Laborer (JSON-LD)

Example of a specialized laborer (e.g., a high-altitude window cleaner or a deep-sea welder).

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Marcus Peak",
  "jobTitle": "High-Altitude Specialist",
  "description": "Specialized labor for extreme heights and difficult access points.",
  "knowsAbout": ["Rope Access", "External Facade Repair"],
  "offers": {
    "@type": "Offer",
    "itemOffered": {
      "@type": "Service",
      "name": "Difficult Access Cleaning",
      "description": "Window cleaning for skyscrapers and high-rise buildings."
    },
    "priceSpecification": {
      "@type": "UnitPriceSpecification",
      "price": "250.00",
      "priceCurrency": "USD",
      "unitText": "hour"
    }
  }
}
```

## Tips for Tradespeople
*   **PriceSpecification**: Use `UnitPriceSpecification` for hourly or per-visit rates. Use `minPrice` or `maxPrice` for project ranges.
*   **Home Service**: Use `areaServed` to show the geographic range for mobile/home services.
*   **Credentials**: Use `award` or `hasCredential` to show certifications and licenses.

## Things to Avoid
*   **Hidden Fees**: Be transparent about call-out charges.
*   **Vague Area Served**: Specify cities or regions accurately.
