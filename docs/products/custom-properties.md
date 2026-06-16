# Custom & Technical Properties

Not every product attribute is defined in the Schema.org vocabulary. For attributes like "Flavor", "Voltage", or specialized "Material Grades", you must use the `additionalProperty` mechanism.

## The additionalProperty Mechanism

The `additionalProperty` property accepts an array of `PropertyValue` objects. This allows you to define any name-value pair in a way that machines can still parse.

### Key Properties of PropertyValue
*   **name**: The label of the attribute (e.g., "Voltage").
*   **value**: The actual value (e.g., "220V").
*   **unitCode**: (Optional) Standardized unit code (e.g., `VLT` for Volts).
*   **propertyID**: (Optional) A link to a formal definition of this property (e.g., from GS1 or a Wikipedia entry).

---

## Comprehensive Example: Product with Custom Attributes (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Industrial Power Drill",
  "brand": { "@type": "Brand", "name": "PowerTool" },
  "additionalProperty": [
    {
      "@type": "PropertyValue",
      "name": "Operating Voltage",
      "value": "18",
      "unitCode": "VLT"
    },
    {
      "@type": "PropertyValue",
      "name": "Motor Type",
      "value": "Brushless",
      "propertyID": "https://en.wikipedia.org/wiki/Brushless_DC_electric_motor"
    },
    {
      "@type": "PropertyValue",
      "name": "Flavor",
      "value": "Vanilla"
    }
  ]
}
```

## Tips for Custom Properties
*   **Be Specific**: Use clear names for your properties.
*   **Standardize Units**: Whenever possible, use `unitCode` with [UN/CEFACT](https://www.unece.org/cefact/codesfortrade/codes_index.html) codes.
*   **Linking**: Use `propertyID` to point to an external definition of the property. This is highly valued by AI agents and technical search engines.

## Things to Avoid
*   **Direct Key Injection**: Avoid adding keys like `"flavor": "Vanilla"` directly to your `Product` object. They will be ignored or flagged as errors by most validators.
*   **Duplicate Standard Properties**: If a standard Schema.org property exists (like `color` or `weight`), use it instead of `additionalProperty`.
