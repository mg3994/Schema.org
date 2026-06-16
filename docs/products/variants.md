# Product Variants & ProductGroups

When a product comes in different versions—such as different colors, sizes, flavors, or materials—Schema.org provides the `ProductGroup` and `hasVariant` mechanisms to describe these relationships clearly.

## Core Concepts

*   **ProductGroup**: Represents the "parent" entity for a group of related product variants.
*   **variesBy**: A property on the `ProductGroup` that lists which properties differentiate the variants (e.g., `color`, `size`, `flavor`).
*   **hasVariant**: A property on the `ProductGroup` that links to individual `Product` variants.
*   **isVariantOf**: (Optional) A property on an individual `Product` that links back to its parent `ProductGroup`.

---

## Comprehensive Example: Coffee with Different Flavors & Sizes (JSON-LD)

This example shows a single "Product Group" (Coffee Beans) that varies by both flavor and weight.

```json
{
  "@context": "https://schema.org",
  "@type": "ProductGroup",
  "name": "Artisan Roast Coffee Beans",
  "description": "Premium whole bean coffee available in multiple flavors and bag sizes.",
  "@id": "https://example.com/products/coffee-group",
  "variesBy": [
    "https://schema.org/flavor",
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
      "flavor": "Vanilla",
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
      "flavor": "Chocolate",
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
    },
    {
      "@type": "Product",
      "sku": "RM-VAN-1000",
      "name": "Artisan Roast Coffee - Vanilla (1kg)",
      "flavor": "Vanilla",
      "weight": {
        "@type": "QuantitativeValue",
        "value": "1",
        "unitCode": "KGM"
      },
      "offers": {
        "@type": "Offer",
        "price": "28.00",
        "priceCurrency": "USD",
        "availability": "https://schema.org/InStock"
      }
    }
  ]
}
```

---

## Comprehensive Example: Clothing with Different Colors (JSON-LD)

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
*   **Distinct SKUs**: Every variant must have its own unique `sku` and, if available, `gtin`.
*   **Variant-Specific Images**: If the variants look different (e.g., color), provide a specific `image` for each variant.
*   **VariesBy URLs**: Use the full Schema.org URL for the `variesBy` properties for maximum compatibility.
*   **Common Properties**: Put properties that are shared by all variants (like `brand`, `manufacturer`, or `description`) in the `ProductGroup` to avoid redundancy.

## Things to Avoid
*   **Flattening Everything**: Don't put all variants as a flat list of `Product` types on a page without a `ProductGroup`. This makes it harder for search engines to understand they are versions of the same thing.
*   **Missing Differentiation**: If you say a product varies by `flavor`, ensure every variant in the group has a `flavor` property.
*   **Price Ranges**: For `ProductGroup`, use `offers` as an `AggregateOffer` if you want to show the price range across all variants.
