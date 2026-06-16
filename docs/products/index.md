# Products Schema Documentation

A `Product` is anything that is made available for sale.

## Detailed Guides

*   [Physical Dimensions](dimensions.md) - Weight, height, width, and depth.
*   [Product Identifiers](identifiers.md) - GTIN, SKU, MPN.
*   [Advanced Offers & Shipping](advanced-offers.md) - Pricing, delivery, and returns.
*   [Vehicles](vehicles.md) - Cars, motorcycles, and more.
*   [Product Variants](variants.md) - Colors, flavors, sizes, and groups.
*   [Energy & Appliances](appliances.md) - Energy efficiency and consumption.
*   [Custom Properties](custom-properties.md) - Handling flavor, voltage, and non-standard attributes.
*   [Sizing & Specs](sizing.md) - Product sizes, systems, and groups.

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
