# Publication & Broadcast Events

Documentation for broadcasts and on-demand content availability.

## Core Types

*   **PublicationEvent**: The base type for publishing something.
*   **BroadcastEvent**: A specific broadcast of content on TV or Radio.
*   **OnDemandEvent**: Availability of content on-demand (Streaming).

---

## Comprehensive Example: BroadcastEvent (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "BroadcastEvent",
  "name": "Live Election Results",
  "startDate": "2024-11-05T18:00:00Z",
  "endDate": "2024-11-06T04:00:00Z",
  "publishedOn": {
    "@type": "BroadcastService",
    "name": "Global News Network"
  }
}
```

## Tips
*   **Published On**: Use the `publishedOn` property to link to the `BroadcastService`.
*   **Availability**: For on-demand, use `startDate` to show when it becomes available.

## Things to Avoid
*   **Confusing with Content**: This is the *event* of publishing, not the content itself (which would be a `VideoObject` or `Episode`).
