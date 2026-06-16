# Email Markup & Schema Actions

Documentation for using Schema.org within emails to enable "Actions" (like confirming a reservation) directly in the user's inbox.

## Core Types

*   **EmailMessage**: The base type for an email.
*   **ConfirmAction**: Used for one-click confirmations.
*   **ViewAction**: Deep-linking from email to a web page.
*   **RsvpAction**: For event invitations.

---

## Comprehensive Example: One-Click Confirmation Email (JSON-LD)

This JSON-LD would be placed in the `<head>` of an HTML email to show a "Confirm" button in Gmail or Outlook.

```json
{
  "@context": "https://schema.org",
  "@type": "EmailMessage",
  "potentialAction": {
    "@type": "ConfirmAction",
    "name": "Confirm Subscription",
    "handler": {
      "@type": "HttpActionHandler",
      "url": "https://example.com/confirm?token=12345"
    }
  },
  "description": "Confirm your subscription to the Tech Insights newsletter."
}
```

## Tips for Email Markup
*   **Action Handlers**: Always use `HttpActionHandler` for actions that happen via a URL.
*   **Gmail/Outlook Verification**: Most providers require you to register with them (e.g., Google's "Actions in the Inbox" whitelist) before they will display your actions.
*   **Limited Types**: Use standard types like `FlightReservation`, `ParcelDelivery`, or `EventReservation` for maximum compatibility with automated inbox features.

## Things to Avoid
*   **Broken URLs**: Ensure the `url` in the handler is absolute and publicly accessible.
*   **Overwhelming the User**: Don't add multiple complex actions to a single email.
*   **Untrusted Senders**: Email providers won't show schema from senders with poor reputation or missing SPF/DKIM records.
