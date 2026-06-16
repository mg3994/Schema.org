# Consume & Interact Actions

Documentation for actions involving media consumption and social interaction.

## Core Types

### Consumption
*   **WatchAction**: Watching a video or movie.
*   **ListenAction**: Listening to audio or music.
*   **ReadAction**: Reading a book or article.
*   **ViewAction**: Viewing a webpage or image.
*   **EatAction / DrinkAction**: Consuming food or drink.
*   **UseAction**: Generic use of an item.
*   **WearAction**: Wearing clothing.

### Interaction
*   **CommunicateAction**: Sending a message.
*   **AskAction**: Asking a question.
*   **CommentAction**: Making a comment.
*   **ReplyAction**: Replying to a comment.
*   **ShareAction**: Sharing content.
*   **FollowAction**: Following a person or entity.
*   **SubscribeAction**: Subscribing to a service.
*   **JoinAction / LeaveAction**: Joining or leaving a group.
*   **BefriendAction**: Making a friend.
*   **MarryAction**: Getting married.

---

## Comprehensive Example: WatchAction (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "WatchAction",
  "agent": {
    "@type": "Person",
    "name": "Bob"
  },
  "object": {
    "@type": "Movie",
    "name": "Inception"
  },
  "actionStatus": "https://schema.org/ActiveActionStatus",
  "startTime": "2025-01-01T20:00:00Z"
}
```

## Tips for Interaction Actions
*   **In-App Actions**: These are powerful for deep-linking from search results into specific app actions.
*   **Timestamps**: Use `startTime` and `endTime` for recorded actions.
*   **Agents**: For social interactions, the `agent` is usually a `Person`.

## Things to Avoid
*   **Privacy Violations**: Be extremely careful about marking up private user interactions.
*   **Vague Objects**: Ensure the `object` clearly defines what is being consumed or interacted with.
