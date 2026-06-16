# Commerce & Finance Schema Documentation

Documentation for commerce-related entities like offers, orders, and payments.

## Core Types

*   **Offer**: An offer to provide an item or service.
*   **AggregateOffer**: A collection of offers (e.g., used to show a price range).
*   **Demand**: A request for an item or service.
*   **Order**: A record of a completed transaction.
*   **OrderItem**: An individual item within an order.
*   **Invoice**: A statement of money owed.
*   **PaymentMethod**: The method of payment.
*   **PaymentCard / CreditCard**: Specific payment instruments.

---

## Comprehensive Example: AggregateOffer (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Super Coffee Beans",
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "15.00",
    "highPrice": "25.00",
    "priceCurrency": "USD",
    "offerCount": "5",
    "offers": [
      {
        "@type": "Offer",
        "price": "15.00",
        "priceCurrency": "USD",
        "seller": { "@type": "Organization", "name": "Coffee Express" }
      },
      {
        "@type": "Offer",
        "price": "25.00",
        "priceCurrency": "USD",
        "seller": { "@type": "Organization", "name": "Premium Beans" }
      }
    ]
  }
}
```

## Tips for Commerce
*   **Sellers**: Always identify the `seller`.
*   **Valid Until**: Use `priceValidUntil` to show when a price expires.
*   **Conditions**: State the `itemCondition` clearly.
*   **Availability**: Use the `ItemAvailability` enums.

## Things to Avoid
*   **Missing Prices**: An offer without a price is rarely useful.
*   **Vague Sellers**: Be specific about who is selling the product.
