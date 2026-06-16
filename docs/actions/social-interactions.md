# Social Actions & Interactions

Documentation for describing user interactions like likes, dislikes, and votes.

## Core Types

*   **LikeAction**: A positive interaction.
*   **DislikeAction**: A negative interaction.
*   **EndorseAction**: A formal endorsement of an entity.
*   **WantAction**: Expressing a desire for an item.
*   **VoteAction**: Casting a vote.
*   **AgreeAction / DisagreeAction**: Expressing agreement or disagreement.

---

## Comprehensive Example: Content Endorsement (JSON-LD)

This example shows an expert endorsing a technical article.

```json
{
  "@context": "https://schema.org",
  "@type": "EndorseAction",
  "agent": {
    "@type": "Person",
    "name": "Dr. Sarah Data",
    "jobTitle": "Lead Scientist"
  },
  "object": {
    "@type": "ScholarlyArticle",
    "headline": "Quantum Computing Basics",
    "url": "https://example.com/quantum-basics"
  },
  "actionStatus": "https://schema.org/CompletedActionStatus",
  "startTime": "2025-03-01T10:00:00Z"
}
```

## Tips for Social Actions
*   **Verification**: Social actions are most powerful when the `agent` is a verified or authoritative `Person`.
*   **Counters**: Combine with `InteractionCounter` on the target object to show total counts.
*   **Status**: Use `actionStatus` to indicate if the action is currently happening (Active) or finished (Completed).

## Things to Avoid
*   **Privacy**: Be careful with marking up individual user actions on public web pages unless they are intended to be public.
*   **Fake Engagement**: Do not use schema to inflate engagement metrics artificially.
