# Roles, Memberships & Affiliations

Documentation for describing the roles individuals play within organizations and their memberships in programs.

## Core Types

*   **Role**: The base type for any role.
*   **OrganizationRole**: A role in an organization (e.g., employee, founder).
*   **EmployeeRole**: Specifically for employment roles.
*   **PerformanceRole**: A role in a creative work (Actor, Singer).
*   **ProgramMembership**: Membership in a loyalty or professional program.

---

## Comprehensive Example: Employee with Specific Role (JSON-LD)

This example shows how to use `OrganizationRole` to provide more context about an employee's tenure and specific title.

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Innovate Ltd",
  "member": {
    "@type": "OrganizationRole",
    "member": {
      "@type": "Person",
      "name": "Sarah Miller"
    },
    "roleName": "Lead Systems Architect",
    "startDate": "2020-01-01",
    "endDate": "2024-12-31"
  }
}
```

## Comprehensive Example: Loyalty Program Membership (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Jane Doe",
  "hasProgramMembership": {
    "@type": "ProgramMembership",
    "programName": "Sky-High Rewards",
    "membershipNumber": "123456789",
    "hostingOrganization": {
      "@type": "Airline",
      "name": "Global Airways"
    }
  }
}
```

## Tips for Roles
*   **Dates**: Use `startDate` and `endDate` to document the history of a role.
*   **Role Name**: Be descriptive with `roleName` (e.g., "Board Member", "Volunteer", "Lead Vocalist").
*   **Affiliations**: Use `affiliation` on a `Person` as a shorthand for general connection to an `Organization`.

## Things to Avoid
*   **Outdated Memberships**: Update or remove membership schema once it expires.
*   **Confusing Role with Occupation**: `Occupation` describes a *profession* (e.g., "Developer"), while `Role` describes a *specific instance* of that profession at an organization.
