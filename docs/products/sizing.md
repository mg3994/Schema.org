# Product Sizing & Specifications

Documentation for describing product sizes, systems, and groups.

## Core Types

*   **SizeSpecification**: Detailed info about a size.
*   **SizeSystemEnumeration**: Imperial, Metric, etc.
*   **SizeGroupEnumeration**: Regular, Petite, Plus, etc.

---

## Comprehensive Example: Clothing Size Specification (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Classic Fit Denim Jeans",
  "size": {
    "@type": "SizeSpecification",
    "name": "Medium",
    "sizeSystem": "https://schema.org/SizeSystemUS",
    "sizeGroup": "https://schema.org/WearableSizeGroupRegular",
    "suggestedMeasurement": {
      "@type": "QuantitativeValue",
      "value": "32",
      "unitCode": "INH",
      "name": "Waist"
    }
  }
}
```

## Tips for Sizing
*   **Standards**: Always link to the `SizeSystemEnumeration` (e.g., US, UK, Metric).
*   **Groups**: Use `SizeGroupEnumeration` to help users filter by fit (e.g., "Maternity", "Big & Tall").
*   **Measurements**: Provide `suggestedMeasurement` to help users find the perfect fit and reduce returns.

## Things to Avoid
*   **Vague Sizes**: Don't just use a string like "Large"; use the `SizeSpecification` object for clarity.
*   **Inconsistent Systems**: If your site uses multiple sizing systems, clearly define each one in the schema.
