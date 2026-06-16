# Educational & Legal Documentation

Documentation for educational programs and legal/governmental schemas.

## Core Types

### Educational
*   **EducationalOccupationalProgram**: A study program.
*   **Course**: A single course.
*   **WorkBasedProgram**: On-the-job training.
*   **AlignmentObject**: Connecting content to educational standards.

### Legal & Permits
*   **Permit**: A license or permit.
*   **GovernmentPermit**: Specifically for government-issued permits.
*   **Legislation**: Laws, regulations, and statutes.
*   **LegislationObject**: Digital versions of legal documents.

---

## Comprehensive Example: Course (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Course",
  "name": "Introduction to Computer Science",
  "description": "Learn the basics of CS using Python.",
  "provider": {
    "@type": "Organization",
    "name": "Open University",
    "sameAs": "https://www.openuni.edu"
  },
  "courseCode": "CS101",
  "hasCourseInstance": {
    "@type": "CourseInstance",
    "courseMode": "Online",
    "startDate": "2025-09-01",
    "endDate": "2025-12-15"
  }
}
```

## Tips for Educational & Legal
*   **Provider**: For courses, identifying the `provider` is essential.
*   **Legislation Jurisdiction**: Use `legislationJurisdiction` to show where a law applies.
*   **Permit Issuers**: Identify the `issuer` of a permit (usually a `GovernmentOrganization`).

## Things to Avoid
*   **Missing Accreditation**: For high-stakes educational programs, include info about the accrediting body.
*   **Vague Legal Status**: Use `legislationStatus` to show if a law is currently in force.
