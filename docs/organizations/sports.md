# Sports Organizations & Teams

Documentation for professional and amateur sports teams and governing bodies.

## Core Types

*   **SportsOrganization**: The base type for sports entities.
*   **SportsTeam**: A specific sports team.

---

## Comprehensive Example: SportsTeam (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SportsTeam",
  "name": "Emerald City Strikers",
  "sport": "Soccer",
  "coach": {
    "@type": "Person",
    "name": "Sarah Coachman"
  },
  "member": [
    { "@type": "OrganizationRole", "member": { "@type": "Person", "name": "Player A" }, "roleName": "Forward" },
    { "@type": "OrganizationRole", "member": { "@type": "Person", "name": "Player B" }, "roleName": "Goalkeeper" }
  ],
  "homeLocation": {
    "@type": "StadiumOrArena",
    "name": "Strikers Stadium"
  },
  "athlete": [
    { "@type": "Person", "name": "Star Athlete" }
  ]
}
```

## Tips for Sports
*   **Sport Property**: Always specify the `sport` property.
*   **Members and Roles**: Use `OrganizationRole` within the `member` property to specify player positions.
*   **Venues**: Link the team to its `homeLocation`.

## Things to Avoid
*   **Generic Organization**: Use `SportsTeam` or `SportsOrganization` for better categorization.
*   **Outdated Rosters**: Keep the `member` list updated every season.
