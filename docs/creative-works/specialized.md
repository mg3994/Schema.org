# Specialized Creative Works

Documentation for niche creative content like comic stories, quotations, and academic theses.

## Core Types

*   **ComicStory / ComicCoverArt**: For the comic book industry.
*   **Quotation**: A specific quote from a person or work.
*   **Thesis**: An academic thesis or dissertation.
*   **Report**: A formal report (Technical, Government).
*   **ArchiveComponent**: A component of an archival collection.
*   **Statement**: A formal or legal statement.

---

## Comprehensive Example: Academic Thesis (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Thesis",
  "name": "Neural Networks in Renewable Energy Forecasting",
  "author": {
    "@type": "Person",
    "name": "Sarah J. Miller"
  },
  "inLanguage": "en",
  "datePublished": "2024-05-15",
  "description": "A comprehensive study on the application of deep learning for solar power prediction.",
  "sourceOrganization": {
    "@type": "CollegeOrUniversity",
    "name": "Stanford University"
  },
  "educationalLevel": "PhD",
  "keywords": ["AI", "Renewable Energy", "Forecasting"],
  "about": {
    "@type": "Thing",
    "name": "Artificial Intelligence"
  }
}
```

## Tips for Specialized Works
*   **Quotes**: For `Quotation`, use the `spokenBy` or `creator` property.
*   **Comics**: Use `artist`, `penciler`, and `colorist` (standardized as `OrganizationRole` or `Person`) to credit the team.
*   **Theses**: Clearly state the `educationalLevel` (Master, PhD).

## Things to Avoid
*   **Missing Attribution**: Creative works must always have an `author` or `creator`.
*   **Vague Organizations**: For academic and technical reports, the `sourceOrganization` or `publisher` is critical for authority.
