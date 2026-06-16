# Occupations & Professions Documentation

Documentation for defining professions and their requirements.

## Core Types

*   **Occupation**: The definition of a specific profession.
*   **OccupationalExperienceRequirements**: Requirements for a job or profession.

---

## Comprehensive Example: Occupation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Occupation",
  "name": "Cloud Solutions Architect",
  "mainEntityOfPage": "https://example.com/careers/cloud-architect",
  "description": "An expert in designing and managing cloud-based infrastructure.",
  "estimatedSalary": [
    {
      "@type": "MonetaryAmountDistribution",
      "name": "Salary in USA",
      "currency": "USD",
      "median": "150000"
    }
  ],
  "occupationalCategory": {
    "@type": "CategoryCode",
    "codeValue": "15-1241.00",
    "url": "https://www.onetonline.org/link/summary/15-1241.00"
  },
  "educationRequirements": "Bachelor’s degree in Computer Science or related field.",
  "experienceRequirements": {
    "@type": "OccupationalExperienceRequirements",
    "monthsOfExperience": "60"
  }
}
```

## Tips for Occupations
*   **Salary Stats**: Use `estimatedSalary` with `MonetaryAmountDistribution` to provide data on what the job pays.
*   **Category Codes**: Use standard codes like O*NET or ISCO in the `occupationalCategory` property.
*   **Experience**: Use `monthsOfExperience` for precise requirement documentation.

## Things to Avoid
*   **Confusing with JobPosting**: `Occupation` describes the *profession*, while `JobPosting` describes a *specific opening*.
*   **Generic Descriptions**: Be specific about the duties and skills required.
