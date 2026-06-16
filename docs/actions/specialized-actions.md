# Specialized & Complex Actions

Documentation for niche or technically specific actions.

## Core Types

*   **SolveMathAction**: The act of solving a mathematical problem.
*   **PlayGameAction**: Specifically for playing a game.
*   **MoneyTransfer**: The act of transferring money.
*   **BefriendAction**: A social action of making a friend.
*   **VoteAction**: Casting a vote.
*   **ResumeAction**: Resuming a previously suspended action.

---

## Comprehensive Example: MoneyTransfer (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MoneyTransfer",
  "agent": {
    "@type": "Person",
    "name": "Alice"
  },
  "recipient": {
    "@type": "Person",
    "name": "Bob"
  },
  "amount": {
    "@type": "MonetaryAmount",
    "value": "100.00",
    "currency": "USD"
  },
  "beneficiaryBank": {
    "@type": "BankOrCreditUnion",
    "name": "Global Bank"
  },
  "description": "Payment for freelance design work."
}
```

## Tips for Specialized Actions
*   **Agents & Recipients**: Always clearly define the `agent` (who does it) and the `recipient` or `object` (who/what it's done to).
*   **Status**: Use `actionStatus` (Completed, Failed, Active) for recorded actions.
*   **SolveMathAction**: Use the `eduQuestionType` and `assesses` properties if this is part of an educational resource.

## Things to Avoid
*   **Mixing Up Types**: Don't use `MoneyTransfer` for a purchase; use `PayAction` or `BuyAction`.
*   **Missing Outcomes**: If an action results in something (like a `friendship`), use the `result` property.
