# Search & Find Actions

Documentation for actions that involve finding, checking, and tracking items.

## Core Types

*   **SearchAction**: Searching for an item (e.g., sitelinks searchbox).
*   **CheckAction**: Verifying the state or presence of an item.
*   **DiscoverAction**: Finding new items or information.
*   **TrackAction**: Tracking the status or location of an item (e.g., parcel tracking).

---

## Comprehensive Example: Parcel Tracking (JSON-LD)

This example shows how a carrier would document the ability to track a package.

```json
{
  "@context": "https://schema.org",
  "@type": "ParcelDelivery",
  "name": "Order #98765",
  "carrier": {
    "@type": "Organization",
    "name": "Global Parcel Service"
  },
  "potentialAction": {
    "@type": "TrackAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://example.com/track?id=98765",
      "actionPlatform": [
        "http://schema.org/DesktopWebPlatform",
        "http://schema.org/MobileWebPlatform"
      ]
    }
  }
}
```

## Tips for Find Actions
*   **Search Templates**: For `SearchAction`, use `urlTemplate` with placeholders like `{search_term_string}`.
*   **Tracking**: Combine `TrackAction` with `ParcelDelivery` or `Order` for high-value user experience.
*   **State Checking**: Use `CheckAction` for things like "Check Availability" on a product or "Check-in" for a flight.

## Things to Avoid
*   **Broken Search Templates**: Test your URL templates to ensure the search term is passed correctly.
*   **Confusing with PotentialAction**: Most "Find" actions should be marked as `potentialAction` to show the user what they *can* do.
