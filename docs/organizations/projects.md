# Projects, Research & Funding

Documentation for research projects, funding agencies, and broad initiatives.

## Core Types

*   **Project**: A planned undertaking with a specific goal.
*   **ResearchProject**: A project focused on scientific or academic research.
*   **FundingAgency**: An organization that provides money for projects.
*   **Grant**: The actual funding award (see [Grants Guide](../intangibles/grants.md)).

---

## Comprehensive Example: Research Project (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ResearchProject",
  "name": "Project Quantum Flora",
  "description": "Investigating quantum effects in photosynthesis across desert plants.",
  "parentOrganization": {
    "@type": "CollegeOrUniversity",
    "name": "Global Science University"
  },
  "funder": {
    "@type": "FundingAgency",
    "name": "National Science Foundation"
  },
  "subProject": [
    { "@type": "Project", "name": "Cactus Quantum Mapping" }
  ],
  "startDate": "2024-01-01",
  "endDate": "2026-12-31",
  "keywords": ["Quantum Biology", "Botany", "Photosynthesis"]
}
```

## Tips for Projects
*   **Hierarchies**: Use `parentOrganization` and `subProject` to show how complex initiatives fit together.
*   **Funding**: Always link the `funder` to give the project authority.
*   **Team**: Use `member` or `employee` (role based) to list the research team.
*   **Outputs**: Link to `ScholarlyArticle` or `Dataset` created by the project.

## Things to Avoid
*   **Vague Goals**: Be specific in the `description` about what the project aims to achieve.
*   **Missing Dates**: Always include `startDate` and, if known, the projected `endDate`.
