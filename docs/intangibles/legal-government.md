# Legal & Government Schema

Documentation for laws, permits, and governmental services.

## Core Types

*   **Legislation**: A law, act, or regulation.
*   **GovernmentPermit**: A permit issued by a government authority.
*   **GovernmentService**: A service provided by a government agency.
*   **GovernmentOrganization**: The agency or body providing the service or permit.

---

## Comprehensive Example: Government Service (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "GovernmentService",
  "name": "Pass Port Application",
  "description": "Apply for a new passport or renew an existing one.",
  "serviceType": "Passport Service",
  "provider": {
    "@type": "GovernmentOrganization",
    "name": "Department of State",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Washington",
      "addressRegion": "DC"
    }
  },
  "areaServed": {
    "@type": "Country",
    "name": "US"
  },
  "serviceOperator": {
    "@type": "GovernmentOrganization",
    "name": "Bureau of Consular Affairs"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Passport Fees",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": { "@type": "Service", "name": "Adult Renewal" },
        "price": "130.00",
        "priceCurrency": "USD"
      }
    ]
  }
}
```

## Tips for Legal & Gov
*   **Jurisdiction**: For `Legislation`, use `legislationJurisdiction` to specify the region it applies to.
*   **Permit Requirements**: Use `permitAudience` and `validIn` for government permits.
*   **Service Hours**: Include `openingHoursSpecification` for government offices.
*   **Legislation Status**: Use `legislationStatus` to show if a law is "In Force" or "Repealed".

## Things to Avoid
*   **Vague Providers**: Always identify the specific government branch or agency.
*   **Missing Fees**: If a government service has a cost, document it using `Offer`.
*   **Ambiguous Jurisdiction**: Be precise about whether a law is local, state, or federal.
