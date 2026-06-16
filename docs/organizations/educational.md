# Educational Organizations

Documentation for schools, colleges, universities, and other educational institutions.

## Core Types

*   **School**: General primary or secondary school.
*   **CollegeOrUniversity**: Higher education institutions.
*   **ElementarySchool / MiddleSchool / HighSchool / Preschool**: Specific school levels.

---

## Comprehensive Example: CollegeOrUniversity (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "CollegeOrUniversity",
  "name": "Academy of Advanced Sciences",
  "url": "https://www.aas.edu",
  "logo": "https://www.aas.edu/logo.png",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "500 Academic Blvd",
    "addressLocality": "Boston",
    "addressRegion": "MA",
    "postalCode": "02108"
  },
  "alumni": [
    { "@type": "Person", "name": "Notable Alumnus A" }
  ],
  "numberOfStudents": {
    "@type": "QuantitativeValue",
    "value": 15000
  },
  "foundingDate": "1850"
}
```

## Tips for Educational Orgs
*   **Alumni**: Link to notable `Person` entities who graduated from the institution.
*   **Programs**: Use the `hasOfferCatalog` or link to `EducationalOccupationalProgram` entities.
*   **Parent Organization**: For schools that are part of a larger district or system.

## Things to Avoid
*   **Vague Accreditation**: Be clear about the status of the institution.
*   **Old Student Counts**: Keep the `numberOfStudents` updated annually.
