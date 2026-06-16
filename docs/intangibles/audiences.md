# Audiences Schema Documentation

Documentation for defining the target audience of a product, service, or piece of content.

## Core Types

*   **Audience**: The base type for all audiences.
*   **BusinessAudience**: Targeted at businesses or professional groups.
*   **EducationalAudience**: Targeted at students or teachers.
*   **MedicalAudience**: Targeted at medical professionals or patients.
*   **PeopleAudience**: Targeted at people based on age, gender, or other demographics.
*   **ParentAudience**: Targeted at parents.
*   **Researcher**: Targeted at academic or professional researchers.

---

## Comprehensive Example: MedicalAudience (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalWebPage",
  "name": "Management of Type 2 Diabetes",
  "audience": {
    "@type": "MedicalAudience",
    "audienceType": "Clinician",
    "requiredExpertise": "Endocrinology"
  }
}
```

## Tips for Audiences
*   **Specific Properties**: Use properties like `requiredGender`, `suggestedMinAge`, and `suggestedMaxAge` for `PeopleAudience`.
*   **Medical Specifics**: For `MedicalAudience`, use the `MedicalAudienceType` enumeration (e.g., `Clinician`, `MedicalResearcher`).
*   **Nesting**: Audiences are typically nested within a `CreativeWork`, `Service`, or `Product`.

## Things to Avoid
*   **Discriminiation**: Ensure your audience targeting follows local laws and ethical guidelines.
*   **Vague Targets**: Be as specific as possible (e.g., "Pediatricians" instead of just "Doctors").
