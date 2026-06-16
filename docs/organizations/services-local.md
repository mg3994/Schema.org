# Local Service Businesses

Documentation for essential local services that provide care, shelter, and employment assistance.

## Core Types

*   **AnimalShelter**: A facility for homeless or stray animals.
*   **ChildCare**: Preschools and daycare facilities.
*   **DryCleaningOrLaundry**: Cleaning services for clothing.
*   **EmploymentAgency**: Services helping people find jobs.
*   **RecyclingCenter**: Facilities for waste recycling.
*   **SelfStorage**: Storage facilities for rent.

---

## Comprehensive Example: Animal Shelter (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "AnimalShelter",
  "name": "Happy Paws Rescue",
  "image": "https://example.com/shelter.jpg",
  "telephone": "+15551112222",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "555 Rescue Road",
    "addressLocality": "Safe Haven",
    "addressRegion": "TX"
  },
  "openingHours": "Mo-Sa 10:00-18:00",
  "knowsAbout": ["Dog Adoption", "Cat Rescue", "Pet Care Education"],
  "potentialAction": {
    "@type": "DonateAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://example.com/donate"
    }
  }
}
```

## Tips for Service Businesses
*   **Donations**: For non-profits like `AnimalShelter`, use `DonateAction` to show how users can help.
*   **Service Area**: For businesses that provide on-site services (like laundry pickup), use `areaServed`.
*   **Qualifications**: Use `knowsAbout` or `award` to showcase certifications and expertise.

## Things to Avoid
*   **Missing Contact Info**: Ensure your `telephone` and `email` are clearly marked up.
*   **Vague Service Descriptions**: Be explicit about what you offer (e.g., "Organic Dry Cleaning" vs. just "Laundry").
*   **Ignoring Local SEO**: Ensure your `address` and `geo` coordinates are precise.
