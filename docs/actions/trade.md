# Trade & Commerce Actions

Documentation for actions involving trade, money, and commerce.

## Core Types

*   **BuyAction**: The act of buying something.
*   **SellAction**: The act of selling something.
*   **OrderAction**: Placing an order.
*   **PayAction**: Making a payment.
*   **RentAction**: Renting an item.
*   **TipAction**: Giving a tip.
*   **QuoteAction**: Requesting or providing a quote.
*   **PreOrderAction**: Pre-ordering an item.
*   **TradeAction**: The base for all trade actions.

---

## Comprehensive Example: OrderAction (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "OrderAction",
  "agent": {
    "@type": "Person",
    "name": "Jane Doe"
  },
  "object": {
    "@type": "Product",
    "name": "Nexus Smartphone"
  },
  "price": "799.00",
  "priceCurrency": "USD",
  "deliveryMethod": "https://schema.org/ParcelService"
}
```

## Tips for Trade Actions
*   **Price and Currency**: Always include `price` and `priceCurrency`.
*   **Agents and Objects**: Clearly define who is performing the action (`agent`) and what the action is performed on (`object`).
*   **Status**: Use `actionStatus` to track the lifecycle of the trade (Potential, Active, Completed).

## Things to Avoid
*   **Missing Financial Info**: For trade actions, financial details are almost always required for the data to be useful.
*   **Confusing Buy vs Order**: `BuyAction` is the completed purchase, while `OrderAction` is the intent or the act of placing the order.
