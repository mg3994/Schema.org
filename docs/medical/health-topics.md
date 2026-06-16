# Health Topic Content

Documentation for medical and health information pages, focusing on high-authority content.

## Core Types

*   **HealthTopicContent**: Content specifically about a health topic.
*   **MedicalWebPage**: A web page with medical information.
*   **WebPage**: The base type.

---

## Comprehensive Example: Health Article on Diabetes (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalWebPage",
  "name": "Understanding Type 2 Diabetes",
  "description": "A comprehensive guide to managing symptoms and treatment for Type 2 Diabetes.",
  "mainEntity": {
    "@type": "HealthTopicContent",
    "name": "Type 2 Diabetes",
    "hasHealthAspect": [
      "https://schema.org/SymptomsHealthAspect",
      "https://schema.org/TreatmentsHealthAspect",
      "https://schema.org/PreventionHealthAspect"
    ]
  },
  "lastReviewed": "2025-01-01",
  "reviewedBy": {
    "@type": "Person",
    "name": "Dr. Aris Thorne",
    "jobTitle": "Endocrinologist"
  },
  "author": {
    "@type": "Organization",
    "name": "Health Insights Network"
  }
}
```

## Tips for Health Content
*   **Health Aspects**: Use the `hasHealthAspect` property with standard Schema.org values (Symptoms, Treatments, Causes, etc.) to help search engines categorize your medical advice.
*   **Professional Review**: Always include `lastReviewed` and `reviewedBy` to build E-E-A-T (Expertise, Authoritativeness, Trustworthiness).
*   **Audience**: Link to a `MedicalAudience` (e.g., "Patient" or "Clinician").
*   **Specialty**: Use `medicalSpecialty` to categorize the content.

## Things to Avoid
*   **Stale Content**: Update the `lastReviewed` date at least annually.
*   **Anonymous Advice**: Avoid publishing medical content without a named professional or organization as the reviewer.
*   **Missing Disclaimers**: While not a schema property, ensure a medical disclaimer is visible on the page.
