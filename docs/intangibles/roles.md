# Roles & Jobs Documentation

Documentation for organizational roles and job advertisements.

## Core Types

### Roles
*   **Role**: The base for roles.
*   **OrganizationRole**: A role within an organization.
*   **EmployeeRole**: A specific employment role.
*   **PerformanceRole**: A role in a performance (Actor, Musician).

### Jobs
*   **JobPosting**: An advertisement for a job opening.
*   **Occupation**: The definition of a profession.
*   **OccupationalExperienceRequirements**: Requirements for a job.

---

## Comprehensive Example: EmployeeRole (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Tech Corp",
  "member": {
    "@type": "OrganizationRole",
    "member": {
      "@type": "Person",
      "name": "Jane Doe"
    },
    "startDate": "2020-01-01",
    "roleName": "Lead Architect"
  }
}
```

## Tips for Roles & Jobs
*   **Dates**: Use `startDate` and `endDate` for roles.
*   **Job Posting Details**: Include `hiringOrganization`, `jobLocation`, `baseSalary`, and `employmentType`.
*   **Authority**: For `JobPosting`, ensure the `hiringOrganization` points to a valid `Organization`.

## Things to Avoid
*   **Outdated Job Postings**: Use `validThrough` and remove markup for expired jobs.
*   **Vague Role Names**: Use standard industry titles for roles.
