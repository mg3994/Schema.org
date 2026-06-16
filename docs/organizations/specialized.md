# Specialized Organizations Documentation

Documentation for niche organizational types like airlines, NGOs, and news media.

## Core Types

*   **Airline**: A company providing air transport services.
*   **NGO**: Non-governmental organization (typically non-profit).
*   **NewsMediaOrganization**: A news agency or journalism outlet.
*   **PoliticalParty**: A political group.
*   **WorkersUnion**: A labor organization.
*   **Consortium**: A collaborative group of organizations.

---

## Comprehensive Example: NGO with Funding (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "NGO",
  "name": "Global Green Foundation",
  "url": "https://www.globalgreen.org",
  "logo": "https://www.globalgreen.org/logo.png",
  "nonprofitStatus": "https://schema.org/Nonprofit501c3",
  "funder": {
    "@type": "Organization",
    "name": "Sustainable Future Trust"
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "100 Nature Way",
    "addressLocality": "Portland",
    "addressRegion": "OR",
    "postalCode": "97201"
  },
  "areaServed": "Worldwide",
  "knowsAbout": ["Environmental Protection", "Renewable Energy"]
}
```

## Tips for Specialized Orgs
*   **Nonprofit Status**: For NGOs, the `nonprofitStatus` property is vital for transparency and trust.
*   **Actionable News**: For `NewsMediaOrganization`, use properties like `unnamedSourcesPolicy` and `ethicsPolicy` to build authority.
*   **Airline Codes**: Use `iataCode` for `Airline` entities.

## Things to Avoid
*   **Confusing NGO with Charity**: Use the most specific `nonprofitStatus` enumeration if available.
*   **Missing Policies**: For news organizations, missing transparency policies can hurt E-E-A-T signals.
