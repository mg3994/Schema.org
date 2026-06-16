# E-commerce Workflow: From Offer to Delivery

Documentation for describing the full lifecycle of an online transaction, including orders, invoices, and shipping.

## Core Types

*   **Offer**: The initial price and terms for a product.
*   **Order**: A record of a completed or pending transaction.
*   **OrderItem**: An individual line item within an order.
*   **Invoice**: A statement of money owed for an order.
*   **ParcelDelivery**: Information about the physical shipment of the order.

---

## Comprehensive Example: The Transaction Lifecycle (JSON-LD)

This example shows how these entities link together to describe a complete e-commerce flow.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Order",
      "@id": "https://example.com/orders/12345",
      "orderNumber": "12345",
      "orderStatus": "https://schema.org/OrderProcessing",
      "customer": {
        "@type": "Person",
        "name": "Jane Doe"
      },
      "seller": {
        "@type": "Organization",
        "name": "Gadget Store"
      },
      "orderDate": "2025-04-01T10:00:00Z",
      "orderedItem": [
        {
          "@type": "OrderItem",
          "orderedItem": {
            "@type": "Product",
            "name": "Super Smartphone"
          },
          "orderQuantity": 1
        }
      ],
      "partOfInvoice": {
        "@type": "Invoice",
        "confirmationNumber": "INV-999",
        "totalPaymentDue": {
          "@type": "MonetaryAmount",
          "value": "799.00",
          "currency": "USD"
        }
      }
    },
    {
      "@type": "ParcelDelivery",
      "deliveryAddress": {
        "@type": "PostalAddress",
        "streetAddress": "123 Maple St",
        "addressLocality": "Anytown"
      },
      "carrier": {
        "@type": "Organization",
        "name": "FastShip Logistics"
      },
      "partOfOrder": { "@id": "https://example.com/orders/12345" },
      "trackingNumber": "TRACK-7890",
      "trackingUrl": "https://fastship.com/track/7890"
    }
  ]
}
```

## Tips for E-commerce Schema
*   **Graph Linking**: Use `@graph` (as shown above) to show the relationship between the `Order` and the `ParcelDelivery`.
*   **Order Status**: Use the `OrderStatus` enumeration to keep customers informed via their email or account page.
*   **Monetary Amounts**: Always include the currency for `totalPaymentDue` and individual item prices.

## Things to Avoid
*   **Broken Tracking Links**: Ensure the `trackingUrl` is a direct link to the carrier's tracking page.
*   **Privacy**: Be extremely careful about exposing sensitive customer data in public schema blocks. These are best used in private emails or behind authenticated account pages.
