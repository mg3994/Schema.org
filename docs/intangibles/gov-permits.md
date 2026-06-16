# Government Permits & Legislation

Documentation for laws, regulations, and official permits issued by government bodies.

## Core Types

*   **Legislation**: An act, bill, or regulation.
*   **GovernmentPermit**: A permit issued by a government authority.
*   **LegislationObject**: The digital representation of a legislative act.

---

## Comprehensive Example: Legislation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Legislation",
  "name": "Environmental Protection Act 2024",
  "legislationIdentifier": "ACT-2024-001",
  "legislationType": "https://schema.org/Legislation",
  "legislationJurisdiction": {
    "@type": "AdministrativeArea",
    "name": "California"
  },
  "legislationStatus": "https://schema.org/InForce",
  "legislationDate": "2024-01-01",
  "url": "https://example.gov/laws/act-2024-001"
}
```

## Tips for Permits & Laws
*   **Status**: For legislation, use the `legislationStatus` property (InForce, Repealed).
*   **Jurisdiction**: Always specify the `legislationJurisdiction`.
*   **Permit Audience**: For `GovernmentPermit`, use `permitAudience` to show who the permit is for (e.g., "Contractors").
*   **Issuers**: Identify the `issuer` (e.g., "Department of Building Safety").

## Things to Avoid
*   **Inaccurate Dates**: For laws, the date it becomes effective is crucial.
*   **Confusing Permit with Service**: A `GovernmentPermit` is the *authorization*, while a `GovernmentService` is the *process* of getting it.
