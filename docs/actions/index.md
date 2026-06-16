# Actions Schema Documentation

An `Action` represents an action performed by an entity, often on another entity.

## Detailed Guides

*   [Achieve & Trade Actions](trade.md) - Buying, Selling, Winning.
*   [Consume & Interact Actions](interact.md) - Reading, Watching, Subscribing.
*   [Organize & Plan Actions](plan.md) - Reserving, Scheduling, Applying.
*   [Create & Update Actions](update.md) - Writing, Painting, Deleting.
*   [Mobile & Deep Linking](mobile-deeplinking.md) - App entry points and deep links.

## Generic Action Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Action",
  "actionStatus": "https://schema.org/CompletedActionStatus",
  "agent": {
    "@type": "Person",
    "name": "Alice"
  },
  "object": {
    "@type": "Book",
    "name": "The Great Gatsby"
  },
  "startTime": "2025-01-01T10:00:00Z",
  "endTime": "2025-01-01T10:05:00Z"
}
```
