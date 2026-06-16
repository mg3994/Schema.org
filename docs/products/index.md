# Products Schema Documentation

A `Product` is anything that is made available for sale.

## Detailed Guides

*   [Physical Dimensions](dimensions.md) - Weight, height, width, and depth.
*   [Product Identifiers](identifiers.md) - GTIN, SKU, MPN.
*   [Advanced Offers & Shipping](advanced-offers.md) - Pricing, delivery, and returns.
*   [Vehicles](vehicles.md) - Cars, motorcycles, and more.

## Core Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Standard Widget",
  "image": "https://example.com/widget.jpg",
  "description": "A high-quality widget for all your needs.",
  "sku": "WIDG-001",
  "offers": {
    "@type": "Offer",
    "price": "9.99",
    "priceCurrency": "USD"
  }
}
```
