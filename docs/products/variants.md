# Product Variants & ProductGroups

When a product comes in different versions—such as different colors, sizes, flavors, or materials—Schema.org provides the `ProductGroup` and `hasVariant` mechanisms to describe these relationships clearly.

## Core Concepts

*   **ProductGroup**: Represents the "parent" entity for a group of related product variants.
*   **variesBy**: A property on the `ProductGroup` that lists which properties differentiate the variants (e.g., `color`, `size`, `flavor`).
*   **hasVariant**: A property on the `ProductGroup` that links to individual `Product` variants.
*   **additionalProperty**: Used for attributes like "flavor" that are not standard Schema.org properties.

---

## Comprehensive Example: Coffee with Different Flavors & Sizes (JSON-LD)

This example shows a single "Product Group" (Coffee Beans) that varies by both flavor and weight. Since **flavor** is not a standard Schema.org property, we use the `additionalProperty` pattern.

```json
{
  "@context": "https://schema.org",
  "@type": "ProductGroup",
  "name": "Artisan Roast Coffee Beans",
  "description": "Premium whole bean coffee available in multiple flavors and bag sizes.",
  "@id": "https://example.com/products/coffee-group",
  "variesBy": [
    "https://schema.org/additionalProperty",
    "https://schema.org/weight"
  ],
  "brand": {
    "@type": "Brand",
    "name": "RoastMaster"
  },
  "hasVariant": [
    {
      "@type": "Product",
      "sku": "RM-VAN-500",
      "name": "Artisan Roast Coffee - Vanilla (500g)",
      "additionalProperty": [
        {
          "@type": "PropertyValue",
          "name": "Flavor",
          "value": "Vanilla"
        }
      ],
      "weight": {
        "@type": "QuantitativeValue",
        "value": "500",
        "unitCode": "GRM"
      },
      "offers": {
        "@type": "Offer",
        "price": "15.00",
        "priceCurrency": "USD",
        "availability": "https://schema.org/InStock"
      }
    },
    {
      "@type": "Product",
      "sku": "RM-CHO-500",
      "name": "Artisan Roast Coffee - Chocolate (500g)",
      "additionalProperty": [
        {
          "@type": "PropertyValue",
          "name": "Flavor",
          "value": "Chocolate"
        }
      ],
      "weight": {
        "@type": "QuantitativeValue",
        "value": "500",
        "unitCode": "GRM"
      },
      "offers": {
        "@type": "Offer",
        "price": "16.00",
        "priceCurrency": "USD",
        "availability": "https://schema.org/InStock"
      }
    }
  ]
}
```

---

## Comprehensive Example: Clothing with Different Colors (JSON-LD)

Color is a standard property, so it can be used directly.

```json
{
  "@context": "https://schema.org",
  "@type": "ProductGroup",
  "name": "Essential Cotton T-Shirt",
  "variesBy": [ "https://schema.org/color" ],
  "hasVariant": [
    {
      "@type": "Product",
      "color": "Black",
      "image": "https://example.com/tshirt-black.jpg",
      "sku": "TS-BLK",
      "offers": {
        "@type": "Offer",
        "price": "20.00",
        "priceCurrency": "USD"
      }
    },
    {
      "@type": "Product",
      "color": "White",
      "image": "https://example.com/tshirt-white.jpg",
      "sku": "TS-WHT",
      "offers": {
        "@type": "Offer",
        "price": "20.00",
        "priceCurrency": "USD"
      }
    }
  ]
}
```

## Tips for Variants
*   **Unrecognized Properties**: If you need to include an attribute that isn't in Schema.org (like `flavor`, `pattern`, or `connectionType`), always use `additionalProperty`.
*   **Distinct SKUs**: Every variant must have its own unique `sku`.
*   **Common Properties**: Put properties that are shared by all variants (like `brand`) in the `ProductGroup`.

## Things to Avoid
*   **Direct Use of Non-standard Keys**: Don't use `"flavor": "Vanilla"` directly in the JSON; it will fail validation.
*   **Vague VariesBy**: If you vary by a custom property, use `https://schema.org/additionalProperty` in the `variesBy` array.
