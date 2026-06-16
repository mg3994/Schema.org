# Organizations Schema Documentation

An `Organization` represents an institution such as a company, society, university, or government body.

## Major Sub-types

*   [Local Businesses](local-businesses.md) - Physical stores, restaurants, etc.
*   **Corporation**: A business corporation.
*   **EducationalOrganization**: Schools, Universities.
*   **GovernmentOrganization**: Government agencies.
*   **NGO**: Non-governmental organizations.
*   **MedicalOrganization**: Hospitals, clinics, pharmacies.
*   **NewsMediaOrganization**: News agencies and outlets.
*   **OnlineBusiness**: Businesses that operate primarily online.
*   **PerformingGroup**: Music groups, dance groups, theater groups.
*   **SportsOrganization**: Teams and sports governing bodies.
*   **Project**: Funding agencies or research projects.

## Comprehensive List of Types

*   **Airline**: An airline company.
*   **Consortium**: A group of organizations.
*   **Cooperative**: A cooperative organization.
*   **FundingScheme**: A scheme for providing funds.
*   **LibrarySystem**: A system of libraries.
*   **PoliticalParty**: A political organization.
*   **ResearchOrganization**: An organization focused on research.
*   **SearchRescueOrganization**: An organization for search and rescue.
*   **WorkersUnion**: A labor union.

---

## Comprehensive Example: Corporation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Corporation",
  "name": "Nexus Cybernetics",
  "alternateName": "Nexus AI",
  "url": "https://www.nexuscyber.ai",
  "logo": "https://www.nexuscyber.ai/logo.png",
  "sameAs": [
    "https://www.linkedin.com/company/nexus-cyber",
    "https://twitter.com/nexuscyber",
    "https://en.wikipedia.org/wiki/Nexus_Cybernetics"
  ],
  "contactPoint": [{
    "@type": "ContactPoint",
    "telephone": "+1-800-555-0199",
    "contactType": "customer service",
    "areaServed": "US",
    "availableLanguage": ["en", "es"]
  }],
  "founder": {
    "@type": "Person",
    "name": "Elias Vance"
  },
  "foundingDate": "2020-05-20",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Silicon Way",
    "addressLocality": "Palo Alto",
    "addressRegion": "CA",
    "postalCode": "94304",
    "addressCountry": "US"
  },
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": 1250
  },
  "tickerSymbol": "NEXS"
}
```

## Tips for Organizations
*   **Disambiguation**: Use `sameAs` to point to official social media, Wikipedia, and LinkedIn. This is the #1 way to verify your identity to search engines.
*   **Logos**: Use the `logo` property. Google uses this for the Knowledge Panel.
*   **Contact Points**: Define `contactPoint` for customer support, sales, etc. Include `telephone` and `contactType`.
*   **Organization @id**: Define a global `@id` for your organization (e.g., `https://example.com/#organization`) so other pages can reference it without redefining the whole block.

## Things to Avoid
*   **NAP Inconsistency**: Ensure Name, Address, and Phone (NAP) match exactly what is on your website and other directories.
*   **Generic Images**: Don't use stock photos for your logo.
*   **Incomplete Address**: Always provide a full `PostalAddress` object.
