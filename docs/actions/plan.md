# Organize & Plan Actions

Documentation for actions involving planning, scheduling, and allocating resources.

## Core Types

### Planning
*   **PlanAction**: Generic planning.
*   **ScheduleAction**: Scheduling an event or task.
*   **ReserveAction**: Making a reservation (Restaurant, Flight).
*   **CancelAction**: Canceling a plan.

### Organizing
*   **AllocateAction**: Assigning resources.
*   **AuthorizeAction**: Giving permission.
*   **AcceptAction / RejectAction**: Accepting or rejecting an offer or invitation.
*   **ApplyAction**: Applying for a job or program.
*   **BookmarkAction**: Saving an item for later.

---

## Comprehensive Example: ReserveAction (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ReserveAction",
  "agent": {
    "@type": "Person",
    "name": "Alice"
  },
  "object": {
    "@type": "FoodEstablishmentReservation",
    "reservationFor": {
      "@type": "Restaurant",
      "name": "The Golden Fork"
    },
    "startTime": "2025-06-20T19:00:00Z",
    "partySize": 4
  },
  "result": {
    "@type": "Reservation",
    "reservationStatus": "https://schema.org/ReservationConfirmed",
    "reservationNumber": "CONF_789"
  }
}
```

## Tips for Planning Actions
*   **Result**: Use the `result` property to show what was created by the action (e.g., a `Reservation` object).
*   **Targets**: For potential actions, define the `target` so users know where to perform the plan.
*   **Party Size**: For reservations, always include the number of people.

## Things to Avoid
*   **Missing Confirmation**: Always try to include a `reservationNumber` or status in the result.
*   **Invalid Dates**: Ensure the `startTime` is in the future for potential actions.
